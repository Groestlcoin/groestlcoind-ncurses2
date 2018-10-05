# groestlcoind-ncurses2 v0.3.1

Python ncurses front-end for groestlcoind. Uses the JSON-RPC API.

## Dependencies

* Developed with python 3.6.2, Groestlcoin Core 2.16.3
* PyPi packages: aiohttp and async-timeout (see requirements.txt)

## Features

* Updating monitor mode showing groestlcoind's status, including:
* Current block information: hash, height, fees, timestamp, age, diff, ...
* Basic block explorer with fast seeking, no external DB required
* Basic transaction viewer with fast seeking, best with -txindex=1
* Ability to query blocks by hash, height; transactions by txid
* Wallet transaction and balance viewer
* Charting network monitor
* Peer/connection information
* Basic debug console functionality

## Installation and usage

```
git clone https://github.com/groestlcoin/groestlcoind-ncurses2
```

```
pip3 install -r groestlcoind-ncurses2/requirements.txt
```
or, on Arch Linux:
```
pacman -S python-aiohttp python-async-timeout
```

```
cd groestlcoind-ncurses2
python3 main.py
```

groestlcoind-ncurses2 will automatically use the cookie file available in
~/.groestlcoin/, or the RPC settings in ~/.groestlcoin/groestlcoin.conf. To use a different
datadir, specify the --datadir flag:

```
python3 main.py --datadir /some/path/to/your/datadir
```

This is an early development release and a complete rewrite of the original
groestlcoind-ncurses. Expect the unexpected.

Feedback
--------

Please report any problems using the Github issue tracker. Pull requests are
also welcomed.
