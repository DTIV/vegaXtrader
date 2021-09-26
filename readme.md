ViteX Trader
------------

Discordf Set Up
-
1. Create a Discord Server
2. Create a discord bot
    a) https://https://discord.com/developers/applications
    b) Create a New Application and create a new bot
    
3. Create invite url
    OAuth2 > Scopes check bot
    OAuth2 > Permissions set permissions
    
    PERMISSIONS
    -----------
    - Send Messages
    - Manage Messages
    - Read Message History
    - Attach Files
    - View Channels
    
4. Invite Bot in Channel
    -follow url in OAuth2 > Scopes
    

Bot Setup
-

1. Create ViteX wallet
2. Add whitelisted tading pairs to Delegation
3. Create Virtual Env
4. Clone Git Repo
5. pip install requirements.txt
6. Create config.json using sample_config.json
    - Add only the trading pairs that are delegated to the whitelist

    "live": Live Trading,
    "interval": 5m 15m 30m 1h 2h 4h 6h 8h 12h 1d 3d 1w
    "testnet": "https://api.vitex.net/test",
    "mainnet": "https://api.vitex.net",
    "quote_currency": "USDT-000", "BTC-000","ETH-000"
    "discord_token": "YOUR_DISCORD_TOKEN",
    "discord_channel": "YOUR_DISCORD_CHANNEL",
    "stoploss": Defined Stoploss in percent,
    "takeprofit" : Defined Takeprofit in percent,
    "status_updates": Defined notification time in minutes,
    "size": Order Size if dynamic_size is false,
    "dynamic_size": Determines size based on available funds,
    "vite_key": "YOUR_VITE_KEY",
    "vite_secret": "YOUR_VITE_SECRET",
    "viteconnect_address": "VITE_CONNECT_ADDRESS",  (optional: api requests that require address) (None as value)
    "delegation_address": "VITE_DELEGATION_ADDRESS", (optional: api requests that require address) (None as value)
    "whitelist": SELECTED TRADING PAIRS 
        - PRE DEFINED WHITELIST FOR MOST ACCURATE PAIRS


7. (optional) Define Custom Strategy in Strategy.py 
    -A Bollingerband RSI strategy is used as and example

8. run python vitetrader.py