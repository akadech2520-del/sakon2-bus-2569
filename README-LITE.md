# ชุด Lite สำหรับ Google Apps Script + Google Sheets

ชุดนี้ตัดไฟล์รูปภาพฝัง `HeaderImage.html` และ `AppAssets.html` ออก เพื่อให้ Apps Script บันทึกและ Deploy ได้ง่ายขึ้น

## ไฟล์ที่ต้องสร้างใน Apps Script

ให้สร้างไฟล์ตามนี้เท่านั้น:

- `Code.gs`
- HTML ชื่อ `Index` แล้ววางเนื้อหาจาก `Index.html`
- HTML ชื่อ `Admin` แล้ววางเนื้อหาจาก `Admin.html`
- HTML ชื่อ `CSS` แล้ววางเนื้อหาจาก `CSS.html`
- HTML ชื่อ `JavaScript` แล้ววางเนื้อหาจาก `JavaScript.html`

ไม่ต้องสร้าง `HeaderImage` และ `AppAssets` ในชุด Lite

## ถ้าเปิด Apps Script จาก Google Sheets

1. เปิด Google Sheet
2. ไปที่ `ส่วนขยาย > Apps Script`
3. วางไฟล์ให้ครบ
4. เลือกฟังก์ชัน `setupWorkbook`
5. กด `Run`
6. Deploy เป็น Web app

## ถ้าใช้ Apps Script แบบไม่ได้เปิดจาก Google Sheet

1. สร้าง Google Sheet แล้วคัดลอก Spreadsheet ID จาก URL
2. เปิด `Code.gs`
3. แก้บรรทัดแรกจาก

`const SPREADSHEET_ID_OVERRIDE = '';`

เป็น

`const SPREADSHEET_ID_OVERRIDE = 'ใส่ Spreadsheet ID ที่นี่';`

4. บันทึกไฟล์
5. เลือกฟังก์ชัน `setupWorkbook` แล้วกด `Run`

## ตรวจการติดตั้ง

หลัง Deploy เปิด:

`.../exec?check=1`

ถ้าขึ้นว่า `Index`, `Admin`, `CSS`, `JavaScript` พบไฟล์ครบ แปลว่าติดตั้งไฟล์ถูกต้อง

## หลังแก้ไฟล์ทุกครั้ง

ต้องไปที่:

`Deploy > Manage deployments > Edit > Version: New version > Deploy`
