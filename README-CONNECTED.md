# ระบบบริหารจัดการผู้เข้าร่วม - รุ่นเชื่อม Google Sheet จริง

## ใช้งานผ่าน GitHub Pages

1. เปิด Settings > Pages และเลือก Deploy from a branch: `main` / `(root)`
2. นำ `Code.gs` และ `appsscript.json` ไปวางใน Google Apps Script
3. รัน `setupWorkbook` หนึ่งครั้ง แล้ว Deploy เป็น Web app โดย Execute as: Me
4. คัดลอก URL ที่ลงท้าย `/exec` ไปใส่ใน `config.js`
5. เปิด `https://akadech2520-del.github.io/sakon2-bus-2569/`

ตั้ง API ครั้งแรกโดยไม่แก้ไฟล์ได้ด้วย URL รูปแบบ `?api=WEB_APP_URL` ระบบจะจำค่าไว้ในเบราว์เซอร์

ชุดนี้ตั้งค่าให้เชื่อมกับ Spreadsheet ID:

`1kVJAv4H_wVeWYERUc0jT70WPjwHt1MizcwTYbExws4o`

ไฟล์ที่ต้องมีใน Google Apps Script:

- `Code.gs`
- `Index.html`
- `Admin.html`
- `CSS.html`
- `JavaScript.html`
- `HeaderImage.html`
- `AppAssets.html`
- `appsscript.json`

หลังวางไฟล์แล้วให้ทดสอบตามลำดับ:

1. เปิด Apps Script แล้วกด Run ฟังก์ชัน `setupWorkbook`
2. อนุญาตสิทธิ์ Google Sheet และ Google Drive
3. เปิด Web app URL พร้อม `?check=1` เพื่อตรวจไฟล์ เช่น `/exec?check=1`
4. เปิดหน้าเว็บปกติ `/exec`
5. เปิดหน้า Admin ด้วย `/exec?page=admin`

ถ้ายังเห็นข้อมูลไม่อัปเดต ให้ Deploy > Manage deployments > Edit แล้วเลือก Version ใหม่ จากนั้นกด Deploy อีกครั้ง
