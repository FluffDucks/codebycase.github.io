---
layout: article
title: Collection - Operation Systems Notes
key: c02-operation-systems-notes
categories: Collections
tags: Linux, Unix, macOS, Windows
---

# Linux/Unix

- Copy file to another server

> scp prime.war lchen@ny-sample-002:/home/lchen

- Grep log with regular expression from the zip file:

> zgrep --color 'CCVI[0-9]\{12\}' /logs/pl_timings.17-11-01_21.log.gz

- Check if a domain name accessible from DNS

> dig www.codebycase.com +noall +answer

```
www.codebycase.com.	1799	IN	CNAME	codebycase.github.io.
codebycase.github.io.	3600	IN	CNAME	sni.github.map.fastly.net.
sni.github.map.fastly.net. 30	IN	A	151.101.21.147
```

- Curl with proxy and client certificate

> curl -E "./Priceline DB.pem" --key "./Priceline DB.key" -H "Authorization: orgId=116770"  --proxy "nw-prx-v01.dqs.pcln.com:8080" https://api.searchads.apple.com/api/v1/campaigns

- Create a pkcs12 (.pfx or .p12) from OpenSSL files (.pem, .cer, .crt,...)

>openssl pkcs12 -export -in <PEM_file>.pem -inkey <PRIVATE_KEY>.key -out <FILENAME>.p12

- Install certificate to JVM keystore

>sudo keytool -import -alias sunas -keystore /Library/Java/JavaVirtualMachines/jdk1.8.0_144.jdk/Contents/Home/jre/lib/security/cacerts -file /Users/lchen/Downloads/deva-consul.dqs.pcln.com-443.crt

the keystore password is changeit by default


