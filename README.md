# TinyTemp

A very simple file template engine to easily generate configuration files. It has literally 11 lines of code.

## Usage

Suppose you have a file called `service.conf` with the following content:

	${from}:80 {
    	proxy / ${to}:80
	}

After running:

	tinytemp -f service.conf -d '{ "from": "source.com", "to": "destination.com" }'

You get:

	source.com:80 {
    	proxy / destination.com:80
	}

You can check [here](https://docs.python.org/2.4/lib/node109.html) the full reference of the python Template class.

## Dependencies

It only uses python and its standard library so any python interpreter will do.

## Installation

If you want to have it on your system just run (you may need elevated privileges for this):

	curl -L https://github.com/dvddarias/tinytemp/raw/master/tinytemp > /usr/local/bin/tinytemp
	chmod +x /usr/local/bin/tinytemp





