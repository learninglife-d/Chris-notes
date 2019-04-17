# Config php 7.2 บน NGINX

เปิดไฟล์ /etc/php-fpm.d/www.conf
```
vi /etc/php-fpm.d/www.conf
```

แก้ไขไฟล์ ตามนี้
```
user = nginx
group = nginx

listen = 127.0.0.1:9000
```

### Note
```
ในโปรแกรม vi ให้พิม / แล้วตามด้วยคำที่ต้องการค้นหา มันจะเป็นการเซิร์ชคำในไฟล์
ตัวอย่าง เช่น
/user
คือ การเซิร์ชหาคำว่า user ที่อยู่ภายในไฟล์นั้น
```

## Start php-fpm
```
systemctl start php-fpm
systemctl enable php-fpm
```

## Configuring Nginx to use PHP-FPM
เปิดไฟล์ /etc/nginx/conf.d/default.conf
```
vi /etc/nginx/conf.d/default.conf
```

ให้เพิ่มโค๊ดนี้ลงไปในไฟล์
```
location ~ \.php$ {
    root           /usr/share/nginx/html;
    fastcgi_pass   127.0.0.1:9000;
    fastcgi_index  index.php;
    fastcgi_param  SCRIPT_FILENAME         $document_root$fastcgi_script_name;
    include        fastcgi_params;
    }
```

## สั่ง restart Nginx และ php-fpm
```
systemctl restart nginx && systemctl restart php-fpm
```