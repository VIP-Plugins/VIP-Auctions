Paper, Folia, and ShreddedPaper auction house by **VIP Plugins**. Buy Now, bidding, item-frame booths, taxes, featured listings, and NBT previews.
**Version:** Alpha-1.2.0  
**Tested Minecraft Versions:** 1.21.11  
**Java:** 21
## Features
- Buy Now and bidding listings
- GUI browse, search, category sort, and Buy/Bid filters
- Sign + item frame booths (Buy booths and Bid booths)
- Unique listings per booth, optional random fill
- Empty booths show a barrier named Empty
- Vault, internal balances, or item currency
- Optional house tax (seller cut, buyer still pays full price)
- Optional featured listings (pay extra to show on booths first)
- Optional custom duration (`/auction sell 50 6h`)
- Sale, bid, and outbid notifications, plus offline mail
- Staff lookup, force-cancel, and transaction history
- Optional `log.yml`
- NBT hover preview: renamed items, enchantments, attributes, shulker/bundle contents
- Sounds on click, buy, bid, and outbid
- Language files (`lang/en.yml`)
- Folia / ShreddedPaper region-safe
## Install
1. Put `AuctionHouse-Alpha-1.2.0.jar` in your server `plugins` folder.
2. Optional: install [Vault](https://www.spigotmc.org/resources/vault.34315/) plus an economy plugin (EssentialsX, CMI, etc.).
3. Restart the server.
4. Edit `plugins/AuctionHouse/config.yml` and `plugins/AuctionHouse/lang/en.yml`.
5. Run `/auction reload` after config changes. Reload does not wipe live listings.
If Vault is missing, the plugin uses internal balances. Admins can `/auction eco give <player> <amount>`.
## Player commands
| Command | Description |
|---|---|
| `/auction` or `/ah` | Open the auction house |
| `/auction sell <price> [duration] [featured]` | List the held item as Buy Now |
| `/auction bid <starting> [duration] [featured]` | List the held item for bidding |
| `/auction search <query>` | Search listings |
| `/auction listings` | Your listings (shift-click to cancel) |
| `/auction collect` | Collect expired, cancelled, or won items |
| `/auction notify [sale\|bid\|outbid\|mail]` | View or toggle notifications |
| `/auction mail` | Read offline auction messages |
| `/auction eco balance` | Check your balance |
| `/auction help` | Command list |
Duration examples: `30m`, `6h`, `2d`, `1w`. Custom duration and featured listings are off in config until you enable them.
## Staff commands
| Command | Description |
|---|---|
| `/auction connect buy` | Left-click a sign and item frame to make a Buy display |
| `/auction connect bid` | Left-click a sign and item frame to make a Bid display |
| `/auction disconnect` | Unpair a connected sign or frame |
| `/auction admin lookup <id>` | Look up a listing by ID |
| `/auction admin cancel <id>` | Force-cancel a listing (refunds the high bidder) |
| `/auction admin history [player]` | Recent sales and bids |
| `/auction reload` | Reload configuration |
| `/auction eco give/take/set <player> <amount>` | Internal-economy balances only |
Listing IDs are shown on item hover in the GUI.
## Displays
Place an item frame above a sign, then `/auction connect buy` or `/auction connect bid` and left-click both.
- Buy booths show Buy Now listings
- Bid booths show auctions
- Each listing appears on only one booth at a time (when unique listings is on)
- Featured listings are assigned to booths before random ones
## Config (off by default)
These stay off until you turn them on in `config.yml`:
- `tax.enabled` — house cut from seller payout
- `featured.enabled` — pay extra to display first on booths
- `listings.custom-duration` — `/auction sell 50 6h`
- `logging.enabled` — write `log.yml`
Random booth assignment (`displays.random`) is on by default.
Chat text is in `plugins/AuctionHouse/lang/en.yml`, not `config.yml`.
## Permissions
Players get use, sell, buy, bid, collect, and notify by default.
| Permission | Default | Description |
|---|---|---|
| `auctionhouse.use` | true | Open the GUI |
| `auctionhouse.sell` | true | List items |
| `auctionhouse.buy` | true | Buy listings |
| `auctionhouse.bid` | true | Place bids |
| `auctionhouse.collect` | true | Collect items |
| `auctionhouse.notify` | true | Notification toggles |
| `auctionhouse.connect` | op | Pair booths |
| `auctionhouse.disconnect` | op | Unpair booths |
| `auctionhouse.reload` | op | Reload config |
| `auctionhouse.eco` | op | Manage internal balances |
| `auctionhouse.admin` | op | Staff commands (includes connect, disconnect, reload, eco) |
## License
MIT License. See `LICENSE`.
