# Plutonium的mosdns配置
[mosdns食用方法](https://irine-sistiana.gitbook.io/mosdns-wiki/)
  
## 只有正确的dns配置才可以优化上网体验,类似的dns转发器越少越好
### 特点
- 使用geosite分流让域名去该去的地方解析,结果纯净无污染
- 仅抛弃海外ipv4ipv6双栈域名的ipv6记录,无需关闭ipv6玩起代理更省心
- 支持fallback,不在geosite内的域名将本地分组与国内分组并发解析结果更合适
- 支持缓存域名,优先从缓存获取结果随后mosdns自动更新缓存,不用担心缓存失效无法访问(需要在配置文件中手动开启)
- 文件注释齐全易理解
### 注意
- 请保证`mosdns.txt`,`geosite.dat`,`geoip.dat`文件存在否则可能无法使用(存放路径在文件中已使用注释标注)
- 如果让本机走代理海外dns组返回结果更佳,请确保海外dns组可以走代理
- 建议让mosdns做局域网内dns服务器的最上游
- 本配置默认监听5301端口
