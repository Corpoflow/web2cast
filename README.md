# Web2cast

Node based command line tool to cast a webpage to a Chromecast when it's idle. 
This tool REQUIRES you to have `catt` installed and available to the user running this script (PATH).

## catt

Check https://github.com/skorokithakis/catt for install instructions


## Usage

- web2cast --chromecast YourChromecastName --url http://www.google.com --time 5
Will check chromecast YourChromeCast every 5 seconds to see if it's idle. If it is, it will cast http://www.google.com using `DashCast`.
