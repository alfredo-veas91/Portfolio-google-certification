``` bash
cd /etc/suricata
ls 
cd rules/
less custom.rules

#### Un ejemplo de firma encontrada en el archivo customs.rules

alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:estabilished; content:"GET";sid:12345;rev:1;)

############
cat custom.rules

alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)

pass http 172.17.0.77 any -> $EXTERNAL_NET any (msg:"BAD USER-AGENT";flow:established,to_server;content:!”Mozilla/5.0”; http_user_agent; sid: 12365; rev:1;)


############
ls -l /var/log/suricata

############
sudo suricata -r sample.pcap -S custom.rules -k none
############
ls -l /var/log/suricata

cat /var/log/suricata/fast.log

11/23/2022-12:38:34.624866  [**] [1:12345:3] GET on wire [**] [Classification: (null)] [Priority: 3] {TCP} 172.21.224.2:49652 -> 142.250.1.139:80

11/23/2022-12:38:58.958203  [**] [1:12345:3] GET on wire [**] [Classification: (null)] [Priority: 3] {TCP} 172.21.224.2:58494 -> 142.250.1.139:80
############
jq . /var/log/suricata/eve.json | less

jq -c "[.timestamp,.flow_id,.alert.signature,.proto,.dest_ip]" /var/log/suricata/eve.json
```

