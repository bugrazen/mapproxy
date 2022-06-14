## Supervisor Kurulumu

```
sudo apt install supervisor
```

<b>supervisord.conf dosyasına kopyalanacak alan</b>
```
[program:mapproxy]
command= /usr/bin/mapproxy-util serve-develop -b 0.0.0.0:8090 config.yaml
directory=/home/youtube/Masaüstü/youtube_mapproxy
autorestart=true
redirect_stderr=true
stdout_logfile=/home/youtube/Masaüstü/youtube_mapproxy/mapproxy.log
stdout_logfile_maxbytes=500MB
stdout_logfile_backups=50
stdout_capture_maxbytes=1MB
stdout_events_enabled=false
loglevel=warn
```
<b>kopyalamayı yaptıktan sonra uygulamayı yeniden başlatmak için aşağıdaki komutları kullanınız</b>
```
sudo supervisorctl reread
```
```
sudo supervisorctl update
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
