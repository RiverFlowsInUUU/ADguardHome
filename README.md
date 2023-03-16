## 重定向53端口到Adguard Home

## 两个端口冲突，第一个3000，第二个54

## 上游DNS服务器
```
223.5.5.5
114.114.114.114
8.8.8.8
8.8.4.4
101.226.4.6
tls://dot.360.cn
120.196.165.24
https://dns10.quad9.net/dns-query
https://dns.google/dns-query
https://doh.360.cn/dns-query
https://doh-jp.blahdns.com/dns-query
https://dns.alidns.com/dns-query
tls://dns.alidns.com
tls://dns.google
tls://1dot1dot1dot1.cloudflare-dns.com
```

## 负载均衡

## Bootstrap DNS 服务器   (此处:54与第二个设置相同）
```
114.114.114.114:54
1.1.1.1:54
```
