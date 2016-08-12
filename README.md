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







**********************************************
 File @ ***/main.py***

package entry point

**********************************************
 File @ ***/makefile_parser/__init__.py***

Modules __init__.py

**********************************************
 File @ ***/makefile_parser/__main__.py***

Main entry


***def menu***: 

The Menu is here
**********************************************

***def main***: 

This is used in the cli and from a couple places
**********************************************
**********************************************
 File @ ***/makefile_parser/modules/__init__.py***

None

**********************************************
 File @ ***/makefile_parser/modules/manager.py***

Created on Jul 28, 2016

@author: iitow


***class Manager***: 

Represents a management singleton
    
**********************************************

***class Makefile***: 

Represents a Makefile
**********************************************

***class Syntax***: 

This class is used to find elements in a makefile
**********************************************

***def __init__***: 

Manager Constructor


**:param options:** argarse obj
**********************************************

***def pprint***: 

Pretty print out makefiles


**:param title:** String
**********************************************

***def _pprint***: 

Private, Pretty print out makefiles


**:param mk_obj:** Object, Makfile

**:param title:** String
**********************************************

***def _walk***: 

performs scan on all files

**:param path:** String

**:param excludes:** List, list of excludes
**********************************************

***def _is_include***: 

Check for includes in given file name

**:param filepath:** String
**********************************************

***def _write***: 

writes json file

**:param data:** Dict
**********************************************

***def main***: 

main entry point of class
**********************************************

***def find_matches***: 

Find matches in a given makefile
**********************************************

***def traverse***: 

Private recursively traverse nested json data

**:param data:** Nested dict/list

**:param key:** String

**:return:** value
**********************************************

***def __init__***: 

Makefile Constructor


**:param base_path:** String

**:param file_ext:** String

**:param options:** Object, argparse
**********************************************

***def _reader***: 

Private, file reader


**:param filepath:** String
**********************************************

***def _parse***: 

Private, add all parsing here
**********************************************

***def __init__***: 

Syntax constructor


**:param raw:** String

**:param filepath:** String

**:param options:** Object, argparse
**********************************************

***def includes_are***: 

Grab includes from makefile regex


**:param raw:** String
**********************************************

***def comments_are***: 

Grab comments from makefile regex


**:param raw:** String
**********************************************

***def _variables_are***: 

Private, Grab all variables from makefile regex


**:param raw:** String
**********************************************

***def variables_are***: 

Grab all variables from makefile, transforms tuples to dict


**:param raw:** String
**********************************************