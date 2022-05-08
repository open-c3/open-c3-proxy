# open-c3-proxy
open-c3代理

## 什么情况下使用？

跨区域访问open-c3的服务时，访问速度慢。

如：openc3部署在了海外，国内访问慢。

## 使用方式

```
cd /data
git clone https://github.com/open-c3/open-c3-proxy
/data/open-c3-proxy/bin/start addr port
# addr 为要代理的openc3的ip地址或者域名，port为本地开启的新端口
# 如：/data/open-c3-proxy/bin/start 10.10.10.2 8080
```

# 版本

## v1

使用nginx缓存方式，请求过的文件进行缓存。

## v2

通过bin/sync工具把js或者css文件同步到代理机，代理机上有文件的情况下使用代理机的，如果文件不存在，服务请求回后端。
