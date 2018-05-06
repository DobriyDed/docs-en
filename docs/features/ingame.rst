In-game features
=================

Country ban
-----------

Select countries that you do not wish on your server. CSMM will automatically kick anyone joining from an IP in these countries.

**Note** This is very naive protection. Users can get around this with VPN/proxies. 

Commands
--------

calladmin
^^^^^^^^^^
Create a support ticket. CSMM will collect some data such as your inventory and location to display along the ticket.

Custom commands
^^^^^^^^^^^^^^^^

Admins can create custom ingame commands. You can set delay, timeout, cost of the command.

**note: If a custom command has same name as an existing csmm command, the existing csmm command will always take precendence. the custom command never gets executed**

For example: 

$discord::

    say linkToDiscord

You can execute multiple commands by separating with ";"::

    say "Here is one message";say "Here is the second!"

You have access to the players steam and entity ID with "${steamId}" and "${entityId}"::

    sayplayer ${entityId} "WAZAAAAAAAAAAAAA"


Examples

$safehouse::

    teleportplayer ${entityId} 15 85 -53; sayplayer ${steamId} "You are safe now."

$animals::

    spawnmultipleentity ${entityId} 5 @ 59 59 60 61
    
$animals-advanced::

    spawnmultipleentity ${entityId} 5 @ 59 59 59 59 64

$brutality::

    say "Die Bitch" ;spawnmultipleentity ${entityId} 15 @ 2 3 4 5 6 9 15 15 15 17 18 19 21 31 31 35 40 40 45 46 53 56 63 63 63 63 64 67 67 67 70

Spawnmultipleentity is a coppis command for anyone without see example below::

    Spawnentity ${entityId} 59 ;Spawnentity ${entityId} 59
    
Message of the day
------------------

Set a message to be sent to players when they join the server and/or show this message periodically to all players.

This is useful to advertise your discord server, remind people to abide by the rules etc



Support tickets
-----------------

Players can create support tickets with the corresponding command (if enabled). This is a great way for players to ask admins for some assistance, even when there is no admin currently online.

Economy
---------

The economy module allows admins to set a cost to multiple actions (teleports, custom commands, ...). Players can earn money by being ingame or via discord (discord text earner)  the player logins to csmm goes to there profile page and logs with discord

currency name is also configurable: name the currency yourself

Shop
^^^^

*Donators now have access to the new shop from the economy panel*

*Admins can add items to the shop, set the amount quality and price*

*Players go to the same page (eg https://csmm.catalysm.net/shop/42) and can purchase items there*

*Once purchased they can be claimed ingame with the new claim command*
    
.. image:: ../images/Features-Economy-Shop.png
    
