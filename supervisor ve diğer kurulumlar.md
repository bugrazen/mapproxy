## Supervisor Kurulumu

```
pip install supervisor
```

<b>supervisord.conf dosyasına kopyalanacak alan</b>
```
[program:mapproxy]
command= /usr/bin/mapproxy-util serve-develop -b 0.0.0.0:8090 config.yaml
directory=/Masaüstü/youtube_mapproxy
autorestart=true
redirect_stderr=true
stdout_logfile=/mnt/ortofoto/hgm/mapproxy.log
stdout_logfile_maxbytes=500MB
stdout_logfile_backups=50
stdout_capture_maxbytes=1MB
stdout_events_enabled=false
loglevel=warn
```
---
### Diğer Kurulumlar
<b>SSH bağlantısı</b>
```
sudo apt install openssh-server
```
<b>IP adresi almak için</b>
```
sudo apt install net-tools
```
