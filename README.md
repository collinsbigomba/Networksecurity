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
# snort
- install the binary with apt install snort and you will have to type in your ip address of your entire subnet ie 192.168.23.0/24
- For more details about snort id advise you to check out its man page (man snort)
- snort -T -i enp0s3 -c /etc/snort/snort.conf
-  where the T switch initiates testing mode
-  i is the interface (this might differ across multiple networks)
-  c is the configuration file which by default is in the /etc/ directory as per FHS standard
  <br>  <img src="https://github.com/collinsbigomba/Networksecurity/blob/main/images/snort.png" /></br>
<br> u can check out snorpy if youre having difficulty in creating rules</br>
<br> snort - A -alert mode</br>
   - l - logs which are stored in /var/log/snort</br>
   - i - interace
   - q - quiet mode
<br>snort -A console -i enp0s3 -c /etc/snort/snort.conf -q </br>
<br>  This command initiates snort to start and is updated with your current network activity as you can see i used nmap to scan any ip from the subnet and it showed me both the attacker ip and target ip</br>
<br>  <img src="https://github.com/collinsbigomba/Networksecurity/blob/main/images/snortattack.png" /></br>
<br>  <img src="https://github.com/collinsbigomba/Networksecurity/blob/main/images/snortattack1.png" /></br>
- As you can see the in the images above, i carried out an nmap scan on the ip address of 192.168.17.14 and snort was able to recognize the attack on the network which inceases the security of the network since the administrator can know the attacking ip address and block it
- Though if you onfigure proxychains im sure you can get around the detection

# Suricata
- install the software with apt install suricata command in the terminal
- For more details about suricata, check out its help section (suricata --help)
- suricata uses the systemd and you can enable it by typing systemctl enable suricata.service
- 


