# Rapsberry Pi setup

### Setup WiFi (if needed)

https://gist.github.com/victorblasco/31c6e45c73d8e3d87f460a92913c6ade

### Autologin with root

https://gist.github.com/victorblasco/64192555faa0f8dbf4fb867af2997128

### Clone repo

```
$ apt-get update
$ apt-get install git
$ mkdir Code
$ cd Code
$ git clone https://github.com/victorblasco/instabot.py.git
```

### Install dependencies

```
$ apt-get install vim
$ apt-get install python3-pip
$ pip3 install requests
$ pip3 install fake-useragent
```

### Copy .py files inside /root/Code/instabot.py folder

### Add script/s

```
$ cd
$ vim account1.sh
#!/bin/bash

rm /root/Code/instabot.py/account1.log

while true
do
  python3 /root/Code/instabot.py/account1.py &> /root/Code/instabot.py/account1.log
done
```

### Edit .bashrc (if you want autoboot)

```
sleep 3
bash /root/account1.sh &

sleep3
bash /root/account2.sh
```