# fj-dns2proxy
Offensive DNS server

This tool is inspired by Loenardo's projet https://github.com/LeonardoNve/dns2proxy

This version use UDP socket to receive/send DNS messages and scapy lib to decode/rewrite packets

Two main features:
----------
- Visual and colored outout to console (wouhaaa !!!)
- Juste only one configuration file  

In fj-transform.cfg file:
----------
- you must used regular expresion to create rewrrite rules
- you can transform a string (part of fqdn), entire fqdn, or antire domain name






