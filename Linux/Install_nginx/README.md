# Install nginx

## Install epel และ packages ที่จำเป็น
ใน CentOS มักจะมีแพ็กเกจให้ใช้ได้น้อยกว่าของ Fedora ทางทีมของ Fedora จึงสร้าง repo ชื่อ EPEL (Extra Packages for Enterprise Linux) สำหรับผู้ใช้ RedHat และ CentOS
```
yum install -y epel-release
yum install -y net-tools mlocate wget vim yum-utils htop
```

## ระบุ repo ของ NGINX
สร้างไฟล์ช่อ nginx.repo
```
vi /etc/yum.repos.d/nginx.repo
```

และใส่ข้อมูลตามนี้
```
[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
gpgcheck=0
enabled=1
```

## Install Nginx และตั้งค่าให้เริ่มต้นทำงาน
```
yum -y install nginx
systemctl enable nginx && systemctl start nginx
```

## ทดสอบ
ลองเปิดเบร้าเซอร์และใส่ ip address ของเครื่องที่เราได้ติดตั้งลงไป ก็จะพบหน้า wellcome ของ nginx ก็เป็นอันเสร็จสิ้น
![alt text](https://github.com/learninglife-d/note/tree/master/Linux/install_nginx/nginx-welcome.png)

