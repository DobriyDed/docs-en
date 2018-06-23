FAQ
===========

How do I link my discord profile to CSMM?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Go to your profile page on CSMM, look for the Discord ID section and click the Discord icon to log in.

How do I add other people as admin on CSMM?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Make sure the admin has logged in to CSMM at least once, to make sure he/she has a user profile. Next, go to your server settings -> Basic server settings -> add/remove admins.
Fill in the new admins steam ID there, CSMM will look to find a profile with corresponding steam ID.

Note that admins will have full control of your server on CSMM. Be careful who you give this permission to!


How does the import/export system work?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Data is exchanged in JSON format. JSON is very much like XML, a data transfer syntax.
It doesn't need as much syntax fluff as XML, it's very simple!

An example of what a shop export looks like ::

	[
		{
			"name": "bottledWater",
			"friendlyName": "water",
			"amount": 5,
			"quality": 0,
			"price": 5
		},
		{
			"name": "cornBread",
			"friendlyName": "food",
			"amount": 5,
			"quality": 0,
			"price": 5
		},
		{
			"name": "turd",
			"friendlyName": "shit mate",
			"amount": 100,
			"quality": 0,
			"price": 1000
		},
		{
			"name": "baconAndEggs",
			"friendlyName": "baconAndEggs",
			"amount": 50,
			"quality": 0,
			"price": 2000
		}
	]

In JSON, [] means multiple entries (array) and {} means an object. In practice, what this means for CSMM import/export is that every import statement will start with [ and end with ]. Every {} denotes a new entry (shop listing, cron job or custom command) which holds the keys and values.

To get started with this method of configuration, it's recommended to create 2-3 entries via the web interface and exporting those to a file. That will show you the fields that can be configured and give you a good baseline to build the rest of your config.

Some important pointers for JSON syntax 
 - Note the , after every object except the last object.
 - Every string has " " around it
 - Numbers or boolean values (true/false) don't need " "

When you import your data, it is still validated by the same rules as you would do it via the web interface. This means that itemNames in shop must be valid item names on your server, commands need to be valid etc 


How do I have CSMM commands from ingame chat?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This functionality requires an API mod. CSMM cannot provide it but the mod Coppi's additions provides a very useful command 'tcch' which can hide messages starting with a certain prefix from chat. Since v4.92 it supports multiple prefixes.
