This plugin connects your [Tip4serv.com](https://tip4serv.com/) store to your Rust Oxide server. It checks if a player has made a donation on your Tip4Serv store and delivers the order in a minute (group, inventory item...) by typing commands in the server console.

## HMAC authentication

Tip4serv adds a layer of security using HMAC authentication to communicate. It is a strong authentication method that is used by banks https://en.wikipedia.org/wiki/HMAC

## Installation

Open an account on [Tip4serv.com](https://tip4serv.com/), follow the instructions and add a Rust server.

1) Drag and drop `tip4serv.cs` into the oxide `plugins` directory on your Rust server.
2) Reload the plugin by typing `oxide.reload Tip4serv` in your Rust server console.
3) Set `key` to your tip4serv API key in the config file `tip4serv.json`.
4) Reload plugin by typing `oxide.reload Tip4serv` in console.

> You should get this message: **Server has been successfully connected**

## Setting up commands on Tip4Serv

***Before setting up your commands on Tip4serv.com, you should know that command work in your server's console (not ingame as an admin).***

Here are some commands you can use in the products configuration: [MY PRODUCTS](https://tip4serv.com/dashboard/my-products)

Add a player to a group previously created with oxide.group add [group-name]:

`oxide.usergroup add {steam_id} [group-name]`

Remove a player from a group:

`oxide.usergroup remove {steam_id} [group-name]`

Give a permission to a player:

`oxide.grant user {steam_id} [permission-name]`

Remove a permission from a player:

`oxide.revoke user {steam_id} [permission-name]`

## Give an inventoy item or a kit

[Give plugin is required](https://umod.org/plugins/give)

Give an item to a player inventory:

`giveto {steam_id} (item-short-name) (quantity)`

Give a kit to a player:

`givekitto {steam_id} (kit-name)`

## Need help?

[Contact us](https://tip4serv.com/contact)