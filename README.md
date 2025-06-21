#  check-file-exists

A Nagios check to monitor the presence of absence of a file

## Requirements

Python3.2 or newer

## Usage

```
user@host$ ./check-file-exists --help
usage: check-file-exists [-h] -f PATH [--present | --absent]
                         [--warning | --critical]

Check for the (non) existence of a file

optional arguments:
  -h, --help            show this help message and exit
  -f PATH, --file PATH  file to check
  --present             return OK if file exists, and WARNING or CRITICAL if
                        file does not exist
  --absent              return OK if file does not exist, and WARNING or
                        CRITICAL if it exists
  --warning, -w         Upon failure, return WARNING
  --critical, -c        Upon failure, return CRITICAL

To check for pending reboots on Debian/Ubuntu:

check-file-exists -f /var/run/reboot-required --absent
```
