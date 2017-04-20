# XMPP-Chat-Client Setup and Installation

Here you will find the setup for the XMPP-Chat-Client based on strophe.js and Openfire

## Getting started

### Requirements

You need Openfire working on an ubuntu system. (Note: I tried with openfire_4.0.4. With Version 4.1.1 there were problems with the Openfire Websocket Plugin, i am not sure about latest versions.)


### Openfire konfiguration

In Openfire administration, make the following settings: 
* Serverconfiguration -> ClientConnection -> Plain-text -> Advanced Configuration -> STARTTLS policy -> Disabled
* Serversettings -> Compressionsettings -> Client compression Policies: Not available
* Serversettings -> HTTP Binding -> Script Syntax: Enabled  
* Plugins -> Available Plugins -> Openfire WebSocket Plugin  -> add it (if the plugin is not in pluginlist, it can be manuel downloaded here:
 https://www.igniterealtime.org/projects/openfire/plugins.jsp  and uploaded manually 
* restart openfire

## Project Setup
* move the project files to www folder
* in the script.js change the following variables:

```var server``` is the server is the openfire servername (see openfire administration)

```var BOSH_SERVICE ws://[IP of system]:7070/ws/ ```

* for easier testing you can add standard users in the ``` (document).ready ```
