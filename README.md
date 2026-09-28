# 🚗 ระบบเว็บไซต์ One Stop Service ยานพาหนะราชการ
### ฝ่ายพัฒนาชุมชนและสวัสดิการสังคม สำนักงานเขตคลองเตย

เว็บไซต์นี้เป็นระบบ Frontend แบบ Standalone (Single Page Application) สำหรับการบริหารจัดการคิวและยานพาหนะราชการ เชื่อมต่อระบบฐานข้อมูล Google Sheets และระบบแจ้งเตือน LINE Official Account ผ่าน Google Apps Script API

---

## 📁 ไฟล์ในโฟลเดอร์นี้

1. **`index.html`** — โค้ดหน้าเว็บทั้งหมด (HTML5, Tailwind CSS, FontAwesome, JavaScript Single Page Application)
2. **`.nojekyll`** — ไฟล์คอนฟิกสำหรับ GitHub Pages เพื่อป้องกันไม่ให้ระบบ Jekyll มองข้ามไฟล์
3. **`README.md`** — คู่มือการติดตั้งและการใช้งาน

---

## 🚀 ขั้นตอนการนำไฟล์ขึ้น GitHub Pages (Step-by-Step)

### ขั้นที่ 1: สร้างคลังเก็บโค้ด (Repository) บน GitHub
1. เปิดเว็บไซต์ [GitHub.com](https://github.com/) และล็อกอินเข้าสู่บัญชีของคุณ
2. คลิกปุ่ม **New** (หรือเครื่องหมาย `+` ด้านขวาบน แล้วเลือก **New repository**)
3. ตั้งชื่อ Repository เช่น: `klongtoei-car-service` หรือ `car-service`
4. เลือกระดับการเข้าถึง: **Public** (สาธารณะ เพื่อเปิดใช้งาน GitHub Pages ฟรี)
5. ไม่ต้องติ๊กเลือก Add a README file (เพราะเรามีไฟล์เตรียมไว้แล้ว)
6. คลิกปุ่มสีเขียว **Create repository**

---

### ขั้นที่ 2: อัปโหลดไฟล์ขึ้น GitHub
มีให้เลือก 2 วิธีตามความสะดวก:

#### วิธีที่ ก: ลากและวางผ่านหน้าเว็บ GitHub (ง่ายและเร็วที่สุด)
1. ในหน้า Repository ที่เพิ่งสร้าง ให้คลิกลิงก์ **"uploading an existing file"**
2. ลากไฟล์ทั้ง 3 ไฟล์จากโฟลเดอร์นี้:
   - `index.html`
   - `.nojekyll`
   - `README.md`
   มาวางลงในช่องอัปโหลดบนหน้าเว็บ GitHub
3. ด้านล่างในช่อง Commit changes พิมพ์ว่า `Initial commit` แล้วกดปุ่มสีเขียว **Commit changes**

#### วิธีที่ ข: อัปโหลดผ่าน Git Command Line
```bash
git init
git add .
git commit -m "Initial release v1.0"
git branch -M main
git remote add origin https://github.com/<ชื่อผู้ใช้ GitHub>/<ชื่อ Repository>.git
git push -u origin main
```

---

### ขั้นที่ 3: เปิดใช้งาน GitHub Pages
1. ไปที่เมนู **Settings** (รูปฟันเฟือง) ด้านบนของหน้า Repository
2. เลื่อนเมนูด้านซ้ายลงมา คลิกที่หัวข้อ **Pages**
3. ในส่วน **Build and deployment**:
   - Source: เลือก **Deploy from a branch**
   - Branch: เลือก **main** และโฟลเดอร์เป็น **/ (root)**
4. คลิกปุ่ม **Save**
5. รอระบบ GitHub ประมวลผลประมาณ 1-2 นาที คุณจะได้ URL เว็บไซต์ เช่น:
   ```
   https://<ชื่อผู้ใช้ GitHub>.github.io/<ชื่อ Repository>/
   ```

---

## 🔗 โครงสร้างลิงก์สำหรับเชื่อมต่อกับ Rich Menu ใน LINE OA

เมื่อได้ URL เว็บไซต์แล้ว สามารถนำไปต่อท้ายเพื่อเปิดไปยังหน้าที่ต้องการได้ทันที:

| เมนูที่ต้องการเปิด | URL Parameter | ตัวอย่าง URL ฉบับสมบูรณ์ |
| :--- | :--- | :--- |
| **ขอใช้รถ (ในฝ่าย)** | `?page=request` | `https://<user>.github.io/<repo>/?page=request` |
| **ยืมรถ (9 ฝ่าย)** | `?page=borrow` | `https://<user>.github.io/<repo>/?page=borrow` |
| **คำขอของฉัน** | `?page=my_requests` | `https://<user>.github.io/<repo>/?page=my_requests` |
| **ตารางคิวรถประจำวัน** | `?page=queue` | `https://<user>.github.io/<repo>/?page=queue` |
| **Admin Dashboard** | `?page=admin_dashboard` | `https://<user>.github.io/<repo>/?page=admin_dashboard` |
| **Admin Login (บนคอม)** | `?page=admin_login` | `https://<user>.github.io/<repo>/?page=admin_login` |
| **บันทึกไมล์ (แบบ 4)** | `?page=mileage` | `https://<user>.github.io/<repo>/?page=mileage` |
| **บันทึกเติมน้ำมัน** | `?page=fuel` | `https://<user>.github.io/<repo>/?page=fuel` |
| **แจ้งซ่อมบำรุง** | `?page=repair` | `https://<user>.github.io/<repo>/?page=repair` |
| **ทำเนียบ พขร.** | `?page=roster` | `https://<user>.github.io/<repo>/?page=roster` |
| **ลงทะเบียนสมาชิก** | `?page=register` | `https://<user>.github.io/<repo>/?page=register` |

---

## 🛡️ ความปลอดภัยของระบบ (Security Model)

- **ไม่มีรหัสลับใน GitHub:** หน้าเว็บ `index.html` ไม่มี Google Sheet ID, ไม่มี LINE Token, และไม่มีกุญแจสำคัญใดๆ
- **ระบบหลังบ้านแยกเด็ดขาด:** ข้อมูลทั้งหมดประมวลผลผ่าน Google Apps Script (GAS) API Server-side
- **การล็อกอิน Admin:** ป้องกันด้วยรหัส PIN 6 หลัก และการตรวจสอบ LINE User ID ที่ได้รับอนุญาต พร้อมระบบ Session Token อายุ 12 ชั่วโมง
- **การเชื่อมต่อ API:** ส่งคำขอแบบ POST ด้วย Text/Plain เพื่อรองรับ Cross-Origin Request โดยไม่ต้องผ่านกระบวนการ Preflight OPTIONS
