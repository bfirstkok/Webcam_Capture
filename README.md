# Webcam Capture

เว็บเพจระบบ Static สำหรับเปิดกล้องเว็บแคมบนเบราว์เซอร์ และ “แคปภาพ” เป็น Snapshot แบบเรียลไทม์ โดยใช้ `MediaDevices API` (ไม่ต้องมี Backend)

## Features
- ขอสิทธิ์การเข้าถึงกล้อง และแสดงภาพสด (Live video)
- กด Capture เพื่อดึงเฟรมปัจจุบันไปแสดงบน Canvas/รูปภาพ
- ใช้งานได้แบบไฟล์ HTML เดี่ยว ๆ (Static)

## Requirements
- เบราว์เซอร์สมัยใหม่: Chrome / Edge / Firefox (แนะนำเวอร์ชันล่าสุด)
- ต้องอนุญาต Permission กล้องเมื่อเบราว์เซอร์ถาม

## How to use
1. เปิดไฟล์ `webcam.html` ด้วยเบราว์เซอร์
2. กด Allow/อนุญาตการเข้าถึงกล้อง
3. ใช้ปุ่ม/คอนโทรลบนหน้าเว็บเพื่อ Capture รูป

## Important Notes (HTTPS)
เบราว์เซอร์ส่วนใหญ่ “ต้องใช้ HTTPS” เพื่อเข้าถึงกล้อง:
- ถ้าเปิดแบบ `file://` อาจโดนบล็อก
- แนะนำให้รันผ่าน Local server หรือ Deploy ขึ้น HTTPS (เช่น GitHub Pages)

## Run with a Local Server (แนะนำ)
ตัวอย่างวิธีรันแบบง่าย ๆ:

### Python
```bash
# Python 3
python -m http.server 8000
```
แล้วเปิด:
- `http://localhost:8000/webcam.html`

### Node.js (http-server)
```bash
npx http-server . -p 8000
```

## Deploy on GitHub Pages
1. ไปที่ Repo Settings → Pages
2. เลือก Branch: `main` และโฟลเดอร์ root (/) (หรือค่าที่คุณใช้)
3. เปิด URL ของ GitHub Pages แล้วเข้าหน้า `webcam.html` เช่น:
- `https://<username>.github.io/<repo>/webcam.html`

## Troubleshooting
- **กล้องไม่ขึ้น / Permission ไม่เด้ง**: เช็คว่าใช้ HTTPS หรือ `localhost` และไม่ปิด Permission ไว้ใน Browser settings
- **มีหลายกล้อง**: อาจต้องเลือกอุปกรณ์จากการตั้งค่าเบราว์เซอร์/ระบบ
- **หน้าเว็บไม่โหลดกล้องบน Safari**: อาจมีข้อจำกัดเพิ่มเติม แนะนำทดสอบ Chrome/Edge ก่อน

## License
Provided as-is by the repository owner.  
(ถ้าต้องการแจกจ่าย/ใช้งานจริงจัง แนะนำเพิ่มไฟล์ LICENSE)
