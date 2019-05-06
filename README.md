# clipboard-sync
 
## Description

It's a small client-server script which allows to synchronise clipboard
  between two computers. It's very useful when you have a virtual machine
  like VirtualBox without installed guest additions (Mac OS X guest for example).
  It works on Linux, Mac OS X and Windows.

## Installation (both client and server)

1. Install [Node.js](http://nodejs.org)

    * on OSX use [homebrew](http://brew.sh) `brew install node`
    * on Windows use [chocolatey](https://chocolatey.org/) `choco install nodejs`
    * on Debian based linux use `apt-get install nodejs npm`
    
2. Install forever package:

    npm install forever -g

3. Install clipboard-sync with [npm](https://npmjs.org/package/clipboard-sync):

    npm install -g clipboard-sync

## Usage

Starting a server using one of the following ways:

    clipboard-sync                  # Using default settings, bind to 0.0.0.0:1077
    clipboard-sync 192.168.1.2      # Using default port 1077
    clipboard-sync 192.168.1.2:1077 # Full syntax


Starting a client using one of the following ways:

    clipboard-sync -c                  # Using default settings, connect to 10.0.2.2:1077
    clipboard-sync -c 192.168.1.2      # Using default port 1077
    clipboard-sync -c 192.168.1.2:1077 # Full syntax
    
Setting refresh interval in milliseconds (how often script will spy on
clipboard changes), can be set in both client and server mode:

    clipboard-sync -c -i 100

## License

Licensed under MIT.
