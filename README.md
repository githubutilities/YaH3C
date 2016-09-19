# H3C SYSU East(802.1X)

```
# Login
---> Start
<--- Request, Identity
---> Response, Identity
<--- Request, EAP-MD5-CHALLENGE
---> Response, EAP-MD5-CHALLENGE
<--- Some unknown code
<--- Success

# Then enter random check loop
<--- Request, Identity
---> Response, Identity

# Logoff
# Not responding to random check loop also results in auto-logoff
---> Logoff
<--- Failure
```

> Request ID, `version hash` + `username`
>
> EAP-MD5-CHALLENGE, `num` + `username`
>
> `num` is calculated by ( ordinal(first 16 character of case-sensitive password) xor ordinal(16 bytes md5 data converted to decimal) )

# [scapy](https://github.com/secdev/scapy)
* [华为H3C iNode客户端802.1X协议的分析和破解](https://story.tonylee.name/2016/07/14/hua-wei-h3c-inodeke-hu-duan-802-1xxie-yi-de-fen-xi-he-po-jie/)
* [中山大学东校区校园网认证的客户端（非官方）YaH3C](https://github.com/humiaozuzu/YaH3C)
* [西电北校区校园网客户端Linux CLI版 xd-h3c](https://github.com/godspeed1989/xd-h3c)
