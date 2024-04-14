
#### IT-23 DNS Presentation Server

##### import and start container with

```
$ docker import export.zip bind9-it23:latest
$ docker run -d --name bind9-it23 -p 53:53 -p 53:53/udp bind9-it23:latest
```

##### Lösung

```
$ nslookup -q=TxT start.it23.local 127.0.0.1
-> start.it23.local        text = "maybealittleriddle"
```
```
$ nslookup -q=txt maybealittleriddle.it23.local 127.0.0.1
-> What is always in front of you but can’t be seen?
```
```
$ nslookup -q=txt future.it23.local 127.0.0.1
-> future.it23.local       text = "Contact the Admin"
```
