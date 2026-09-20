# Slayd Yaratuvchi Telegram Bot

Foydalanuvchi mavzu yozadi → bot AI orqali slayd matnini tayyorlaydi →
`.pptx` fayl qilib yuboradi.

## 1. Nima kerak bo'ladi

- **BOT_TOKEN** — @BotFather'dan olgan tokeningiz
- **GEMINI_API_KEY** — Google AI Studio'dan (aistudio.google.com) olinadigan
  API kalit. Bepul tarifda kuniga cheklangan so'rov soni bilan foydalanish mumkin.

Bu ikkalasini ham kodning ichiga yozmang — ular **environment o'zgaruvchi**
sifatida beriladi (pastda ko'rsatilgan).

## 2. Render.com orqali joylashtirish (bepul, kartasiz)

1. **GitHub'da hisob oching** (agar yo'q bo'lsa).
2. Shu papkadagi fayllarni (`main.py`, `requirements.txt`) GitHub
   repositoriyasiga yuklang.
3. **Render.com**'da hisob oching (GitHub akkaunt bilan kirish mumkin).
4. Dashboard'da **"New +" → "Web Service"** ni tanlang (Background Worker EMAS —
   u kartasiz ishlamaydi).
5. GitHub repositoriyangizni ulang va tanlang.
6. Sozlamalar:
   - **Runtime**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python main.py`
   - **Instance Type**: Free
7. **"Environment"** bo'limiga o'ting, quyidagilarni qo'shing:
   - `BOT_TOKEN` = sizning bot tokeningiz
   - `GEMINI_API_KEY` = sizning Gemini API kalitingiz
8. **"Create Web Service"** tugmasini bosing — deploy boshlanadi (bir necha daqiqa vaqt oladi).

## 3. Test qilish

Deploy tugagach (loglar oxirida "Bot ishlayapti" yoki shunga o'xshash xabar
ko'rinadi), Telegram'da botingizni oching, `/start` bosing, mavzu yozing —
bir necha soniyadan so'ng `.pptx` fayl kelishi kerak.

## 4. Muhim eslatma (bepul tarif haqida)

Render'ning bepul "Web Service" tarifi, agar 15 daqiqa hech kim murojaat
qilmasa, xizmatni "uxlatib qo'yishi" mumkin. Birinchi xabar kelganda qayta
uyg'onadi, bu bir necha soniya kechikish keltirib chiqarishi mumkin — bu
normal holat.

## 5. Keyingi qadamlar (keyinroq qo'shamiz)

- Telegram Mini App (chiroyli interfeys)
- Valyuta/kredit tizimi (har bir generatsiya uchun tanga sarflash)
- To'lov tizimi (Telegram Stars yoki Click/Payme)
- Slayd sonini tanlash, tilni tanlash, shablon tanlash
