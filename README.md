#  check-file-exists

A Nagios check to monitor the presence of absence of a file

## Requirements

Python3 with the `argparse`, `sys`, `os`, and `textwrap` modules

## Usage

```
user@host$ ./check-file-exists --help
usage: check-file-exists [-h] -f PATH [--present | --absent]

Check for the (non) existence of a file

optional arguments:
  -h, --help            show this help message and exit
  -f PATH, --file PATH  file to check
  --present             return OK if file exists, and CRITICAL if file does
                        not exist
  --absent              return OK if file does not exist, and CRITICAL if it
                        exists

To check for pending reboots on Debian/Ubuntu:  

check-file-exists -f /var/run/reboot-required --absent  
```
