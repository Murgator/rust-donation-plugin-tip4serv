## Donation plugin for Rust (Tip4Serv)

This plugin connects your [Tip4serv.com](https://tip4serv.com/) store to your Rust oxide server.
It checks if a player has made a donation on your Tip4Serv store and delivers the order in a minute (group, inventory item...) by typing commands in the server console

#### HMAC authentification

Tip4serv adds a layer of security using HMAC authentication to communicate. It is a strong authentication method that is used by banks https://en.wikipedia.org/wiki/HMAC

#### Dependency

Install oxyde mod on your server: [https://umod.org/](https://umod.org/games/rust)

#### Installation

Open an account on [Tip4serv.com](https://tip4serv.com/), follow the instructions and add a Rust server.

1) Drag and drop `tip4serv.cs` into the oxide `plugins` directory on your Rust server.
2) Reload the plugin by typing `oxide.reload Tip4serv` in your Rust server console.
3) Set `key` to your tip4serv API key in the config file `tip4serv.json`.
4) Reload plugin by typing `oxide.reload Tip4serv` in console.

You should get this message: **Server has been successfully connected**

## Setting up commands on Tip4Serv

***Before setting up your commands on Tip4serv.com, you should know that command work in your server's console (not ingame as an admin).***

Here are some commands you can use in the products configuration: [MY PRODUCTS](https://tip4serv.com/dashboard/my-products)

##### oxide.usergroup add {steam_id} [group-name]

Add a player to a group previously created with `oxide.group add [group-name]`

Examples: 

`oxide.usergroup add {steam_id} vip`

##### oxide.usergroup remove {steam_id} [group-name]

Remove a player from a group

Examples: 

`oxide.usergroup remove {steam_id} vip`

##### oxide.grant user {steam_id} [permission-name]

Give a permission to a player

Examples: 

`oxide.grant user {steam_id} vanish.permanent`

##### oxide.revoke user {steam_id} [permission-name]

Remove a permission from a player

Examples: 

`oxide.grant revoke {steam_id} vanish.permanent`

## Give an inventoy item or a kit

[Give plugin is required](https://umod.org/plugins/give)

##### giveto {steam_id} [item-short-name] [quantity]

Give an item to a player inventory.

Example: `giveto {steam_id} apple 1`

##### givekitto {steam_id} [kit-name]

Give a kit to a player.

Example: `givekitto {steam_id} premium`

## Need help ?

[Contact us](https://tip4serv.com/contact)
