This plugin connects your [Tip4serv.com](https://tip4serv.com/) store to your Rust Oxide server. It checks if a player has made a donation on your Tip4Serv store and delivers the order in a minute (group, inventory item...) by typing commands in the server console.

## HMAC authentication

Tip4serv adds a layer of security using HMAC authentication to communicate. It is a strong authentication method that is used by banks [HMAC WIKI](https://en.wikipedia.org/wiki/HMAC)

## Price

We take a 5% commission and that’s it ! You have access to all features with no subscription required.

## Features

* Unlimited game servers & commands
* Create subscriptions plan
* Commands status tracking
* Stock management
* Deliver roles & messages on Discord
* Easily offer a product to a friend
* Create discount coupon
* Add managers for your store
* Purchase email and invoice
* Sales statistics
* Private flow for subscribers
* Custom sub-domain
* Customize store colors
* No ads

## Store available in 15 languages

English, Danish, Dutch, English, French, German, Hungarian, Italian, Norwegian, Polish, Portuguese, Romanian, Russian, Spanish, Swedish and Turkish.

## Several payment methods

Here are the payment methods you can offer your players: Card, Paypal, Google Pay, Ideal, Giropay, Bancontact, Sofort, Sepa, EPS, BACS, Multibanco, BECS, Przelexy24, BOLETO, OXXO, Afterpay.

## Installation via plugin

Open an account on [Tip4serv.com](https://tip4serv.com/), follow the instructions and add a Rust server.

- Drag and drop `tip4serv.cs` into the oxide `plugins` directory on your Rust server.
- Reload the plugin by typing `oxide.reload Tip4serv` in your Rust server console.
- Set `key` to your tip4serv API key in the config file `tip4serv.json`.
- Reload plugin by typing `oxide.reload Tip4serv` in console.

> You should get this message: **Server has been successfully connected**

## Installation via RCON
Open an account on [Tip4serv.com](https://tip4serv.com/), follow the instructions and add a Rust server.

- Click on Connect with RCON
- Enter your server IP  
- Enter your server RCON port
- Enter your server RCON password

> You should get this message: **Server has been successfully connected**

## Setting up commands on Tip4Serv

***Before setting up your commands on Tip4serv.com, you should know that command work in your server's console (not ingame as an admin).***

Here are some sample commands you can use in the products configuration: [MY PRODUCTS](https://tip4serv.com/dashboard/my-products)

But you can use any plugin commands you want.


## Give a group or permission

Add a player to a group previously created with oxide.group add [group-name]:

`oxide.usergroup add {steam_id} group-name`

Remove a player from a group:

`oxide.usergroup remove {steam_id} group-name`

Give a permission to a player:

`oxide.grant user {steam_id} permission-name`

Remove a permission from a player:

`oxide.revoke user {steam_id} permission-name`

## Give an inventory item with steam_id (advised)

**IMPORTANT: Please select the option [Player must be online] in your product editor**

`inventory.giveto {steam_id} item-short-name quantity`

Example: `inventory.giveto {steam_id} scientist 5`

See [Rust item list](https://www.corrosionhour.com/rust-item-list/)

## Give an inventory item with username

**IMPORTANT: Please select the option [Player must be online] in your product editor**

`inventory.giveto {rust_username} item-short-name quantity`

Example: `inventory.giveto {rust_username} scientist 5`

## Give an inventory item or a kit with Give plugin

**IMPORTANT: Please select the option [Player must be online] in your product editor**

You can also use [Give plugin](https://umod.org/plugins/give)

Give an item to a player inventory with Give plugin:

`giveto {steam_id} item-short-name quantity`

Example: `giveto {steam_id} fun.guitar 1`

Give a kit to a player with Give plugin:

`givekitto {steam_id} kit-name`

## Give money

Give money to a player with [Economics plugin](https://umod.org/plugins/economics)

`deposit {steam_id} amount`

## Give points

Give points to a player with [Server Rewards](https://umod.org/plugins/server-rewards)

`sr add {rust_username} amount`

## Need help?

[Contact us](https://tip4serv.com/contact)