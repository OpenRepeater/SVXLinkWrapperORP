SVXLinkWrapperORP
====================================
Wrapper for SVXLink with customizations for OpenRepeater Project
**Based upon code by Guy Sheffer 4Z7GAI**

Features
--------

* Autoconnect to stations on startup, and keep-alive option
* QSO Echolink logger in sqlite3 and a simple web viewer for it
* Send DTMF preset commands from echolink chat

Requirements
------------
1. OpenRepeater Project pkgs install
2. SVXLink pkgs
3. python
4. python modules: importlib python-sqlite

Install all requirements except SVXLink on Debian
----------------------------------------------------------

::
    
    apt-get install python-sqlite



Quick setup on Debian
------------------------------
::
    
    git clone https://github.com/OpenRepeater/SVXLinkWrapperORP.git
    cd SVXLinkWrapperORP
    python src/SvxLinkWrapper.py
    
    To update remote change: from within folder SVXLinkWrapperORP, type "git pull"


How to configure QSO logger module
-----------------------------------
1. set DATABASE_PATH in modules.EcholinkLoggerModule to the location of EcholinkQsoLog.sqlite
2. Make sure the folder that EcholinkQsoLog.sqlite has read/write permissions, as well as the file
3. If you want to view latest qsos from a browser you can move ``www/EcholinkQsoLog.php`` to a location on your webserver (on Ubuntu / Debian the default path is ``/var/www`` )