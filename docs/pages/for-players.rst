For players
************


Ingame commands
================

Note: server admins can enable/disable every command. So not every command might work on the server you play on!

Calladmin
^^^^^^^^^^

Get an admins help with something! This will automatically record your location & inventory.


Usage::

    $calladmin My bike is glitched

A page for your ticket will be made on the website. An admin will (hopefully) resolve your issue soon!

Teleports
^^^^^^^^^^

Create custom teleport locations. You can set your teleport location to public and give the name to your friends. 

Set a new teleport location::

    $settele teleportName

Teleport to a location::

    $tele teleportName

Remove a teleport location::

    $removetele teleportName

List all your saved locations::

    $listtele
    
Shows all public tps for the server::

    $listtele public

Rename a location::

    $renametele oldName newName

Set a teleleport location to public::

    $telepublic teleportName

Set a teleport location to private::

    $teleprivate teleportName
    
Economy
^^^^^^^^^^
Find out your economy balance::

    $balance
    
Shop
^^^^^^

Claim all items you have purchased. Drops all claimed items at the players feet. Best to do this on a even surface. If you have more than 10 items ready to be claimed, only the first 10 will be given at a time.::

    $claim

List all items that can be claimed::

    $claim list

Replies with a link to the server shop::

    $shop

Who
^^^^^^^^^^

See who was in a certain radius around your current location. Size defaults to 150 blocks. When a large amount of players has been in your area, it will show who was there the latest. Consider keeping the area to search as small as possible for most accurate results ::

    $ who

You can specify the location to search. Min 1 max 500 ::

    $who 250