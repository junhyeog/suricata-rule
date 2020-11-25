### snort(suricata) rule 파일을 제작하여 특정 사이트 트래픽을 탐지하여라.

- test.rules 파일에 20개의 사이트를 탐지하는 룰을 만든다.
- 이후 fast.log를 확인하면서 20개의 사이트가 제대로 탐지되는지 확인을 해 본다.
- 가급적이면 평문 통신(HTTP)이 이루어 지는 사이트 뿐만 아니라 TLS 통신(HTTPS)을 하는 사이트에 대한 탐지를 구현해 본다.

- https://gitlab.com/gilgil/sns/-/wikis/suricata/report-suricata-rule
- https://gitlab.com/gilgil/sns/-/wikis/suricata/suricata

### install
```
sudo apt install suricata
```

### run
```
suricata -s <rules file> -i <interface>
```
```
suricata -s test.rules -i enp0s3
```

### fast.log
```
tail -f /var/log/suricata/fast.log
```
