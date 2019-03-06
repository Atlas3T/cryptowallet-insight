Bitcore Node Dash with Insight Docker
=========
### Installing

From the same directory as the dockerfle:

`docker build -t <bitcore-docker-dash> .`

Run Dash testnet (the default):

`docker run -d -p 3005:3005 -p 19999:19999 -v /root/dash-node/testnet --name dash-testnet bitcore-docker-dash`

Run Dash mainnet:

`docker run -e DASH_LIVENET=1 -d -p 3005:3005 -p 9999:9999 -v /root/dash-node/livenet --name dash-livenet bitcore-docker-dash`


### Environment variables

- `DASH_LIVENET` (default: 0) - Set 1 to enable livenet
- `API_ROUTE_PREFIX` (default: api) - Set URL prefix for Insight API
- `UI_ROUTE_PREFIX` (default: "") - Set URL prefix for Insight UI
- `API_CACHE_ENABLE` (default: 1) - Enable/disable Insight API cache
- `API_LIMIT_ENABLE` (default: 1) - Enable/disable Insight API rate limiter
- `API_LIMIT_WHITELIST` (default: "127.0.0.1 ::1") - Whitelist, delimited by space
- `API_LIMIT_BLACKLIST` (default: "") - Blacklist, delimited by space
- `API_LIMIT_COUNT` (default: 10800)
- `API_LIMIT_INTERVAL` (default: 10800000)
- `API_LIMIT_WHITELIST_COUNT` (default: 108000)
- `API_LIMIT_WHITELIST_INTERVAL` (default: 10800000)
- `API_LIMIT_BLACKLIST_COUNT` (default: 0)
- `API_LIMIT_BLACKLIST_INTERVAL` (default: 10800000)