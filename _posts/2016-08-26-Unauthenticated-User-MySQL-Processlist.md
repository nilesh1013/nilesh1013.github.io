---
layout: post
title: Unauthenticated User in MySQL ?
author: Nilesh Sharma
---
Yesterday I have seen in MySQL processlist some unauthenticated user was showing. I was wondering what is this ? So I did some research and found out some interesting thing about MySQL config.

##  Unauthenticated User in MySQL ProcessList
-----

| 305168 | debian               | 127.0.0.1:39834 | NULL      | Connect |  NULL | Reading from net   | NULL             |    0.000 |
| 305169 | debian               | 127.0.0.1:39114 | NULL      | Connect |  NULL | Reading from net   | NULL             |    0.000 |
| 305170 | unauthenticated user | 127.0.0.1:39842 | NULL      | Connect |  NULL | Reading from net   | NULL             |    0.000 |
| 305171 | unauthenticated user | 127.0.0.1:39860 | NULL      | Connect |  NULL | Reading from net   | NULL             |    0.000 |
| 305172 | unauthenticated user | 127.0.0.1:39876 | NULL      | Connect |  NULL | Reading from net   | NULL             |    0.000 |
+--------+----------------------+-----------------------+-----------+---------+-------+--------------------+------------------+----------+


Apparently what happened that a connection with "unauthenticated user" in the User column has initiated a connection but hasn't sent his credentials yet, so the server doesn't know who exactly is connecting.

If such connections only showed up in the list when they were authenticated, it could potentially run the server out of available sockets and you wouldn't even know why.

At most of the times, such connections get stuck because of DNS Resolve not happening accordingly or it's taking so much time.

Actually by default MySQL checks for user hostnames using DNS check. Now there are some scenarios 

You never know when you hosting provider DNS goes down and MySQL will silently stop letting users in.
Most worst thing is that you don't even find out what the problem is while diagnosing the issue ?

Another scenerio which many happen that DNS goes slow, now because of all this connections will get slow
as well eventually.

Also another problem is that if your servers are externally available than anybody can do DDOS attacks on your MySQL instance very easily.

So if you don't need to restrict MySQL users based on hostnames than disable this feature of MySQL's authentication system by adding **"skip_name_resolve"** in my.cnf config file of MySQL.
