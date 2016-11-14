# fj-dns2proxy
Offensive DNS server

This tool is inspired by Loenardo's projet https://github.com/LeonardoNve/dns2proxy

This version use UDP socket to receive/send DNS messages and scapy lib to decode/rewrite packets

##Two main features:
- Visual and colored outout to console (wouhaaa !!! +1)
- Juste only one configuration file  

##transform.cfg file:
- you must used regular expresion to create rewrrite rules
- you can transform a string (part of fqdn), entire fqdn, or antire domain name

```
# Example to rewrite a simple string: 
^wwww\.:www.
^social\.:www.
^web\.:www.
^account\.:accounts.
#
# Example to rewrite entire fqdn
^fred\.example\.com\.$:www.example.com.
#
# Example to rewrite fqdn to a fake host
^fred2\.example\.com:myhost.mydomain.com
#
# Example to rewrite entire domain name 
^.+\.example\.org:localhost
```

##Usage :
```
usage: fj-dns2proxy.py [-h] [-i IPLOCAL] [-r RESOLVER] [-c] [-s]

optional arguments:
  -h, --help            show this help message and exit
  -i IPLOCAL, --ipLocal IPLOCAL
                        Local IP to bind (default:all)
  -r RESOLVER, --resolver RESOLVER
                        resolver DNS (default:8.8.8.8)
  -c, --nocolor         Print without color
  -s, --silence         Silence mode
```


