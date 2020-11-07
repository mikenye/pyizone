# pyizone

This python module aims to implement query and control of WiFi-enabled iZone 310 and compatible family of climate control devices.

## Installing pre-requisites

Clone the repository, change into the directory and run `pip install -r requirements.txt`.

It will require python3, and has been tested with version 3.5 and later.

## Using as a command line tool

You can import this module to use it as a command line tool. For example:

### View help ###

```
$ python3 -m pyizone
usage: izone [-h] [--verbose] {discover,get,set} ...

Control a control-bridge equipped iZone airconditioning system

optional arguments:
  -h, --help          show this help message and exit
  --verbose, -v

Available subcommands:
  {discover,get,set}
```

### Discover devices ###

```
$ python3 -m pyizone discover
Found 1 iZone Controls-Bridge:
  Device ID: 000000XXX (at: xxx.xxx.xxx.xxx:xxxxx)
Run 'export IZONE_DEVICE=xxx.xxx.xxx.xxx' to automatically target this controls-bridge for all future izone commands.
```

```
$ export IZONE_DEVICE=xxx.xxx.xxx.xxx
```

### Querying settings ###

```
$ python3 -m pyizone get fan
xxx.xxx.xxx.xxx: System fan is: low
```

```
$ python3 -m pyizone get mode
xxx.xxx.xxx.xxx: System mode is: vent
```

### Setting settings ###

```
$ python3 -m pyizone set power on
xxx.xxx.xxx.xxx: System power is: on
```

```
$ python3 -m pyizone set mode vent
xxx.xxx.xxx.xxx: System mode is: vent
```

```
$ python3 -m pyizone set fan low
xxx.xxx.xxx.xxx: System fan is: low
```
