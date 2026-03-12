# งาน WEEK 10
### N-Tier Architecture: Multi-Tier on Docker
## 👤 **ข้อมูลนักศึกษา**
* **ชื่อ** : สรภูริ์ ทองจันทร์
* **สาขา** : วิศวกรรมคอมพิวเตอร์ ( เทียบโอน )
* **รหัส** : 675430206078-7

## 🎯 วัตถุประสงค์การเรียนรู้
* ✅ อธิบายข้อดีของการใช้ Docker แทน Traditional VM Deployment ได้
* ✅ เขียน Dockerfile สำหรับ Node.js Application ได้
* ✅ ใช้งาน Docker Compose เพื่อจัดการ Multi-Container Application ได้
* ✅ ตั้งค่า Network ระหว่าง Containers ได้
* ✅ สร้าง Docker volumes สำหรับ persistent data ได้
* ✅ วิเคราะห์และเปรียบเทียบ VM Deployment vs Docker Deployment ได้ ⭐

### สิ่งที่เปลี่ยนแปลงในการใช้ Docker แทน VM:
|Component	|VM|	Docker|
|:--|:--|:--|
|PostgreSQL	|apt install postgresql|	postgres:16-alpine image|
|Node.js	|nvm install 20 + PM2|	node:20-alpine + Dockerfile|
|Nginx	|apt install nginx	|nginx:alpine image|
|SSL	Self-signed certificate|	Self-signed ใน Nginx container|
|Network|	localhost + ports|	Docker internal network|
|Data	|Files on VM|	Docker volumes|
|Config	|Files in /etc/	|Mounted config files|
|Management|	systemctl, pm2|docker compose|