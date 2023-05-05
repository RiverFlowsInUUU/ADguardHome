## 重定向53端口到Adguard Home

## 两个端口冲突，第一个3000，第二个54

## 上游DNS服务器
```
方案一
223.5.5.5
114.114.114.114
（建议填入本地运营商DNS）
8.8.8.8
8.8.4.4
方案二
1.1.1.1
8.8.8.8
tls://223.6.6.6:853
tls://1.12.12.12:853
tls://120.53.53.53:853
https://223.6.6.6/dns-query
https://1.12.12.12/dns-query
https://120.53.53.53/dns-query
```

## 负载均衡

## Bootstrap DNS 服务器   (此处:54与第二个设置相同）
```
114.114.114.114:54
1.1.1.1:54
```

## DNS缓存关闭 查询速度0


## 规则订阅

```
anti-AD 
Github地址：https://github.com/privacy-protection-tools/anti-AD
https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/master/anti-ad-easylist.txt
 
ChinaList+EasyList
http://sub.adtchrome.com/adt-chinalist-easylist.txt
 
EasyList China 中文补充规则
https://easylist-downloads.adblockplus.org/easylistchina.txt

BlueSkyXN 百万拦截
Github地址：https://github.com/BlueSkyXN/AdGuardHomeRules
https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/all.txt

秋风のとおり道
Github地址：https://github.com/TG-Twilight/AWAvenue-Adblock-Rule
https://ghproxy.net/https://raw.githubusercontent.com/TG-Twilight/AWAvenue-Adblock-Rule/main/AWAvenue-Adblock-Rule.txt
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


## 最后将软路由的DNS设置为其ip地址如192.168.11.1


## 与openclash相配合
参考：https://github.com/vernesong/OpenClash/discussions/1420
```
openclash：关闭本地DNS劫持，打开自定义上游DNS
Adguard Home：上游DNS设置为127.0.0.1:7874
```
## SSR Plus 设置 先开AD Home 再开SSRP
![image](https://user-images.githubusercontent.com/66954900/227261341-76f48a37-9bce-40c2-ab3f-aa50a729a1fd.png)

