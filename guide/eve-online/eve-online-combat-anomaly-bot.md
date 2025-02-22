# EVE Online Combat Anomaly Bot

This bot uses the probe scanner to warp to combat anomalies and kills rats using drones and weapon modules.

## Features

+ **safe**: does not inject into or write to the EVE Online client. That is why using it with EVE Online is not detectable.
+ **accurate & robust**: This bot uses Sanderling memory reading to get information about the game state and user interface.

## Setting up the Game Client

Despite being quite robust, this bot is far from being as smart as a human. For example, its perception is more limited than ours, so we need to set up the game to make sure that the bot can see everything it needs to. Following is the list of setup instructions for the EVE Online client:

+ Set the UI language to English.
+ Undock, open probe scanner, overview window and drones window.
+ Set the Overview window to sort objects in space by distance with the nearest entry at the top.
+ In the ship UI, arrange the modules:
  + Place to use in combat (to activate on targets) in the top row.
  + Hide passive modules by disabling the check-box `Display Passive Modules`.
+ Configure the keyboard key 'W' to make the ship orbit.

## Starting the Bot

To start the bot, download the script from https://catalog.botlab.org/6768ac24433ab268f62a0177dba2639b70aee4b32c6b4cf98f0d9381f7188a49 and then run it.

In case the BotLab client program is not yet installed on your system, the script will redirect you to the installation guide at https://to.botlab.org/guide/how-to-install-the-botlab-client-and-register-the-botlab-command

After completing the installation, run the script again to start the bot.

The bot needs a few seconds to start and find the EVE Online client process. It also shows status messages to inform what it is doing at the moment and when the startup is complete.

![EVE Online App Starting](./image/2019-10-08.eve-online-autopilot-bot-startup.png)

From here on, the bot works automatically. It detects the topmost game client window and starts working in that game client.

## Configuration Settings

All settings are optional; you only need them in case the defaults don't fit your use-case.

+ `anomaly-name` : Choose the name of anomalies to take. You can use this setting multiple times to select multiple names.
+ `hide-when-neutral-in-local` : Set this to 'yes' to make the bot dock in a station or structure when a neutral or hostile appears in the 'local' chat.
+ `rat-to-avoid` : Name of a rat to avoid, as it appears in the overview. You can use this setting multiple times to select multiple names.
+ `module-to-activate-always` : Text found in tooltips of ship modules that should always be active. For example: "shield hardener".

When using more than one setting, start a new line for each setting in the text input field.
Here is an example of a complete settings string:

```
anomaly-name = Drone Patrol
anomaly-name = Drone Horde
hide-when-neutral-in-local = yes
rat-to-avoid = Infested Carrier
module-to-activate-always = shield hardener
```

----

In case I forgot to add something here or you have any questions, don't hesitate to ask on the [BotLab forum](https://forum.botlab.org/).

## Pricing and Online Sessions

You can test the bot for free. When you want the bot to run more than 15 minutes per session, use an online session as explained at [https://to.botlab.org/guide/online-session](https://to.botlab.org/guide/online-session)

Online sessions cost 2000 credits per hour. To add credits to your account, follow the instructions at https://reactor.botlab.org/billing/add-credits

For more about purchasing and using credits, see the guide at https://forum.botlab.org/t/purchasing-and-using-botlab-credits-frequently-asked-questions-faq/837

## Running Multiple Instances

This bot supports running multiple instances on the same desktop. In such a scenario, the individual bot instances take turns sending input and coordinate to avoid interfering with each other's input. To learn more about multi-instance setup, see https://to.botlab.org/guide/running-bots-on-multiple-game-clients

