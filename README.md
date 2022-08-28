# MONITORING SENSOR


## Kullanımı


* collectd: collectd.conf dosyası ile monitor edilenler redise yazılır

* redis: collectd verileri buraya yazılır

* collectd_script: redisten okunan veri influxdb api gw'e yazılır.


## API_GW Kullanımı

-- influxdb kurulmuş olmalıdır. Influxdb'ye bağlanıp mevcut kullanıcının token bilgisini alın. Data -> Tokens -> Kullanıcı'nın üzerine tıklayın --> Copy to Clipboard

-- influxdb'ye ait olan bilgileri güncelle

-- Web container içine bağlan

-- Aşağıdaki komutlar ile apigw token oluştur:

root@753220044fab:/code# python3 manage.py migrate
root@753220044fab:/code# python3 manage.py createsuperuser
Username (leave blank to use 'root'): yetkili_kullanici
Email address: 
Password: 
Password (again): 
Superuser created successfully.
root@753220044fab:/code# python manage.py drf_create_token yetkili_kullanici


-- collectd_script içindeki apigw host ve token bilgilerini güncelle.


