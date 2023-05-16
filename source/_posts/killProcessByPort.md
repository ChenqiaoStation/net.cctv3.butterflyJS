---
title: Windows macOS Linux 端口被占用解决方案汇总
date: 2023-05-16 16:59:54
tags: macOS
---

# macOS

## lsof -i:xxxx

```bsah
lsof -i:4000
COMMAND     PID        USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
Google     3874 net.cctv3.i   25u  IPv6 0x25405a5d3cfb6c93      0t0  TCP localhost:63955->localhost:terabase (ESTABLISHED)
node      62320 net.cctv3.i   23u  IPv6 0x25405a5d3cfb7a93      0t0  TCP *:terabase (LISTEN)
node      62320 net.cctv3.i   24u  IPv6 0x25405a5d3cfad793      0t0  TCP localhost:terabase->localhost:63955 (ESTABLISHED)
```

## kill -9 xxxx

```bash
kill -9 62320
```
