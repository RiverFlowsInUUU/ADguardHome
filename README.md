## 重定向53端口到Adguard Home

## 两个端口冲突，第一个3000，第二个54

## 上游DNS服务器
```
223.5.5.5
114.114.114.114
（建议填入本地运营商DNS）
8.8.8.8
8.8.4.4
```

## 负载均衡

## Bootstrap DNS 服务器   (此处:54与第二个设置相同）
```
114.114.114.114:54
1.1.1.1:54
```

## 规则订阅
```
HalfLife，规则合并自 EasylistChina、EasylistLite、CJX’sAnnoyance 合并规则（每周更新)
https://gitee.com/halflife/list/raw/master/ad.txt
 
anti-AD 目前中文区命中率最高的广告过滤列表，精确的广告屏蔽和隐私保护。已支持AdGuardHome，dnsmasq，Surge，Pi-Hole，SmartDNS等。Github地址：https://github.com/privacy-protection-tools/anti-AD
https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/master/anti-ad-easylist.txt
 
ChinaList+EasyList
http://sub.adtchrome.com/adt-chinalist-easylist.txt
 
EasyList China 中文补充规则
https://easylist-downloads.adblockplus.org/easylistchina.txt
 
xinggsf，乘风广告过滤规则
https://gitee.com/xinggsf/Adblock-Rule/raw/master/rule.txt
```

## 自定义规则 去除YouTube广告
```
/googleads.$~script,domain=~googleads.github.io
/pagead/lvz?
||google.com/pagead/
||static.doubleclick.net^$domain=youtube.com
||youtube.com/get_midroll_
||safebrowsing.googleapis-cn.com
||doubleclick.net
```


# 最后将软路由的DNS设置为其ip地址如192.168.11.1
