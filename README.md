# Web2cast

Node based command line tool to cast a webpage to a Chromecast when it's idle. 
This tool requires 2 things:

- `catt` installed and available to the user running this script
- `cast-web-api` installed, running and accessible

`catt` in turn uses the `DashCast` Chromecast app: http://stestagg.github.io/dashcast/

## catt
Check https://github.com/skorokithakis/catt for install instructions

## cast-web-api
Check https://github.com/vervallsweg/cast-web-api for install instructions

## Usage
```
Usage: web2cast [options]

Options:
  -V, --version              output the version number
  -a, --api [string]         ip:port of the cast-web-api (default: false)
  -c, --chromecast [string]  the name of the target device (default: false)
  -u, --url [string]         the URL to cast (default: false)
  -t, --time [int]           interval in seconds to test if the Chromecast (default: 5)
  -b, --bin [string]         absolute path to catt binary (default: "catt")
  -h, --help                 output usage information

```

## Examples

```
web2cast 
        --chromecast YourChromecastName 
        --url http://www.google.com 
        --time 5 
        --bin /opt/catt/catt 
        --api 127.0.0.1:3000
```

This example will query the `cast-web-api` device endpoint at `http://127.0.0.1:3000` every 5 seconds to see if `YourChromecastName` is idle.<br>
If it is, it will cast google.com to the Chromecast called `YourChromecastName` using the `catt` binary in `/opt/catt/catt`.<br>


## Roadmap
- Extract what we need from the `cast-web-api` and use it in this package so we're not dependent on `cast-web-api`.
- Extract what we need from `catt` for casting `DashCast` with a specific URL and implement it into this package.
