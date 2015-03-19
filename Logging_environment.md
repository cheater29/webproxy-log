### You'll need ###
  * access to your Mikrotik
  * WebProxy Log
  * WebProxy Log Catcher

### Mikrotik configuration ###

First of all, if you are not using manual client-side proxy configuration, you'll need to set up transparent proxy on your Mikrotik. You can learn [here](http://wiki.mikrotik.com/wiki/How_to_make_transparent_web_proxy) more about it.

When you're sure that clients will make traffic through proxy, you'll have to set up logging in your Mikrotik. Either by using the console or [WinBox](http://wiki.mikrotik.com/wiki/Manual:Winbox):

  * go to 'System/Logging/Actions'
  * add new Action with following details:
![http://lh6.ggpht.com/_glRSY7BdJS4/TM3Qb_A9WmI/AAAAAAAAAjM/7u7QFWsPz9g/s800/action.png](http://lh6.ggpht.com/_glRSY7BdJS4/TM3Qb_A9WmI/AAAAAAAAAjM/7u7QFWsPz9g/s800/action.png)
    * **Name**: WebProxyLog
    * **Type**: remote
    * **Remote Address**: _enter  here the IP address of the remote computer where WebProxy Log Catcher will be running_
    * **Remote Port**: _enter here UDP port of the computer where WebProxy Log Catcher will be listening from the remote computer - usually for syslog 514_

  * now go to 'System/Logging/Rules'
  * add new rule with following details:
![http://lh6.ggpht.com/_glRSY7BdJS4/TM3QcF50nzI/AAAAAAAAAjU/Sjm87KkB1ws/s800/rule.png](http://lh6.ggpht.com/_glRSY7BdJS4/TM3QcF50nzI/AAAAAAAAAjU/Sjm87KkB1ws/s800/rule.png)
    * **Topics**: web-proxy, !debug
    * **Prefix**: proxy
    * **Action**: WebProxyLog _(or whatever name you gave to the action)_

**Make sure that UDP port you specified for remote logging is open both in [Mikrotik's firewall](http://wiki.mikrotik.com/wiki/Manual:IP/Firewall/Filter) and in [remote computer's firewall](http://windows.microsoft.com/en-us/windows7/Open-a-port-in-Windows-Firewall)!**

### WebProxy Log Catcher configuration ###
  * [download](http://code.google.com/p/webproxy-log/downloads/list) and install WebProxy Log package
  * when you run WebProxy Log Catcher for the first time, the settings dialog will pop up (or you can select 'Cofigure' option by right-clicking WebProxy Log Catcher's icon in system tray)
![http://lh5.ggpht.com/_glRSY7BdJS4/TM3QcMN37OI/AAAAAAAAAjQ/q9qW5zOVj8w/s800/config.png](http://lh5.ggpht.com/_glRSY7BdJS4/TM3QcMN37OI/AAAAAAAAAjQ/q9qW5zOVj8w/s800/config.png)
  * configure IP address, UDP port and logs locations (where IP addres and UDP port are located on compter where WebProxy Log Catcher is running - the same IP address and UDP port you specified for the remote computer in you Mikrotik)
  * once you apply configuration, you are ready to start!

That's it!