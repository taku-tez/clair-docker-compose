## AmazonLinux2 or Other Linux vulnerability scan with clair.

#### docker-compose up clair
```
$ docker-compose up -d
```

#### Install clair-sccaner
```
$ wget https://github.com/arminc/clair-scanner/releases/download/v11/clair-scanner_linux_amd64 -O clair-scanner
$ mv clair-scanner /usr/local/bin/ && chmod a+x clair-scanner
```

#### Exec vulnerability scan
```
clair-scanner -c http://127.0.0.11:6060 --ip=[HostIP] --reportAll=true [ImageID]
```
