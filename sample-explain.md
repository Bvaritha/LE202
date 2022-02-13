# อธิบายโปรแกรม 1-6
## Run Example 1
Microcontroller ESP01 มีเสาอากาศสำหรับ WIFI ซึ่งในการเขียนโปรแกรมลงบน Microcontroller ต้องต่อกับ serial port หลังจากนั้นก็ดูตัวอย่างโปรแกรมโฟลเดอร์ Pattani โดยจะมีทั้งหมด 9 โปรแกรม โดยจะใช้โปรแกรม 01_Serial_Monitor ในโปรแกรมนี้เขียนขึ้นมาเพื่อทดสอบ มีทั้งหมด 2 ฟังก์ชัน คือ Set up รันครั้งเดียว และ Loop ที่จะรันแบบวนลูบ
- Set up จะ set serial port ที่ความเร็ว 115200
- Loop มีตัวแปรมาเพิ่ม count ขึ้นเรื่อยๆ โดยที่ให้แสดงผลตัวแปรcount ออกมาและให้หน่วงเวลา 1 วินาที
ในแต่ละโปรแกรมที่ใช้ platformio จะมี configuration file ชื่อว่า "platformio.ini"
วิธีการอัพโหลดโปรแกรมลงบนMicrocontroller ใช้คำสั่ง pio run -t upload เมื่อโปรแกรมพร้อมรันจะใช้คำสั่ง pio run device monitor เพื่อดูผลลัพธ์ ถ้าจะรีเซทให้กดปุ่มสีแดง
## Run Example 2
