Quick Start
===========

Install `Allocs Fixes <https://7dtd.illy.bz/wiki/Server%20fixes>`_.
--------------------------------------------------------------------

Confirm the webserver is up and running. To do this, you can type ``ip:port`` in your browser. You should see the dynamic map page.

The webserver uses ControlPanelPort+2 as port. You can find ControlPanelPort in your serverconfig.xml.  
  ControlPanelPort could also be called query port on some larger hosting providers

Set up authentication credentials for CSMM
--------------------------------------------

Connect to your server console (telnet, webpanel, ingame should all work) and execute these commands.

Check if you have any set up already::

  webtokens list

Add a new token::

  webtokens add <name> <token> 0

Don't forget the 0 at the end! It's important CSMM has privilege 0 to ensure all functions can properly work.

Reload permissions::

  reloadwebpermissions

**These credentials are sensitive! You should treat these as a password. (Keep it secret, no obvious names/tokens)**
**its advised to use a combination of numbers, letters, lowercase and uppercase aswell as symbols**

*It is highly recommended to remove any tokens that are not being used.*

Add your server 
----------------

Go to the website, login and navigate to the add server page. Fill in the info, click submit and you will be taken to your servers dashboard.

Add an admin 
----------------

**how to add an admin to your csmm server**

*first get the admin to login to csmm with steam this will create a profile*

*then go to csmm settings -> Basic server settings -> blue button "add/remove admins" -> enter the admins steamid and click Add*

*once you have done this the admins name and steamid should show on the right hand side*


