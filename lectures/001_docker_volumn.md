## Docker Volumn 
container ถูกออกแบบมาให้ใช้งานได้ชั่วคราว มักจะถูกลบออกเมื่อหยุดการทำงาน และข้อมูลที่เก็บไว้ด้านในจะหายไปด้วย เช่น ถ้าเราเปิด container database mysql ไว้ ถ้าหาก container นี้ถูกลบออก ข้อมูลข้างในที่เราควรเก็บไว้ในฐานข้อมูลก็จะหายไปด้วย

**docker volumn** เกิดขึ้นมาเพื่อจัดเก็บข้อมูลถาวรให้กับ container โดยเราสามารถสั่งให้ container เชื่อต่อมาให้ volumn ได้

## ตัวอย่างคำสั่ง
    docker run -d --rm -p 8080:80 -v nginx-data:/usr/share/nginx/html --name nginx-test nginx

## ชุดคำสั่ง
### docker volume list
    ดู volume ทั้งหมดในระบบ

    