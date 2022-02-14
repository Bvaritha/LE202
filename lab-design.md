# Sensor ตรวจจับควัน โดยใช้ Arduino
## วัตถุประสงค์
1. ศึกษาพื้นฐานของไมโครคอนโทรเลอร์โดยนำมาประยุกต์ใช้ในงานต่างๆ
2. ศึกษาระบบคำสั่งของไมโครคอนโทรเลอร์ที่ใช้ตรวจจับควัน
3. ศึกษาการเชื่อมต่อไมโครคอนโทรเลอร์กับอุปกรณ์ต่างๆ
## อุปกรณ์
1. บอร์ด Arduino UNO R3 
2. Sensor MQ2
3. LED 3 ตัว (สีเขียว,สีเหลือง,สีแดง)
4. ตัวต้านทาน 3 ตัว
5. สาย USB
## ศึกษาข้อมูลเบื้องต้น
> - https://en.wikipedia.org/wiki/Smoke_detector
> - https://www.vivint.com/resources/article/how-do-smoke-detectors-work
> - https://www.cybertice.com/article/196/%E0%B8%AA%E0%B8%AD%E0%B8%99%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99-arduino-%E0%B9%80%E0%B8%8B%E0%B9%87%E0%B8%99%E0%B9%80%E0%B8%8B%E0%B8%AD%E0%B8%A3%E0%B9%8C%E0%B8%95%E0%B8%A3%E0%B8%A7%E0%B8%88%E0%B8%88%E0%B8%B1%E0%B8%9A%E0%B8%84%E0%B8%A7%E0%B8%B1%E0%B8%99-mq2-lpg-co-smoke-gas-sensor
## วิธีทำ 
1. Arduino uno r3 ต่อเข้ากับ หลอดไฟ LED โดยขา13ของ 
- Arduino เชื่อมกับ LED1
2. Arduino uno r3 ต่อเข้ากับเซ็นเซอร์ตรวจจับควัน MQ2
- A5 -> A0, 5V -> Vcc, GND -> GND
3. จากนั้นให้ต่ออุปกรณ์ตามข้อ 1,2  แล้วอัพโหลดโค้ดตัวอย่างด้านล่างลง Arduino uno r3 โค้ดนี้จะอ่านค่า Analog จา่ก เซ็นเซอร์ตรวจจับควัน MQ2 มาใช้งาน
```int ledPin = 13;
int analogPin = 5; //ประกาศตัวแปร ให้ analogPin แทนขา analog ขาที่5
int val = 0;
void setup() {
  pinMode(ledPin, OUTPUT);  // sets the pin as output
  Serial.begin(9600);
}

void loop() {
  val = analogRead(analogPin);  //อ่านค่าสัญญาณ analog ขา5
  Serial.print("val = "); // พิมพ์ข้อมความส่งเข้าคอมพิวเตอร์ "val = "
  Serial.println(val); // พิมพ์ค่าของตัวแปร val
  if (val > 500) { // สามารถกำหนดปรับค่าได้ตามสถานที่ต่างๆ
    digitalWrite(ledPin, HIGH); // สั่งให้ LED ติดสว่าง
  }
  else {
    digitalWrite(ledPin, LOW); // สั่งให้ LED ดับ
  }
  delay(100);
}
```
4. เปิด Serial Monitor ขึ้นมาเพื่อดูค่าสัญญาณ Analog ที่เซ็นเซอร์ตรวจจับควัน MQ2 ส่งให้ Arduino จะเห็นว่าถ้าเซ็นเซอร์ตรวจจับควัน MQ2 ยัง ไม่โดนควันค่าจะน้อยกว่า 500 ไฟ LED ยังไม่ติด
5. ถ้าเราจุดกํายานแล้วนำไปวางใกล้ๆ เซ็นเซอร์ตรวจจับควัน MQ2 ค่าที่อ่านได้จะสูงขึ้น หลอดไฟ LED จะติด
## 
