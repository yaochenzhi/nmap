# nmap domain
nmap domain.com
# nmap ip
nmap ip.x.x.x
# nmap multi-ip all at once
nmap 192.168.0.1 192.168.0.7 192.168.0.191
# nmap an ip range
nmap 192.168.0.1-30
# nmap the entire subnet
nmap 192.168.0.*
# nmap from file list 
$] echo -e "192.168.0.3\n192.168.0.5" > targets.txt
$] nmap -iL targets.txt

# Aggressive / Detailed Scan [ More info ]
nmap -A domain.com
nmap --tracerouter domain.com
nmap -O domain.com
nmap -sV domain.com (service version column)

# More Port Scanning Options
nmap -F domain.com (fast mode)
nmap -p 20-25,80,443 domain.com
nmap -p http,mysql domain.com
nmap -p- domain.com (all ports)
nmap --open domain.com

# Saving Scan Results
nmap -F -oN results.txt domain.com
nmap -F -oX results.xml domain.com

nmap -v domain.com