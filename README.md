# MapProxy

Harita hizmetlerinden (GeoServer, QGIS Server, ArcGIS Server vb.) gelen verileri önbelleğe alarak, sunucuyu sürekli yormayan ve daha hızlı bir **proxy** dir.

MapProxy ile verilerinizi **WMS** veya **WMTS/TMS** olarak sunabilirsiniz.

**QGIS** gibi masaüstü uygulamalarında veya **OpenLayers** gibi kütüphaneler ile rahatlıkla kullanılabilir.

**Açık Kaynak** kodlu bir uygulamadır.

![mapproxy-overview](https://user-images.githubusercontent.com/95212909/156734539-ec2922cc-2a5e-4e12-a44f-0fc173fb43d8.png)

-----

## KURULUM ve YAPILANDIRMA AYARLARI


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
python3 install pip

```
<b>4. MapProxy kurulumu</b>
```
pip install MapProxy
```
<b>5. MapProxy için yeni bir kurulum dosyası oluşturma</b>
```
mapproxy-util create -t base-config youtube_proxy
```
<b>6. oluşturduğumuz dosya yoluna git</b>
```
cd youtube_proxy
```
<b>6. MapProxy çalıştırmak komutu/b>
```
mapproxy-util serve-develop config.yaml
```
<b>farklı bir port ile çalıştırmak için:</b>
```
mapproxy-util serve-develop -b 0.0.0.0:8080 config.yaml
```
<b>**seed** çalıştırma komutu:</b>
```
sudo mapproxy-seed -f config.yaml -c 4 seed.yml
```
