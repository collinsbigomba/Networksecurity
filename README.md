# Networksecurity

## Objective
The goal is to install and configure snort and suricata

The Detection Lab project aimed at installing snort and suricata which are both network intrusion detection systems (NIDS) and intrusion prevention systems (IPS) that monitor network traffic for suspicious activity and potential threats.

### Skills Learnt
- Network Traffic analysis
- Intrusion detection and prevention
- snort rule writing
- System and network administration


### Tools Used
- Snort
- suricata
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- 

## Steps
snort
- install the binary with apt install snort and you will have to type in your ip address of your entire subnet ie 192.168.23.0/24
- For more details about snort id advise you to check out its man page (man snort)
- snort -T -i enp0s3 -c /etc/snort/snort.conf
-  where the T switch initiates testing mode
-  i is the interface (this might differ across multiple networks)
-  c is the configuration file which by default is in the /etc/ directory as per FHS standard
  <br>  <img src="https://github.com/collinsbigomba/metasploitable2/blob/main/images/snort.png" /></br>



  b
