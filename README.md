# MapProxy

Harita hizmetlerinden (GeoServer, QGIS Server, ArcGIS Server vb.) gelen verileri önbelleğe alarak, sunucuyu sürekli yormayan ve daha hızlı bir **proxy** dir.

MapProxy ile verilerinizi **WMS** veya **WMTS/TMS** olarak sunabilirsiniz.

**QGIS** gibi masaüstü uygulamalarında veya **OpenLayers** gibi kütüphaneler ile rahatlıkla kullanılabilir.

**Açık Kaynak** kodlu bir uygulamadır.

![mapproxy-overview](https://user-images.githubusercontent.com/95212909/156734539-ec2922cc-2a5e-4e12-a44f-0fc173fb43d8.png)

-----

## KURULUM ve YAPILANDIRMA AYARLARI

#### [Kurulum videosu için tıklayınız](https://www.youtube.com/watch?v=dF_2r2awycQ)

-----

<b>1. Python kurulumu</b>
```
sudo apt install python3
```
<b>2. Python sürüm kontrolü</b>
```
python3 --version
```
<b>3. pip kurulumu</b>
```
sudo apt update
sudo apt install python3-pip
```
<b>4. pip sürüm kontrolü</b>
```
pip --version
```
<b>5. MapProxy kurulumu</b>
```
sudo apt install mapproxy
```
<b>6. MapProxy için yeni bir kurulum dosyası oluşturma</b>
```
mapproxy-util create -t base-config youtube_mapproxy
```
<b>7. oluşturduğumuz dosya yoluna git</b>
```
cd youtube_mapproxy
```
<b>8. MapProxy çalıştırmak komutu</b>
```
mapproxy-util serve-develop config.yaml
```
<b>farklı bir port ile çalıştırmak için:</b>
```
mapproxy-util serve-develop -b 0.0.0.0:8090 config.yaml
```
<b>**seed** çalıştırma komutu:</b>
```
sudo mapproxy-seed -f config.yaml -c 4 seed.yml
```
