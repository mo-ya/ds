# ds - Directories usage Summary tool

## Overview

**ds** displays the number of files and the file space usage in directories in the target directory.

(This tool uses **find** and **du** commands)

## Usage

    $ ds [dir]

## Example

    $ cd /var
    $ ds
    
    91      90688   89M     cache
    6565    83396   82M     lib
    15      12      12K     lock
    106     19592   20M     log
    11      144     144K    run
    15      136     136K    spool
    46      324620  318M    tmp
    245     1176    1.2M    www
    0       4       4.0K    yp

Output is number of files, file space usage (kbyte), file space usage (human readable format), directory. 

## Tips

### Sort by the number of files

    $ ds | sort -n
    
    11      144     144K    run
    15      12      12K     lock
    15      136     136K    spool
    46      324620  318M    tmp
    91      90688   89M     cache
    106     19592   20M     log
    245     1176    1.2M    www
    6565    83396   82M     lib

### Sort by the file space usage

    $ ds | sort -k 2n
    
    15      12      12K     lock
    15      136     136K    spool
    11      144     144K    run
    245     1176    1.2M    www
    106     19592   20M     log
    6565    83396   82M     lib
    91      90688   89M     cache
    46      324620  318M    tmp
