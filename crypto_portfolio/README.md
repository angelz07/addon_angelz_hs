Community Hass.io Add-ons: Crypto Portfolio



About
Crypto Portfolio is an addon for Home Assistant to manage and track your cryptocurrency investments. With this addon, you can record your transactions, monitor the price evolution of each cryptocurrency, and visualize your overall portfolio performance.

Installation
The installation of this add-on is pretty straightforward and not different in comparison to installing any other Hass.io add-on.

Add this repository to your Hass.io instance.
Install the "Crypto Portfolio" add-on.
Start the "Crypto Portfolio" add-on.
Check the logs of the "Crypto Portfolio" add-on to see if everything went well.
Open the dashboard at http://your-home-assistant-ip:8123.
Add-on Configuration
Note: Remember to restart the add-on when the configuration is changed.

Example add-on configuration:

json

{
  "update_interval": "5min",
  "currencies": ["bitcoin", "ethereum", "matic-network"]
}
Option: update_interval
The update_interval option allows you to set how frequently the addon will fetch the latest cryptocurrency prices. Default is 5min.

Option: currencies
The currencies option allows you to specify which cryptocurrencies you want to track in your portfolio. Provide the CoinGecko IDs for each currency.

Example
When installed, the addon will provide a pre-configured dashboard to get you started. This can be edited as per your needs. Make sure you do not change the internal API proxy used by the addon.

Default home page showing some portfolio data:


