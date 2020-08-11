# Redis
Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. It supports data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs, geospatial indexes with radius queries and streams.
![](images/redis_icon.png)

Fun Fact: Redis means 
> "REmote DIctionary Server."
## Contents
+ **Installation**
+ **Before you start**
+ **Read,Write,Update,Delete**
+ **Setting Time Limit on Keys**
+ **MSET,INCR,DECR**
+ **Hashes**
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

We can update the value of a key

> set key new_value

![](images/update.png)

And to delete a key

> del key

![](images/delete.png)

**Notice something curious**: We did not have to put quotation marks around a single string value we wanted to store.Both `set name afnan` and `set name "afnan"`are same in redis.Even we can wrap up both key and value by quotation or not,no problem with it.

But if we use multiple strings, we must use quotation i.e. `set "first name" afnan` or `set name "sihat afnan"`.Otherwise it will show error.

## Setting Time Limit on Keys
We can set a time limit to keys.it means that the key will be destroyed after a certain period of time.To set a time limit to an already declared key,

> EXPIRE key seconds

And to check how many seconds it has before being destroyed,

> TTL key

![](images/expire.png)

Or we can set the time while creating the key.

>  set key value [EX seconds]

Or there's another command called **SETEX**

> SETEX key seconds value 

If we want to use miliseconds,we can use **PSETEX**

> PSETEX key milliseconds value  

## MSET,INCR,DECR
using `MSET` , we can declare multiple keys in a same line.`INCR` and `DECR` are used to incrememnt and decrement a number.

![]images/incr.png)

We can increment or decrement by a fised value

![](images/incrby.png)

## Hashes

In Redis, a Hash is a data structure that maps a string key with field-value pairs. Thus, Hashes are useful to represent objects. They key is the name of the Hash and the value represents a sequence of field-name field-value entries. We could describe a computer object as follows:

**computer name "MacBook Pro" year 2015 disk 512 ram 16**

We can use `HSET` command to create hashes and hget for extracting the key or values.If we want to declare all fields in one line,we've to use `HMSET`.Look at the following image

![](images/hset.png)

Also,we can increment/decrement the value of fields

![](images/hincrby.png)


