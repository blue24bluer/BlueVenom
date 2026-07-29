

# ☣️ BlueVenom C2 & Payload Generator 

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0.0-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/Python-3.8%2B-green.svg" alt="Python">
  <img src="https://img.shields.io/badge/Platform-Cross--Platform-lightgrey.svg" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-orange.svg" alt="License">
</p>

**BlueVenom** هو إطار عمل متقدم للقيادة والتحكم (Command & Control - C2) ومولد حمولات (Payload Generator) عابر للمنصات. يدمج النظام بين الذكاء الاصطناعي، التشفير الديناميكي (FUD)، وشبكات الند للند (P2P) لبناء وإدارة شبكات البوت نت (Botnets) بطريقة ذكية ولا مركزية.

---

## ⚠️ إخلاء مسؤولية (Disclaimer)
> **تنبيه هام:** تم تطوير هذا المشروع **للأغراض التعليمية، أبحاث الأمان السيبراني، واختبار الاختراق الأخلاقي (Red Teaming) فقط**. المطوّر غير مسؤول عن أي استخدام غير قانوني أو ضار لهذا النظام. استخدامك لهذا الكود يعني موافقتك على تحمل المسؤولية الكاملة عن أفعالك.

---

## ✨ المميزات الرئيسية (Key Features)

### 🦠 1. مولد وحاقن الحمولات (Multi-Platform Payload Engine)
* **Android (APK):** حقن الحمولات الخبيثة داخل تطبيقات أندرويد الشرعية (Smali Injection)، مع دعم توقيع `V1/V2/V3` لتخطي حماية `Play Protect` وتحسين هيكلة الملف عبر `Zipalign`.
* **Windows (EXE):** بناء ملفات تنفيذية أصلية بصمت (Stealth Native). يتضمن ميزات مثل: متصفح وهمي (Webview)، Keylogger مدمج، رسائل خطأ وهمية (Dialogs)، ودمج الملفات (SFX Binder).
* **Linux / Termux:** بناء ملفات ELF مع تقنيات بقاء (Persistence) عبر `Crontab` و `Bashrc`، سكربت `Fake Sudo` لاصطياد كلمات مرور الـ Root، وتخطي إغلاق الشاشة (Wakelock).

### 🌐 2. شبكة الإتصال المتقدمة (BlueNet & C2 Comms)
* **TCP Reverse Shell:** اتصالات خام ومدارة مباشرة للتحكم الفوري.
* **HTTP/HTTPS Polling:** اتصال متخفي عبر بروتوكولات الويب.
* **UDP Streaming:** بث حي وسريع للوسائط (كاميرا أمامية/خلفية، أو مشاركة الشاشة).
* **BlueNet (P2P Switch):** راوتر افتراضي مدمج يتيح اتصال البوتات ببعضها البعض (Bot-to-Bot Routing) وتخطي الجدران النارية بدون الحاجة لصلاحيات Root.

### 🧠 3. محرك الذكاء الاصطناعي (AI Integration)
* **تحويل الثغرات تلقائياً (Auto-Weaponization):** ربط مع `BlueBot AI` لقراءة وصف ثغرات `CVE` أو روابط الـ Exploits من جيت هاب، وتحويلها تلقائياً إلى أكواد بايثون هجومية (Silent Payloads/Scanners).
* **التفكير العميق (Think Mode):** تحليل ذكي لهيكل النظام المستهدف واتخاذ قرارات مستقلة للهجوم.

### 🛡️ 4. التشفير والتخطي (FUD & Evasion)
* التكامل مع محرك **BlueCode** لتشويش الأكواد (Obfuscation) بطبقات تشفير متعددة قبل عملية البناء (Compilation).
* استنساخ الشهادات الرقمية (Certificate Cloning) لتخطي حماية `SmartScreen` في ويندوز.

### ⚙️ 5. التجميع المتبادل (Cross-Compilation)
* بناء ملفات `Windows EXE` من أنظمة `Linux/Termux` باستخدام بيئة **WINE**.
* بناء ملفات `Linux ELF` من أنظمة `Windows` باستخدام **WSL**.

---

## 🛠️ المتطلبات (Prerequisites)

يعتمد السكربت على تثبيت الاعتماديات المفقودة تلقائياً (Auto-Dependency Installer)، ولكن يتطلب النظام بعض الأدوات الأساسية في بيئة العمل:

* **Python 3.8+**
* **أدوات أندرويد (اختياري لبناء الـ APK):** `Java`, `Apktool`, `Zipalign`, `Apksigner`.
* **أدوات البناء المتبادل (اختياري):** `WINE` (للينكس/تيرمكس)، `WSL` (للويندوز).

**المكتبات الأساسية (يقوم السكربت بتثبيتها تلقائياً):**
`flask`, `werkzeug`, `pycryptodome`, `pywebview`, `keyboard`, `requests`, `pyinstaller`, `filetype`

---

## 🚀 التثبيت والتشغيل (Installation & Usage)

1. قم باستنساخ المستودع (Clone the repository):
   ```bash
   git clone https://github.com/Username/BlueVenom.git
   cd BlueVenom
   ```

2. قم بتشغيل السكربت الأساسي (سيقوم بفحص وتثبيت المكتبات المفقودة وإنشاء قواعد البيانات الأولية):
   ```bash
   python bluevenom.py
   ```

3. **الوصول إلى لوحة التحكم:**
   بمجرد تشغيل السيرفر، ستظهر واجهة الويب (C2 Panel) على الرابط المحلي:
   ```text
   http://127.0.0.1:2424
   ```
   *(أو عبر الـ IP الخاص بالشبكة المحلية للاستخدام الخارجي).*

---

## 📂 هيكلة المشروع (Project Structure)

يعتمد BlueVenom على هيكلة منظمة للفصل بين الحمولات، الأدوات، والسجلات:

```text
BlueVenom/
├── admin_scripts/          # سكربتات التحكم وأوامر المسؤول (Server-side attacks)
├── BlueDroid/              # أدوات حقن وهندسة الأندرويد (APK)
│   ├── payload/            # قوالب الحمولات (Java/Smali)
│   └── tools/              # (Apktool, Zipalign, Apksigner, android.jar)
├── bot_uploads/            # الملفات والصور المسحوبة من أجهزة الضحايا
├── files_upload/           # السكربتات المجهزة للإرسال (Victim scripts)
├── injected_logs/          # سجلات عمليات الحقن والبناء
├── locales/                # ملفات الترجمة (دعم الواجهة متعددة اللغات)
├── successful_injections/  # المخرجات النهائية (EXE, APK, ELF)
├── attacks.json            # قاعدة بيانات الهجمات المخصصة
├── bot_info.json           # قاعدة بيانات الأجهزة المتصلة
├── c2_events.json          # سجل البث المباشر للأحداث (Live Feed)
└── cves_db.json            # قاعدة بيانات ثغرات CVE المولدة بالذكاء الاصطناعي
```

---

## 💻 التفاعل مع واجهة برمجة التطبيقات (API Overview)

يحتوي BlueVenom على واجهة API متكاملة للتحكم الخارجي والتكامل مع روبوتات أخرى (مثل BlueRever):

* `POST /api/c2/perform_injection` : لبدء عملية بناء وحقن حمولة جديدة.
* `POST /api/c2/heartbeat` : نبض البوتات (Heartbeat) لسحب الأوامر.
* `POST /api/c2/result/<bot_id>/<command_id>` : استقبال نتائج الأوامر من البوتات.
* `GET /api/c2/bots_status` : جلب حالة البوتات المتصلة حالياً.
* `POST /api/c2/bot_to_bot` : توجيه أمر من بوت إلى آخر عبر شبكة P2P.
* `POST /api/c2/execute_attack` : شن هجوم AST متقدم (Server-side & Client-side).

---

## 🤝 المساهمة (Contributing)
نرحب بالمساهمين! إذا كان لديك إضافات (مثل قوالب FUD جديدة، تحسين استغلالات CVE، أو دعم لمنصات أخرى)، يرجى فتح `Pull Request`. يرجى التأكد من التوثيق المناسب لأي كود جديد.

---

## 📜 الترخيص (License)
هذا المشروع مرخص بموجب رخصة **MIT**. راجع ملف `LICENSE` لمزيد من التفاصيل.

---
*Developed with 🧠 by [@blue24bluer]*
