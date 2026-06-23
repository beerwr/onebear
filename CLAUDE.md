# Onebear Project

Multi-product project. See subfolder CLAUDE.md files for product-specific instructions.

## Structure

```
design-system/   ← Brand-level design spec (shared across all products)
landing/         ← Landing page (onebear.ai) — main product
```

## Design System (`design-system/`)

แหล่งความจริงเดียวของ brand Onebear — ใช้ร่วมกันทุก product

| ไฟล์ | เนื้อหา |
|---|---|
| `01_Colors.md` | สี token ทั้งหมด (hex, CSS var) |
| `02_Typography.md` | ฟอนต์ Gofive + ขนาด/weight |
| `03_Spacing.md` | spacing scale |
| `04_Buttons.md` | ปุ่มทุก variant + กฎ sizing |
| `05_Brand-Assets.md` | logo, mascot, usage rules |
| `06_Icons.md` | icon system |
| `07_Web-Patterns.md` | section patterns + Layout Rules (R1–R4) |
| `08_Landing-v3.md` | snapshot ของ landing v3.1 |
| `fonts/` | TTF master fonts (source — อย่า deploy โดยตรง) |
| `assets/` | master images/logos (source — อย่า deploy โดยตรง) |

**กฎ: ก่อนแก้ UI ทุกครั้งในทุก product เปิดไฟล์ที่เกี่ยวข้องก่อนเสมอ**

### วิธีใช้ Design System

- **อ่าน spec** → เปิดไฟล์ `.md` ที่เกี่ยวข้องก่อนแก้ UI
- **สร้าง web assets** → รัน `sync-assets.py` ใน product folder (แปลง TTF → woff2, copy images)
- **อย่าแก้ไฟล์ใน `landing/assets/` หรือ `landing/fonts/` โดยตรง** — generated files เสมอ

## Git workflow

Working branch: `feat/next` → PR → `main`  
ห้าม commit ตรงไปที่ `main`
