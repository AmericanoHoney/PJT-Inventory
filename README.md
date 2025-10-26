หากต้องการ clone ใช้คำสั่ง

git clone --recurse-submodules https://github.com/AmericanoHoney/PJT-Inventory.git


# 📦 PJT Inventory System (Fullstack Project)

ระบบจัดการคลังสินค้า **PJT Inventory System**  
ประกอบด้วย **Frontend (Next.js + React + MUI)** และ **Backend (Express + Drizzle + MySQL)**  
ออกแบบมาเพื่อให้สามารถจัดการสต็อกสินค้า รับ–จ่ายสินค้า ตรวจสอบสินค้าคงคลัง และสร้างรายงานสรุปได้แบบครบวงจร  
รองรับการเชื่อมต่อระหว่าง Frontend และ Backend ผ่าน REST API

---

## 🧭 เกี่ยวกับโปรเจกต์นี้

**PJT Inventory System** คือระบบจัดการคลังสินค้า ที่พัฒนาขึ้นเพื่อช่วยให้ร้านค้าและองค์กรขนาดเล็ก–กลาง  
สามารถจัดการข้อมูลสินค้าได้อย่างมีประสิทธิภาพ ลดการซ้ำซ้อน และเพิ่มความโปร่งใสในการบริหารคลังสินค้า  

ระบบนี้แบ่งออกเป็น 2 ส่วนหลักคือ:

| ส่วนระบบ       | เทคโนโลยีหลัก                                                      | หน้าที่ 
|-----------    |----------------                                                   |----------
| **Frontend**  | Next.js 15, React 19, MUI v7, TailwindCSS, Zustand, React Query   | จัดการ UI แสดงผลข้อมูลสินค้า สต็อก การรับ–จ่ายสินค้า และรายงาน |
| **Backend** | Node.js 22, Express.js, TypeScript, Drizzle ORM, MySQL, OAuth2      | จัดการข้อมูลในฐานข้อมูล การยืนยันตัวตน และการสื่อสารกับ Frontend |

---

## 👩‍💻 ทีมพัฒนา

| ชื่อ                        | รหัสนักศึกษา |
|------                     |----------------|
| น.ส. ณัฐรดา หนูจิตร         | 660610757 |
| น.ส. ทิพวรินท์ สีห์วรางกูร     | 660610760 |
| น.ส. ธนพร ตั้งผดุงสุข        | 660610762 |

---

## 🧩 โครงสร้างโปรเจกต์

```bash
PJT-Inventory/
 ├─ frontend/     # Next.js + React + MUI + TailwindCSS (Client)
 ├─ backend/      # Express + Drizzle + MySQL (Server)
 └─ README.md

---

## 🚀 ขั้นตอนการใช้งาน

1️⃣ ติดตั้งเครื่องมือพื้นฐาน

ก่อนเริ่มต้น โปรดตรวจสอบว่ามีเครื่องมือเหล่านี้ติดตั้งแล้ว:
Node.js 22+
pnpm → เปิดใช้งานผ่าน corepack enable
Docker และ Docker Compose


2️⃣ ติดตั้ง Dependencies
เข้าไปที่แต่ละโฟลเดอร์เพื่อติดตั้งแพ็กเกจที่จำเป็น:

cd frontend
pnpm install

cd ../backend
pnpm install


3️⃣ ตั้งค่า Environment Variables
คัดลอกไฟล์ตัวอย่าง .env.example แล้วสร้าง .env ทั้งใน frontend และ backend

cp frontend/.env.example frontend/.env
cp backend/.env.example backend/.env


จากนั้นแก้ไขค่าตามสภาพแวดล้อมของคุณ (URL, Database, OAuth, API endpoint)


4️⃣ รันระบบด้วย Docker Compose (โหมด Production)
ใช้ Docker รันทุกส่วนของระบบใน container เดียวกัน

docker compose up -d

สำหรับ backend ให้รันคำสั่งเพิ่มเติมเพื่อตั้งค่าฐานข้อมูล:

pnpm db:push
pnpm db:seed


5️⃣ รันระบบในโหมดพัฒนา (Local Development)
หากต้องการรันด้วยเครื่องโดยตรงแทน Docker:

▶️ Backend
cd backend
npm run dev

💻 Frontend
cd frontend
npm run dev


เปิดใช้งานได้ที่ http://localhost:3000