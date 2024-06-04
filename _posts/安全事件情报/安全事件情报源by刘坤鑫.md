# 今日工作

整理情报源。

## IOC文章博客源

### 已爬

    https://blog.talosintelligence.com/  *****
    https://s.tencent.com/research/report/
    https://research.checkpoint.com/category/threat-research/  *****
    https://securityintelligence.com/category/x-force/  *****
    https://www.microsoft.com/security/blog/  *****
    https://www.fortinet.com/blog/threat-research.html  *****
    https://www.proofpoint.com/us/blog/threat-insight
    https://news.sophos.com/en-us/ *****

### 其他

    blog.talosintelligence.com  *****
    blog.malwarebytes.com  *****
    research.checkpoint.com   *****
    cofense.com  *****
    www.fortinet.com  *****
    securityintelligence.com  *****
    www.proofpoint.com
    isc.sans.edu  *****
    news.sophos.com *****
    www.microsoft.com  *****
    www.cybereason.com
    www.us-cert.gov
    blog.netlab.360.com
    krebsonsecurity.com
    unit42.paloaltonetworks.com
    www.cyberark.com
    securelist.com
    www.trustwave.com
    www.zscaler.com
    www.wordfence.com
    www.europol.europa.eu
    www.darkreading.com
    blog.ptsecurity.com
    www.recordedfuture.com
    blog.semmle.com
    www.riskiq.com
    wikileaks.org

## 其他

```yaml
-
   url: https://www.botvrij.eu/data/
   threat_type: ioc
   content_type: 
   note: 文件夹，里面有各种IOC
-
   url: http://osint.bambenekconsulting.com/feeds/
   threat_type: c&c, dga...
   content_type: 
   note: 文件夹，大杂烩
-
   url: https://certstream.calidog.io/
   threat_type: 
   content_type: 
   note: 查询有问题的证书
-
   url: https://www.ccssforum.org/malware-certificates.php
   threat_type: 
   content_type: 
   note: 恶意软件证书
-
   url: http://cinsscore.com/list/ci-badguys.txt
   threat_type: 
   content_type: ip
   note: cins是商业ip评分，这份名单是评分很差的那部分
-
   url: https://github.com/martenson/disposable-email-domains
   threat_type: 
   content_type: email
   note: 
-
   url: https://osint.digitalside.it/Threat-Intel/csv/
   threat_type: ioc
   content_type: 
   note: 原网站提供多种共享方式[MISP, STIX2, CSV, TXT, TAXII2]
-
   url: https://securitytrails.com/dns-trails
   threat_type: 
   content_type: 
   note: 查dns
-
   url: https://feodotracker.abuse.ch/downloads/ipblocklist.csv
   threat_type: c&c
   content_type: ip
   note: 5分钟更新一次
-
   url: https://feodotracker.abuse.ch/downloads/ipblocklist_aggressive.csv
   threat_type: c&c
   content_type: ip
   note: 上一个的完整版
-
   url: https://feodotracker.abuse.ch/downloads/malware_hashes.csv
   threat_type: 
   content_type: file
   note: 5分钟更新一次
-
   url: http://iplists.firehol.org/
   threat_type: 
   content_type: 
   note: 超过 400 个公开可用的 IP 订阅
-
   url: https://www.iblocklist.com/lists
   threat_type: 
   content_type: ip
   note: 各种类型
-
   url: https://raw.githubusercontent.com/stamparm/ipsum/master/ipsum.txt
   threat_type: 
   content_type: ip
   note: 
-
   url: http://malc0de.com/bl/IP_Blacklist.txt
   threat_type: 
   content_type: ip
   note: sinkhole，好像半年没更新了
-
   url: https://maltiverse.com/dashboards/feeds
   threat_type: ioc
   content_type: 
   note: 聚合了一吨ioc，集成了几十家网站的IOC源
-
   url: https://data.netlab.360.com/feeds/dga/dga.txt
   threat_type: dga
   content_type: 
   note: 
-
   url: https://openphish.com/feed.txt
   threat_type: phishing
   content_type: url
   note: 付费解锁更多功能
-
   url: http://data.phishtank.com/data/online-valid.csv
   threat_type: phishing
   content_type: url
   note: 没有密钥一天只能下有限次？
-
   url: https://rescure.fruxlabs.com/rescure_blacklist.txt
   threat_type: ioc
   content_type: ip
   note: 
-
   url: https://rescure.fruxlabs.com/rescure_domain_blacklist.txt
   threat_type: ioc
   content_type: domain
   note: 
-
   url: https://rescure.fruxlabs.com/rescure_malware_hashes.txt
   threat_type: ioc
   content_type: file
   note: 
-
   url: https://rescure.fruxlabs.com/covid.txt
   threat_type: ioc
   content_type: domain
   note: COVID-19
-
   url: https://rescure.fruxlabs.com/maze.txt
   threat_type: Ransomware
   content_type: domain
   note: 
-
   url: https://isc.sans.edu/feeds/suspiciousdomains_High.txt
   threat_type: 
   content_type: domain
   note: 除了高危险，还有中、低危险
-
   url: https://sslbl.abuse.ch/blacklist/sslblacklist.csv
   threat_type: c&c
   content_type: file
   note: SSL Certificate Blacklist，5分钟更新
-
   url: https://sslbl.abuse.ch/blacklist/sslipblacklist.csv
   threat_type: c&c
   content_type: ip
   note: Botnet C2 IP Blacklist，5分钟更新
-
   url: https://sslbl.abuse.ch/blacklist/sslipblacklist_aggressive.csv
   threat_type: c&c
   content_type: ip
   note: Botnet C2 IP Blacklist，上一条的完整版
-
   url: https://sslbl.abuse.ch/blacklist/ja3_fingerprints.csv
   threat_type: c&c
   content_type: file
   note: JA3 Fingerprint Blacklist，5分钟更新
-
   url: https://threatconnect.com/blog/ingest-technical-blogs-reports/
   threat_type: ioc
   content_type: 
   note: 在九十多个开源博客中提取 IOCs，不过还没搞明白咋用
-
   url: https://raw.githubusercontent.com/WSTNPHX/scripts-n-tools/master/malware-email-addresses.txt
   threat_type: 
   content_type: email
   note: 
-
   url: https://www.threatminer.org/
   threat_type: ioc
   content_type: 
   note: 可以查询IOC
-
   url: https://urlhaus.abuse.ch/browse/
   threat_type: 
   content_type: url
   note: 含分类
-
   url: https://iocfeed.mrlooquer.com/feed.csv
   threat_type: ioc
   content_type: ip
   note: 支持IPv6
```

上述网站来源：

https://github.com/hslatman/awesome-threat-intelligence/blob/master/README_ch.md

## 未整理

以前整理的，还没有分类

    https://isc.sans.edu/feeds/suspiciousdomains_High.txt
    http://data.netlab.360.com/feeds/dga/dga.txt
    https://openphish.com/feed.txt
    http://cinsscore.com/list/ci-badguys.txt
    http://cybersweat.shop/iprep/iprep_ramnode.txt
    http://blocklist.greensnow.co/greensnow.txt
    https://www.malwaredomainlist.com/hostslist/hosts.txt
    https://myip.ms/files/blacklist/htaccess/latest_blacklist.txt
    https://openphish.com/feed.txt
    https://ransomwaretracker.abuse.ch/downloads/RW_DOMBL.txt
    https://ransomwaretracker.abuse.ch/downloads/RW_IPBL.txt
    https://ransomwaretracker.abuse.ch/downloads/RW_URLBL.txt
    http://sblam.com/blacklist.txt
    http://www.ciarmy.com/list/ci-badguys.txt
    http://www.nothink.org/blacklist/blacklist_malware_dns.txt
    http://www.nothink.org/blacklist/blacklist_malware_http.txt
    http://www.nothink.org/blacklist/blacklist_malware_irc.txt
    http://www.nothink.org/blacklist/blacklist_ssh_all.txt
    http://cinsscore.com/list/ci-badguys.txt
    http://dns-bh.sagadc.org/
    http://rules.emergingthreats.net/fwrules/
    http://danger.rulez.sk/projects/bruteforceblocker/

# 明天安排


