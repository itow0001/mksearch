### Introduction
```
    Do you need to easily relate a C source code change check-in to a binary?
    This tool recursively grabs all the Makefiles parses each file and if a value
    is found produces a json file containing the relevant info.
    Currently supports:
    - Variables
    - Includes
    - Comments
    The goal is to fully support GNU make standards:
    https://www.gnu.org/software/make/manual/html_node/Quick-Reference.html
    This tool was designed to support Freebsd but should work for all systems 
    using GNU make
```
###Package Create/Install###
```
 python setup.py install
 or.
 pip install mksearch
```

****************************
###CLI Info ###
```
mksearch

optional arguments:
  -h, --help  show this help message and exit
  -j          execute the values
  -e          execute the values
  -d          execute the values
  -p PATH     base path to scan files
  -i INCLUDE  include files or directories
  -s SEARCH   search for key words returns makefile output
  --version   show program's version number and exit
```
### Api Doc Reference ###






