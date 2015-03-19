## 1.5.0.4 ##

#### _Changes in WebProxy Log_ ####

#### Added: ####
  * <a href='/p/webproxy-log/issues/detail?id=15'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=15'>bug #15</a></a> - Added update checker in Help menu

#### Fixed: ####
  * <a href='/p/webproxy-log/issues/detail?id=17'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=17'>bug #17</a></a> - Menu icons have been updated
  * <a href='/p/webproxy-log/issues/detail?id=18'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=18'>bug #18</a></a> - WebProxy Log starts faster


---



## 1.5.0.3 ##

#### _Changes in WebProxy Log_ ####

#### Fixed: ####
  * <a href='/p/webproxy-log/issues/detail?id=12'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=12'>bug #12</a></a> - buttons displacement
  * <a href='/p/webproxy-log/issues/detail?id=13'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=13'>bug #13</a></a> - program startup - in certain scenarios program hangs on error when checking dates with entries

#### _Changes in WebProxy Log Catcher_ ####

#### Fixed: ####
  * <a href='/p/webproxy-log/issues/detail?id=14'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=14'>bug #14</a></a> - WebProxy Log Catcher could not create initial configuration

---



## 1.5.0.2 ##

#### _Changes in WebProxy Log_ ####

#### Added: ####
  * Czech language (thanks to Alen Bajo)

#### Fixed: ####
  * <a href='/p/webproxy-log/issues/detail?id=10'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=10'>bug #10</a></a> - ‘Delete records’ would ask to delete 0 records
  * <a href='/p/webproxy-log/issues/detail?id=8'><a href='https://code.google.com/p/webproxy-log/issues/detail?id=8'>bug #8</a></a> - saved/not saved message hasn’t been displayed after exporting IP aliases list

#### Updated: ####
  * communication with databse is a bit faster


#### _Changes in WebProxy Log Catcher_ ####
#### Added: ####
  * 'Configure' option to the tray icon
  * Configuration dialog (opens once you click 'Configure')


#### _Changes in Installation_ ####
#### Added: ####
  * ‘Tell us what you think’ at uninstall

---


## 1.5.0.1 ##

#### _Changes in WebProxy Log_ ####

#### Fixed: ####
  * bug where description text in ‘General settings’ dialog wouldn’t fit in Indonesian
  * bug where ‘Internet traffic’ report did not show day separation, but merged two days within same day
  * bug where 'Settings' dialog would've been opened even if WebProxy Log is installed in user mode

#### Updated: ####
  * black frame around flag image in 'Language select' dialog
  * grid list behavior in 'IP aliases' dialog

#### Added: ####
  * 'Online help' and 'Changelog' under menu 'Help'

---



## 1.5.0.0 beta3 ##

#### _Changes in WebProxy Log_ ####

#### Further improved: ####
  * log importing
#### _Changes in installation_ ####

#### Added: ####
  * the option to create startup icon for WebProxy Log Catcher

---



## 1.5.0.0 beta2 ##

#### _Changes in WebProxy Log_ ####

#### Improved: ####
  * log importing

---



## 1.5.0.0 beta1 ##

#### _Changes in package_ ####

#### Added: ####
  * WebProxy Log Catcher - module that captures and stores Mikrotik Web Proxy's messages
  * updated graphics

#### _Changes in WebProxy Log_ ####

#### Added ####
  * /stop command line switch - which causes all WebProxy Log windows to be closed
  * new settings dialog which shows only in admin mode, user mode displays 'select database dialog' only
  * server filter list - added feature that automatically gets clipboard data so you can easily enter new server to the list (Copy shortcut from report)
  * support to automatically split large log files (thanks to G.D.G. Software http://www.gdgsoft.com and their Gsplit)
  * top 10 servers pie-chart
  * top 10 surfers pie-chart
  * delete web page records

#### Fixed ####
  * bug when importing empty log file
  * bug with import and export IP alias list (no 'IP address' and 'Alias' in csv file)
  * bug when Mikrotik logging is configured without prefix or prefix other then ‘logging’

#### Updated ####
  * new and improved importation of a log file
  * delete records dialog

#### _Changes in installation_ ####

#### Added: ####
  * installation languages

#### Updated ####
  * full and user mode options

#### Known issues ####
  * log file format is still not checked for the right format (this could be trouble if you're using custom software to capture logs instead of WebProxy Log Catcher)
  * WebProxy Log Catcher can only run with user logged on, cannot be installed as a service
  * report can only be generated if from and to dates are within same year

---


## 1.0.0.0 beta5 ##

#### Fixed ####
  * if using one of import switches on empty configuration - no source defined error message is displayed
  * fixed "day names" error with non-english languages on report generating (thanks to Pujo)

---



## 1.0.0.0 beta4 ##

#### Added ####
  * support for reading unix-formatted log files (thanks to Pujo)
  * international support for date separators (thanks to Pujo)

---


## 1.0.0.0 beta3 ##

#### Added ####
  * progress when reading dates on main screen (right after startup)
  * command line switches (/i and /import - opens WebProxy log, imports log files, and exits the program silently)
  * option to delete all records for certain user

#### Fixed ####
  * error in case generating report with activated empty filter list
  * bug when creating database when it was unplanned in certain scenarios

#### Know issues ####
  * Will perform with error if you try to use /i or /import switches before first manual log import
  * Unable to read log files larger than 10 MB