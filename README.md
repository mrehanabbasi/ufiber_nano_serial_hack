# UFiber Nano G - Serial Hack
https://community.ubnt.com/t5/UFiber-GPON/UFiber-Nano-G-GPON-Huawei-HG8245-Configuration/m-p/2139059#M511



## Dependencies
pip3 install paramiko scp



## Usage
Сhange your serial number on UFiber Nano G via ssh
```sh
./ubi_serial_hack.py -r 192.168.1.1 -p 22 --serial 48:57:54:43:30:30:30:30
```

Change your serial and MAC
```sh
./ubi_serial_hack.py -r 192.168.1.1 -p 22 --serial 48:57:54:43:30:30:30:30 --mac 11:22:33:44:55:66
```

Manual method. Put the mtdblock3.BIN in the script folder and run with --nossh flag.
```sh
./ubi_serial_hack.py --nossh --serial 48:57:54:43:30:30:30:30
```

Ignoring abnormal termination with unsupported boards.
```sh
./ubi_serial_hack.py --insecure --serial 48:57:54:43:30:30:30:30
```

Read only from filepath
```sh
./ubi_serial_hack.py -f mtdblock3.BIN
```



## Tested
Firmware versions: v2.1.1 and v4.1.0



## Used links
https://web.archive.org/web/20190214022357/https://blog.onedefence.com/changing-the-gpon-serial-on-the-ubiquiti-ufiber-nano-g-part-two/

https://github.com/palmerc/AESCrypt2

https://github.com/dylangerdaly/UFiber-Nano-G-Playpen
