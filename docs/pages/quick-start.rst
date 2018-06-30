Quick Start
===========

Install `Allocs Fixes <https://7dtd.illy.bz/wiki/Server%20fixes>`_.
--------------------------------------------------------------------

Allocs fixes is probably already installed on your server, if not you'll end up installing it anyway most likely.

Confirm the webserver is up and running. To do this, you can browse to ``http://ip:port`` in your browser. Replace ip and port with the values for your server (so for example you'd type something like this; http://192.168.0.1:8084) You should see the dynamic map page.

To get the port of the webserver, you will need to go into your serverconfig. xml and find the value for "ControlPanelPort".
The webserver uses ControlPanelPort+2 as port.

If you do not have direct access to your server config (usually because of hosting companies setting it up for you), you'll need to do some more digging;

 - ControlPanelPort could also be called query port on some larger hosting providers;
 - When Your server boots up, you should see a logline like this "1.234 Started Webserver on 8082" (located in output_log.txt)
 - See this page for additional information in [Allocs server fixes Docs](https://7dtd.illy.bz/wiki/Integrated%20Webserver)
 
 If you have troubles connecting to webserver page and cannot see server map, check network settings
 - server must be up and runnign and connectable by players 
 - webserver port must be 
   - PortFowarded in router NAT tables
   - Allowed to connect in router firewall
   - Allowed to connect in server's software firewall AND antivirus software

Set up authentication credentials for CSMM
--------------------------------------------

To be able to read data and execute actions on your server, you need to make a authentication name and token. 
You will create these yourself, so pick any value BUT consider that these are like the keys to your server. If you let other people know what these are or you pick easy to guess values, this is a security risk! Be smart.

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

How to add/rmove another admin account to your server 
-----------------------------------------------

First of all, new admin must login to CSMM system to create user account. You cannot add Admin without CSMM account! 

On server settings page, in "Basic server settings" section, press blue button "Add/romove admins" 
Enter SteamID (usually it's a 17-digit number). If SteamID is correct and user have CSMM account, user name and 2 buttons below appears to add and remove admin from server. 

You should see all active CSMM server admins in column to the right

**Warning: this operation is NOT granting player "admin" priveleges on server, only allows to use CSMM system to manage it. For example, grant admin access to himslelf **

