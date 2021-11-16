# FAV/E
[![License](https://img.shields.io/badge/license-MIT-_red.svg)](https://opensource.org/licenses/MIT) [![Twitter Follow](https://img.shields.io/twitter/follow/un4gi_io?label=%40un4gi_io&style=social)](https://twitter.com/un4gi_io)

<img src="img/fave.png">

FAV/E (Find A Vulnerability/Exposure) utilizes the NIST CVE database search API to search for vulnerabilities and exposures while filtering based on age, keywords, and other parameters.

https://un4gi.io/blog/fave-find-a-vulnerability-exposure

## Usage:

Use the `-h` flag to display available flags
```
$ fave -h
```
| Flag | Description | Example |
|------|-------------|---------|
| `-cwe` | Search for CVEs based on a CWE number. | `fave -cwe 79` |
| `-exact` | Return only items matching the exact keyword(s) specified with -k | `fave -k un4gi -exact` |
| `-fd` | Number of days to filter results (prior to today) | `fave -fd 5` |
| `-fm` | Number of months to filter results (prior to today) | `fave -m 2` | 
| `-fy` | Numer of years to filter results (prior to today) | `fave -y 3` |
| `-k` | Search for CVEs based on a keyword (or words) | `fave -k "Microsoft Windows 10" -exact` |
| `-s` | Search for CVEs based on the CVSS V3 severity. | `fave -cvss CRITICAL` |

Example usage:
```
$ fave -k "Windows 10" -exact -cvss CRITICAL -fy 2
```

## Installation
To install, use:
```
go install github.com/un4gi/fave@latest
```
