## วิธีการติตตั้ง Platformio
1. เปิดบราวเซอร์ เพื่อดาวน์โหลด git จากนั้นก็ติดตั้งที่คอมพิวเตอร์
โดยไปที่ 
- https://github.com/choompol-boonmee/iotset1
 - Download  Git : https://git-scm.com/download/win
2. เมื่อดาวโหลดเสร็จ เปิด command prompt ใส่คำสั่ง 
> git clone https://github.com/choompol-boonmee/iotset1.git
3. รัน โปรแกรมในโฟลเดอร์ software 
``
python-3.9.1-amd64.exe
pip install -U platformio
``
4. เปิด command prompt หรือ cmd เข้าไปโฟลเดอร์ iotset1
``
cd iotset1/examples
dir
``
5. รันตัวอย่างที่ 1
``
Cd ioset1/examples/ex01
pio run
``
6. รันตัวอย่างที่ 2
``
cd iotset1/examples/ex03
pio run
``
