CLI
===

tree
---

```shell
chapters
├── api.md
├── backend.md
├── chrome-plugins.md
├── cli.md
├── devices.md
├── documents.md
├── graphics.md
├── hardware.md
└── ops.md

0 directories, 9 files
```

sl
---

![SL](./images/cli/sl-tool.jpg)

curl
---

``` shell
curl -I -s -A 'Googlebot' www.phodal.com
HTTP/1.1 200 OK
Server: mokcy/0.17.9
Content-Type: text/html; charset=utf-8
Connection: keep-alive
Vary: Accept-Encoding
Vary: Accept-Language, Cookie
Content-Language: en
X-UA-Compatible: IE=Edge,chrome=1
Date: Thu, 09 Apr 2015 14:39:11 GMT
X-Page-Speed: Powered By Phodal
Cache-Control: max-age=0, no-cache
```

``` shell
curl --data "_method=PUT&led1=1&sensors1=22&sensors2=12&temperature=14" http://b.phodal.com/athome/1
```
