
 1. Launch Scapy
```bash
sudo su
scapy

2. Basic Packet Sniffing
Start sniffing:
sniff()

--Generate traffic:
ping google.com

--Stop sniffing:
CTRL + C on both terminals

--Save results:
paro = _
paro.summary()
Screenshot:
/screenshots/sniff-basic.png

3. Interface-Specific Sniffing
sniff(iface="br-internal")

--Generate traffic:
ping 10.6.6.1
Open browser → http://10.6.6.23
paro2 = _
paro2.summary()
Screenshot:
/screenshots/interface-sniff.png

4. ICMP-Only Sniffing
sniff(iface="br-internal", filter="icmp", count=5)
Generate traffic:
ping 10.6.6.23

Save result:
paro3 = _
paro3.summary()
paro3[3]
Screenshot:
/screenshots/sniff-icmp.png



