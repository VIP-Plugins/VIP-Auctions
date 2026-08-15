# VIP-Auctions

Paper, Folia, and ShreddedPaper auction house by **VIP Plugins**. Buy Now, bidding, and item-frame booths.

**Version:** Alpha-1.0.0  
**Minecraft:** 1.21.11  
**Java:** 21

## Features

- Buy Now and bidding listings
- GUI browse, search, category sort, and Buy/Bid filters
- Sign + item frame booths (Buy booths and Bid booths)
- Unique listings per booth
- Vault, internal balances, or item currency
- Confirm buy/bid screens
- Collect expired, cancelled, or won items
- Folia / ShreddedPaper region-safe

## Install

1. Put `AuctionHouse-Alpha-1.0.0.jar` in your server `plugins` folder.
2. Optional: install [Vault](https://www.spigotmc.org/resources/vault.34315/) plus an economy plugin (EssentialsX, CMI, etc.).
3. Restart the server.
4. Edit `plugins/AuctionHouse/config.yml` if needed.
5. Run `/auction reload` after config changes. Reload does not wipe live listings.

If Vault is missing, the plugin uses internal balances. Admins can `/auction eco give <player> <amount>`.

## Player commands

| Command | Description |
|---|---|
| `/auction` or `/ah` | Open the auction house |
| `/auction sell <price>` | List the held item as Buy Now |
| `/auction bid <starting>` | List the held item for bidding |
| `/auction search <query>` | Search listings |
| `/auction listings` | Your listings (shift-click to cancel) |
| `/auction collect` | Collect expired, cancelled, or won items |
| `/auction eco balance` | Check your balance |
| `/auction help` | Command list |

Listings last 24 hours.

## Staff commands

| Command | Description |
|---|---|
| `/auction connect buy` | Left-click a sign and item frame to make a Buy display |
| `/auction connect bid` | Left-click a sign and item frame to make a Bid display |
| `/auction disconnect` | Unpair a connected sign or frame |
| `/auction reload` | Reload configuration |
| `/auction eco give/take/set <player> <amount>` | Internal-economy balances only |

## Displays

Place an item frame above a sign, then `/auction connect buy` or `/auction connect bid` and left-click both.

- Buy booths show Buy Now listings
- Bid booths show auctions
- Each listing appears on only one booth at a time

## Permissions

Players get use, sell, buy, bid, and collect by default.

| Permission | Default | Description |
|---|---|---|
| `auctionhouse.use` | true | Open the GUI |
| `auctionhouse.sell` | true | List items |
| `auctionhouse.buy` | true | Buy listings |
| `auctionhouse.bid` | true | Place bids |
| `auctionhouse.collect` | true | Collect items |
| `auctionhouse.connect` | op | Pair booths |
| `auctionhouse.disconnect` | op | Unpair booths |
| `auctionhouse.reload` | op | Reload config |
| `auctionhouse.eco` | op | Manage internal balances |
| `auctionhouse.admin` | op | Staff commands (includes connect, disconnect, reload, eco) |

## License

MIT License. See `LICENSE`.
