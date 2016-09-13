# Leetcode-crawler
A simple python crawler/parser for downloading accepted codes from https://leetcode.com

## Package dependencies
1. BeautifulSoup

`pip install beautifulsoup4`

2. requests

`pip install requests`

## Compatibility
Work under python2.7 or later.

For platforms, it works on both Mac OS X and Linux (Debian), not sure if it behaves well on Windows (there're some codes deal with directories and files, i have no idea about the python package's compatibilities with Windows)

## Usage
- `git clone` this repository
- Install all the necessary python packages
- Open source file `lc-crawler.py`, change the `NAME` and `PASSWORD` variables to your own account of LeetCode
- Execute `lc-crawler.py`

The script will try to sign into your account based on the info you supplied, iterate through all the problems, find the `Accepted` submissions, download it (only one will be downloaded if there're more than one `Accepted` submissions). All the source code files will be gathered into a directory named `Leetcode-archive` (in current working directory) by default, you chan modify it in the `lc-crawler.py` too, of course.

Performance bottleneck of this script should be network, it takes several minutes (yes, i'm in China) to finish all the round, guess it'll be several times faster if you got a great network.

## TODO
Born with a lot parsing work, the script is vulnerable, any details they bring to the website(https://leetcode.com) can result in a crash/not work. If you found some bugs, please add to [Issues](https://github.com/b1ns4oi/Leetcode-crawler/issues)
