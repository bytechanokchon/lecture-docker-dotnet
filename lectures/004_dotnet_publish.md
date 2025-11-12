## Dotnet publish
โดยปกติการนำ dotnet application ไปใช้งาน จะต้องแปรงเป็น binary ก่อน

## คำสั่ง
### dotnet publish
    แปรงชุดคำสั่ง C# ให้อยู่ในรูปแบบ binary
    ตัวอย่าง
        dotnet publish .\hello-docker.csproj -o published

โดยเมื่อชุดคำสั่งถูกรันแล้ว จะได้ไฟล์ทั้งหมดที่จำเป็นต่อการทำงานของแอพพลิเคชัน และสามารถเข้าใช้งานได้ผ่าน .exe (ถ้าใช้ docker ไม่จำเป็นต้องใช้)

โดยหากเราต้องการไฟล์ binary ที่ไม่ต้อง compile โดยอิงจากระบบปฏิบัติการที่่ใช้อยู่ เราสามารถใช้คำสั่งได้ดังนี้

    dotnet publish .\hello-docker.csproj -o published /p:UseAppHost=false

*ENTRYPOINT เป็นคำสั่งที่ container จะเรียกใช้งานทุกครั้งที่่เริ่มทำงาน*