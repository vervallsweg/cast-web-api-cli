# cast-web-api-cli
[![npm version](https://badge.fury.io/js/cast-web-api-desktop.svg)](https://badge.fury.io/js/cast-web-api-desktop)
[![Dependency Status](https://img.shields.io/david/vervallsweg/cast-web-api-desktop.svg)](https://david-dm.org/vervallsweg/cast-web-api-desktop)
[![npm](https://img.shields.io/npm/dm/cast-web-api-desktop.svg?maxAge=2592000)]()

CLI manager for [cast-web-api](https://github.com/vervallsweg/cast-web-api).

## Installation
	$ npm install cast-web-api-cli -g

You might run into [issues](https://github.com/vervallsweg/cast-web-api/issues/79) with the optional Google-Assistant integration.

## First steps
    $ cast-web-api-cli start

The server runs on your network ip:3000 by default. On error it defaults to 127.0.0.1. Adjustable via:

	$ cast-web-api-cli start -H 192.168.0.11 -p 8080

## Usage

    $ cast-web-api-cli -h
    
       USAGE
    
         cast-web-api-cli <command> [options]
    
       COMMANDS
    
         start               Start cast-web-api as daemon           
         stop                Stop the cast-web-api daemon           
         status              Check status of the cast-web-api daemon
         startup             Start the cast-web-api daemon on system startup      
         unstartup           Remove the cast-web-api daemon start on system startup
         fix-perm            Changes permissions on /config to current user
         help <command>      Display help for a specific command    
    
       GLOBAL OPTIONS
    
         -h, --help         Display help                                      
         -V, --version      Display version

### Parameters

Every changed parameter will be saved in `/config/config.json`. The location will be changed in the next release.

### Run on system startup

Enable start cast-web-api on startup.

    $ cast-web-api-cli startup
    
Disable start cast-web-api on startup.

    $ cast-web-api-cli unstartup
