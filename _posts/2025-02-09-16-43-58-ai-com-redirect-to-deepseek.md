---
title: 全球人类访问deepseek可以少敲几个字符了
tags:
- 个人成长
categories:
- 杂谈
---



今天用 ai.com 访问chatgpt发现被重定向到了 chat.deepseek.com , 开始我还以为是局域网有人整活儿，搞了DNS污染，后面在新加坡服务器检测了一下，发现真的是 ai.com 被重定向到了 chat.deepseek.com ！

检测命令

```
curl -I -L https://ai.com
```

检测结果

```
~# curl -I -L https://ai.com
HTTP/2 302 
date: Sun, 09 Feb 2025 08:45:01 GMT
content-type: text/html
content-length: 143
location: https://chat.deepseek.com/
cache-control: private, max-age=0, no-store, no-cache, must-revalidate, post-check=0, pre-check=0
expires: Thu, 01 Jan 1970 00:00:01 GMT
report-to: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v4?s=D6f1H%2BrCAV8gvhaa3J1WKma2BJ1qGRwmdMH9b4UulIpbjn5SPa54jtW5ZLOwDD2MCWKU4SaEhK1LGSMC1xw1SVY7Krk6dB60P8xGrVP7eTjs2t9R5QwO%2FoE%3D"}],"group":"cf-nel","max_age":604800}
nel: {"success_fraction":0,"report_to":"cf-nel","max_age":604800}
server: cloudflare
cf-ray: 90f294b5bccafd07-SIN
alt-svc: h3=":443"; ma=86400
server-timing: cfL4;desc="?proto=TCP&rtt=1297&min_rtt=1269&rtt_var=283&sent=7&recv=12&lost=0&retrans=0&sent_bytes=3393&recv_bytes=818&delivery_rate=2229407&cwnd=227&unsent_bytes=0&cid=af4d25d8ce0ef2ff&ts=13&x=0"

HTTP/2 403 
date: Sun, 09 Feb 2025 08:45:01 GMT
content-type: text/html; charset=UTF-8
content-length: 7614
accept-ch: Sec-CH-UA-Bitness, Sec-CH-UA-Arch, Sec-CH-UA-Full-Version, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA-Platform-Version, Sec-CH-UA-Full-Version-List, Sec-CH-UA-Platform, Sec-CH-UA, UA-Bitness, UA-Arch, UA-Full-Version, UA-Mobile, UA-Model, UA-Platform-Version, UA-Platform, UA
critical-ch: Sec-CH-UA-Bitness, Sec-CH-UA-Arch, Sec-CH-UA-Full-Version, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA-Platform-Version, Sec-CH-UA-Full-Version-List, Sec-CH-UA-Platform, Sec-CH-UA, UA-Bitness, UA-Arch, UA-Full-Version, UA-Mobile, UA-Model, UA-Platform-Version, UA-Platform, UA
cross-origin-embedder-policy: require-corp
cross-origin-opener-policy: same-origin
cross-origin-resource-policy: same-origin
origin-agent-cluster: ?1
permissions-policy: accelerometer=(),autoplay=(),browsing-topics=(),camera=(),clipboard-read=(),clipboard-write=(),geolocation=(),gyroscope=(),hid=(),interest-cohort=(),magnetometer=(),microphone=(),payment=(),publickey-credentials-get=(),screen-wake-lock=(),serial=(),sync-xhr=(),usb=()
referrer-policy: same-origin
x-content-options: nosniff
x-frame-options: SAMEORIGIN
cf-mitigated: challenge
cf-chl-out: arq0/t4k2+OZ0GJWlUeDDxJJUAtJNBIZKElOjucoOCG8oBAa8Dwz9UN7He3kXljxJR8LKbhSRSbjpbIv4D15pFItBNbqF7Faxy/h8CvJ2QF+UFRnM9NZdSk/pzjsEs9xtsGiUlvbLdkGXVxEK6srDA==$NQO2Q7CCn9xkCNBIS3foKw==
cache-control: private, max-age=0, no-store, no-cache, must-revalidate, post-check=0, pre-check=0
expires: Thu, 01 Jan 1970 00:00:01 GMT
set-cookie: __cf_bm=skWvrqkVN2vmdz9saHNzPAJoJAZ4W2LWmGxdNt1i1c8-1739090701-1.0.1.1-PZIVLSVXgbnXA5T7AJkcjNXMzp6QazEfu_zxAjCK4k69D9R7ZMPTbcjif6JfEQgSgiXhHLXxQfZTBX69KT_URw; path=/; expires=Sun, 09-Feb-25 09:15:01 GMT; domain=.deepseek.com; HttpOnly; Secure; SameSite=None
strict-transport-security: max-age=31536000; includeSubDomains; preload
x-content-type-options: nosniff
server: cloudflare
cf-ray: 90f294b5d8d54115-SIN


```



2025年2月9日截图纪念：



![image-20250209164418313](https://cdn.fangyuanxiaozhan.com/assets/1739090662149wnDbdMyG.png)

ai.com 是极其珍贵的顶级域名，以前ai.com是重定向到openai的服务，现在全球用户可以通过ai.com 直达 deepseek的服务，颇有钞能力改变一切的味道。



![deepseek-and-chatgpt](https://cdn.fangyuanxiaozhan.com/assets/1739092181792z5QnjRMR.png)

**I'M RICH!**
