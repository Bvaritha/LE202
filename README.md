# LE202
## Microcontroller 
### Digital
การเอาสัญญาณไฟฟ้ามาแปลงเป็นตัวเลขฐานสอง โดยจะพิจารณาแค่มีแรงดันกับไม่มีแรงดัน การใช้ข้อมูลดิจิตอลมาแทนตัวเลขจะขี้นอยู่กับแรงดัน (on off)
- มาใช้กับหลอดไฟ ให้แทนด้วยแรงดัน ขึ้นอยู่กับระบบข้อมูลที่เอาไปใช้
  - 1digit= 2bits แสดงโดยการเปล่งแสง
- มาใช้กับตัวอักษรไม่ว่าจะเป็นภาษาอังกฤษหรือภาษาไทยให้แทนด้วยตัวเลข 
  - 1digit = 4bits
### Voltages 
  ความต่างศักย์ของไฟฟ้าระหว่างจุดสองจุด หน่วยเป็น โวลต์ มี2ประเภท
1. กระแสสลับ วัดไฟบ้าน 220 V
2. กระแสตรง ขั้วบวก ลบ มีแหล่งกำเนิดไฟฟ้า ซึ่งแต่ละชนิดมีแรงดันไม่เหมือนกัน
- แบตเตอรี่ 2 A 1.5-1.6 V,Usb 5 V,แบตเตอร์ลิเที่ยมอิออน 3.6 V
### Computer 
มีหลายขนาด ตั้งแต่ใหญ่ลงมาถึงขนาดเล็ก ซึ่งเอาไว้เชื่อมโยงกับอินเทอร์เน็ต มีความเร็ว ความจุสูงขึ้นเรื่อยๆ
### Internet 
เชื่อมโยงทุกอย่างเข้าด้วยกันทั้งสัญญาณมือถือทั้งมีสายและไร้สาย ไวไฟ บลูทูธ 
- มีผู้ใช้งานมากกว่า 4,800,000,000 คน 
- มีเว็บไซต์ มากกว่า 1,800,000 เว็บไซต์
### Program lang
การพัฒนาซอฟท์แวร์ให้ทำงานบนคอมพิวเตอร์ชนิดต่างๆ โดยเริ่มจากภาษาแอสแซมบลี้ โดยพัฒนามาเรื่อยๆให้สามารถเขียนและเข้าใจได้ง่ายขึ้น รวดเร็วขึ้น
### Platformio 
Microcontroller มีบริษัทผู้ผลิต เช่น avr armel espressos เป็นต้นซึ่งแต่ละตัวแตกต่างกัน
แพลตฟอร์ม io เปนการพัฒนาซอฟท์แวร์แบบมาตรฐานที่เขียนโปรแกรมแบบเดียว แต่สามารถเขียนโปรแกรมลงบนmicrocontroller ได้หลายแบบ โดยที่สามารถพัฒนาได้หลายอย่าง
วิธีการเขียนโปรแกรมสามารถทำได้หลายแบบ เช่น arduinoนิยมมากก  สามารถนำไปประยุกต์ใช้ได้ทันที ไม่ต้องมาเขียนใหม่หมด
### Iotset1
การเตรียมการพัฒนา microcontroller 
1. เปิดบราวน์เซอร์ เพื่อดาวโหลด Git https://github.com/choompol-boonmee/lab63b.git ไปที่ Git-2.30.0.2-64-bit.exe แล้วติดตั้งที่คอมพิวเตอร์
2. เปิด command promt แล้วรันคำสั่ง git clone
3. รันโปรแกรมที่อยู่ในโฟลเดอร์ software
4. เปิด command promt แล้วไปที่โฟลเดอร์ ioset1
5. รันตัวอยางที่ 1
6. รันตัวอย่างที่ 2

## ตัวอย่างการเขียนโปรแกรม
### การรันโปรแกรม 1
 การเขียนโปรแกรมด้วยแพลตฟอร์มio โดยใช้ microcontroller ที่มีชื่อว่า EST01 มีเสาอากาศสำหรับwifi โดยจะต้องมีอุปกรณ์ ต่อไปยังซีเรียล จากนั้นก็เขียนโปรแกรมลงไปในmicrocontroller ตัวนี้โดยการเสียงไปยังซีเรียล จากนั้นก็ใช้โปรแกรมตัวอย่าง เพื่อทดสอบ
### การรันโปรแกรม 2
 การรันโปรแกรมโดยใช้microcontroller ที่มีชื่อว่า EST01 มีWi-Fiอยู่ในตัวเอง นำไปเสียบกับ USB แล้วจากนั้นอัพโหลดโปรแกรมเข้าไปตามตัวอย่างให้พร้อมทำงาน
### การรันโปรแกรม 3
  เป็นโปรแกรมที่รันบน microcontroller ส่งสัญญาIออกไปสู่ภายนอก EST01 มีทั้งinputและoutput จากนั้นก็เอาไปติดที่USB เพื่อให้พอร์ดออกมาใช่งานด้วย จำเป็นที่จะต้องใช้ adapters เสียบผ่านusb แล้วต่อกับ พอร์ต0ขาว 1เหลือง ถ้าต้องการให้outputออกมาที่ 0 โปรแกรมที่3จะส่งoutputมาที่0 แลิวต่อกับLedเพื่อให้แสงสว่าง จากนั้นก็เขียนโปรแกรม แต่ต้องเสียบขาio0เอาไปด้วย 
#### การรัน relay
  ถูกติดตั้งโปรแกรมที่3 ทำให้ส่งสัญญาณผ่าน พอร์ตที่0 ไปยังหลอดไฟ ส่งผลให้หลอดไฟกระพริบ จากนั้นก็เอาโปรแกรมมารันเพื่อใช้งานจริง เมื่อนำmicrocontroller มาเสียบที่relay ทำให้พอร์ต0 ส่งสัญญาณให้ เปิด-ปิดสวิตซ์ แล้วทำพาวเวอร์แบงค์มาต่อ เพื่อจ่ายไฟให้กับmicrocontroller เพื่อควบคุมให้รีเลย์ทำงาน เปิด ปิด โดยจะได้ยินเสียง
### การรันโปรแกรมที่4
 การนำสัญญาณinputจากภายนอก เข้ามาในmicrocontroller ให้พอร์ด1 input พอร์ด2 output ถ้าสัญญาณเป็น 1 ไปที่พอร์ต2 ทำให้ไฟดับ  ถ้าเป็น0 ไปที่พอร์ด1 ทำให้ไฟติด เมื่อลองไปต่อกับเซนเซอร์แสง ต่อกับไฟเลี้ยงcpu ถ้ามีแสงสว่างจะเป็น 0 ถ้ามืด จะเป็น1 ถ้าเอานิ้วปิดหน้าเซนเซอร์ ทำให้ไฟดับได้เหมือนกันตามสภาพแวดล้อม
### การรันโปรแกรม5
โปรแกรมที่สร้างเว็บเซิฟเวอร์ผ่านwifi นำตัวโปรแกรมที่5เชื่อมกับwi -Fi โดยให้ใส่ชื่อรหัส และพาสเวิร์ด อัพโหลดโปรแกรมขึ้นบน microcontroller  โดยเสียบไปที่usb หลังจากนั้นก็เข้าอัพโหลด เพื่อให้พร้อมรับโปรแกรม ในการทดสอบต้องใช้เว็บบราวเซอร์ แล้วรอการรับส่งสัญญาณไปในmicrocontroller จะมีไฟกระพริบตลอด 
### การรันโปรแกรม6
   ไปที่โฟลเดอร์ 06 wifi  ซึ่งเป็นโปรแกรมที่ใช้wifi โดยตัวอย่างนี้จะสร้างwifi ขึ้นมาเอง โดยให้ตั้งชื่อwifi กับพาสเวิร์ด เตรียมเว็บเซิร์ฟเวอร์ไว้1 ตัว จากนั้นก็รันโปรแกรม โดยการอัพโหลดไปที่microcontroller รอการcomplyเพื่ออัพโหลดไปยังmicrocontroller เพื่อให้เว็บเซิร์ฟเวอร์start จากนั้นก็ทดสอบwifi

