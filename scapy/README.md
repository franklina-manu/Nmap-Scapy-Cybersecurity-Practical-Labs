
 1. Launch Scapy
sudo su
scapy

2. Basic Packet Sniffing
Start sniffing:
sniff()

--Generate traffic:
ping google.com
screenshot:
![image] (https://github.com/franklina-manu/Nmap-Scapy-Cybersecurity-Practical-Labs/blob/main/scapy/interface-sniff.png?raw=true)

--Stop sniffing:
CTRL + C on both terminals
--Save results:
paro = _
paro.summary()


3. Interface-Specific Sniffing
sniff(iface="br-internal")

--Generate traffic:
ping 10.6.6.1
Open browser → http://10.6.6.23
paro2 = _
paro2.summary()
Screenshot:
![image](https://github.com/franklina-manu/Nmap-Scapy-Cybersecurity-Practical-Labs/blob/main/scapy/ping%20google.com.png?raw=true)

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



