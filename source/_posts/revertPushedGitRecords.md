---
title: Git 撤销已经 Push 的代码
date: 2023-05-16 17:15:58
tags: Git
cover: https://net-cctv3.oss-cn-qingdao.aliyuncs.com/net.cctv3.butterflyJS/Snipaste_2023-05-16_17-48-10.jpg
---

## git log --pretty=oneline

```git
(base) ➜  net.cctv3.butterflyJS git:(main) ✗ git log --pretty=oneline

e63ac1bfa3c32f1a87d1ec5c027a4d036c83ddb1 (HEAD -> main, origin/main, origin/HEAD) 🐛 测试一次错误的 Push -_-||
a357ef58618fcbb23d685aa1578764b04f1cfc2c 🐛 测试一次正确的Push -_-||
dbbb5199b21b07f5f31c88b9864a6493c9703356 🆕 Windows macOS Linux 端口被占用解决方案汇总
e675c3c4cd6f380615642f140028e95bdde80be5 🦋 _config.butterfly.yml 初步配置 -_-||
27b22bcf980f7d4c959bfeb10decd0a2133685ee 🦋 Hello `hexo-theme-butterfly`.
261d700bc68a1ac7832a5a4db7dba085f358c579 🔗 A fast, simple & powerful blog framework, powered by Node.js.
ef68d4e29c18f3a813d001ef5ae8a6b66fb8aecb Initial commit
```

## git reset

```git
(base) ➜  net.cctv3.butterflyJS git:(main) ✗ git reset --soft dbbb5199b21b07f5f31c88b9864a6493c9703356
```

## git push origin master --force

```git
(base) ➜  net.cctv3.butterflyJS git:(main) ✗ git push origin main --force

Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:ChenqiaoStation/net.cctv3.butterflyJS.git
 + c9d8276...dbbb519 main -> main (forced update)
```

![](https://net-cctv3.oss-cn-qingdao.aliyuncs.com/net.cctv3.butterflyJS/Snipaste_2023-05-16_17-48-10.jpg)

![](https://net-cctv3.oss-cn-qingdao.aliyuncs.com/net.cctv3.butterflyJS/Snipaste_2023-05-16_17-49-15.jpg)
