# Transfer files more easily over SSH

`sshget` is quickly hacked Python script for transfering files over SSH when
they have, impossible to type names.

## Dependencies

  * Paramiko: `pip install paramiko`
  * Rsync (more download strategies will come later if I ever come baack here)

## Usage

Isn't this awesome?

```shell
$ sshget username@server Abstract Pattern
Connecting to username@server
Executing: find ~ -not -type d -name '*Abstract*' -name '*Pattern*'

Found 2 files matching your request:
  1: PatternMatcherAbstractObserverInterfaceWithSwissChocolate.java
  2: PatternMatcherAbstractObserverInterfaceWithSwissChocolateImpl.java

Which ones should I download? [1-2] 1

PatternMatcherAbstractObserverInterfaceWithSwissChocolate.java
19646 100%   18.74MB/s    0:00:00 (xfer#1, to-check=0/1)

sent 42 bytes  received 19777 bytes  7927.60 bytes/sec
total size is 19646  speedup is 0.99
```

## Copyright

This (the `sshget` file) is licensed under the do-whatever-the-heck-you-want
license. Do whatever you want!

The `progress.py` and `terminal.py` files are (c) 2009 Nadia Alramli under a
BSD license. I included them for convenience, but they don't belong to me.
