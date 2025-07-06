+++
date = '2018-12-01'
draft = false
title = 'ENet with IPv6 support (and Linux/BSD events)'
type = 'project'
categories = ['project', 'middleware', 'featured']
roles = ['coder']
technologies = ['c', 'c++', 'networking', 'porting']
platforms = ['apple', 'iphone', 'ipad', 'macos', 'windows', 'linux', 'bsd', 'nintendo', 'switch', 'playstation']
+++
[ENet](https://github.com/lsalzman/enet) is a popular (nearly) 20 year old C library that provides "reliable transport over UDP". In other words, you get the benefits of TCP over UDP. At the time of this writing, ENet only officially supported IPv4, so I rewrote it to supprt both IPv4 and IPv6.

ENet uses [`select`](https://en.wikipedia.org/wiki/Select_(Unix)) and `poll` to respond to network events. While this does work, `select` can't handle more than 1024 connections (file descriptors), and `poll` performance gets noticibly worse beyond 1024, both of which are undesirable for servers. So in additional IPv6 support, I added support for [`epoll`](https://en.wikipedia.org/wiki/Epoll) (Linux) and [`kqueue`](https://en.wikipedia.org/wiki/Kqueue) (BSD/Apple) event polling methods. Development was done on Ubuntu Linux, FreeBSD, and Windows.

Finally, I added support for both the Nintendo Switch and Sony PlayStation 4's proprietary [BSD Socket](https://en.wikipedia.org/wiki/Berkeley_sockets) implementations. Because of NDA's ossociated with these devices, my code is not available publicly.

Since then, other IPv6 implementations have appeared, and even the main projcet seems to have shown signs of life, but no official IPv6 support. At the time of this writing, there's no concensus on which is the preferrable implementation to support.

My work on ENet lead to my work on `Roaming Procotol`.
