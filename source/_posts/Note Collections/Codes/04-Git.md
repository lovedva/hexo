---
title: Git
---

## Git
### Github Desktop 设置代理
https://stackoverflow.com/questions/16153450/github-windows-client-behind-proxy  

Add these entried to your '.gitconfig' file in your user directory (go to %USERPROFILE%):

[http]
    proxy = http://<proxy address>:<proxy port>

[https]
    proxy = https://<proxy address>:<proxy port>
And if you don't want to store your password in plaintext, I would use a local proxy forwarder like CNTLM which allows you to direct all traffic through it and can store the passwords hashed.

### 注释
在前面加上 #

### 清除所有历史记录（Pack文件过大）
https://www.cnblogs.com/gaowengang/p/10955871.html
