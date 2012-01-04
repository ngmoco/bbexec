BBEXEC .1
============

## Usage
bbexec usage: bbexec.sh [-hv] -d path/to/executable [-p /path/to/pid-file] [-l /path/to/log] [-a "quoted space delimeted list of params"]

This script will daemonize (background) an executable and then pass it on.
NOTE: if the -p(pid,pid-file) parameter is not set this script will attempt
to write one out to /var/run/daemon-basename if run as root and 
/usr/local/var/run/daemon-name if not run as root.

OPTIONS:
   -h       Show this message
   -d       The executable to daemonize (background)
   -p       The pid file to output with the new daemons pid
   -l       The location to log stdout and stderr to
   -a       The quoted space delimeted list of arguments to pass through to the executable
   -v       Verbose

```
$ ./bbexec.sh -d /usr/local/bin/node -p /var/run/node -l /var/log/node -a "app.js --debug-brk"
```
