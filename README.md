# Redis
Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. It supports data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs, geospatial indexes with radius queries and streams.
![](images/redis_icon.png)

Fun Fact: Redis means 
> "REmote DIctionary Server."
## Contents
+ Installation
+ Before you start
+ Read,Write,Update,Delete

## Installing On Windows
Go to Redis official website https://redis.io/ and Scroll down to Windows section. You will see learn more. Click on it and you will get release page.Download the msi file and install it.
Start the **redis server** and **redis client** from the installation folder.
To check if everything's fine,use `ping` command.

![](images/ping.png)

## Installing On Linux 
Follow this link : https://www.javatpoint.com/redis-installation-on-ubuntu

## Before you start
There's another way to install redix i.e. using the zip file.I won't recommend that because in that case you've to run redis-server each time you start the redis-cli.If you've followed the way I described here,you needn't worry about it.

If you're on a Windows Operating System,try to use **WSL(Windows Subsystem for Linux)**(To enable WSL: https://bit.ly/3gMXyZQ) instead of cmd because WSL provides you with suggestions while writing.

## Write,Read,Update,Delete

You can easily set a value to a key.The command is very simple:

> set key value

To retrieve the value , 

> get key

![](images/read_write.png)
