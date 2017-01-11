# map-host
This repository contains a script to easily set map a "host" name to a "host" ip in  ```/etc/hosts``` and ```~/.ssh/config``` and can also place your ```~/.ssh/id_rsa.pub``` onto the "host" machine in one simple command:

```
map-host.sh -k -a sshHost -n host.kroger.com -i 192.168.0.1
```

This is useful for creating VMs and automatically setting up a "Poor Man's" DNS, with the added benefit of placing RSA keys on the "host" for quick access to the host.


## install

### install dependencies
[stormssh](http://stormssh.readthedocs.io/en/master/)
http://stormssh.readthedocs.io/en/master/installing.html

#### Install GNU core utilities
(those that come with OS X are outdated).
Don’t forget to add ```$(brew --prefix coreutils)/libexec/gnubin``` to ```$PATH```.

```
brew install coreutils
```

### clone this project
```bash
git clone ...
```

## use
### script
map-host.sh -h
### options
* -a | alias -- ssh host alias
* -c | clean/remove "host" map
* -d | dry run
* -f | "hosts" file
* -h | help
* -i | IP to map the "host" name to
* -k | place id_rsa.pub key on "host"
* -n | "host" name to map the IP to
* -u | 'user' name for "host"
* -s | silent

### run
```bash
./map-host -a mickey -n mickey.kroger.com -i 127.0.0.1
```

---
