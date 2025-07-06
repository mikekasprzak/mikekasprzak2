+++
date = '2018-12-01'
draft = false
title = 'ENet with IPv6 support (and Linux/BSD events)'
type = 'project'
categories = ['project', 'tech', 'featured']
roles = ['coder']
technologies = ['c', 'c++', 'networking', 'porting']
platforms = ['apple', 'iphone', 'ipad', 'macos', 'windows', 'linux', 'bsd', 'nintendo', 'switch', 'playstation']
+++
[ENet](https://github.com/lsalzman/enet) is a popular (nearly) 20 year old C library that provides both reliable (i.e. TCP) and unreliable network communication over UDP. ENet only supports IPv4, so I rewrote it to supprt IPv6.

ENet uses [`select`](https://en.wikipedia.org/wiki/Select_(Unix)) and `poll` to respond to system events. Both of these are antiquated (and flawed) ways of handling this, and so I added support for [`epoll`](https://en.wikipedia.org/wiki/Epoll) (Linux) and [`kqueue`](https://en.wikipedia.org/wiki/Kqueue) (BSD/Apple).

Finally, I wrote backends that support both the Nintendo Switch and Sony PlayStation 4's proprietary BSD Socket implementations.

Since then, other IPv6 implementations have appeared, and even the main projcet seems to have recently shown signs of life and merged some fixes. TBD if I decide to release my port publicly or not.

That said, my work on ENet lead to me making `Roaming Procotol`, which is argubaly better anyawy.
