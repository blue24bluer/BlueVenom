# 🐍 BlueVenom C2 Framework

<div align="center">
  <pre>

    888~~\  888                    Y88b      /                                           
    888   | 888 888  888  e88~~8e   Y88b    /   e88~~8e  888-~88e  e88~-_  888-~88e-~88e 
    888 _/  888 888  888 d888  88b   Y88b  /   d888  88b 888  888 d888   i 888  888  888 
    888  \  888 888  888 8888__888    Y888/    8888__888 888  888 8888   | 888  888  888 
    888   | 888 888  888 Y888    ,     Y8/     Y888    , 888  888 Y888   ' 888  888  888 
    888__/  888 "88_-888  "88___/       Y       "88___/  888  888  "88_-~  888  888  888 
                                                                                     
  </pre>
  <b>Advanced Command & Control Dashboard</b>
  <br>
  <i>Developed by @blue24bluer</i>
</div>

---

## 📋 Overview (نبذة عامة)
**BlueVenom** is an advanced Command & Control (C2) framework featuring an interactive web dashboard for managing bots across Android, Windows, and Linux. It features a flexible "Bubbles" system that converts raw scripts into GUI tools dynamically, along with advanced injection capabilities.
<br>(هو إطار عمل متقدم للتحكم والسيطرة يوفر واجهة ويب لإدارة البوتات، ويتميز بنظام "الفقاعات" لتحويل السكربتات إلى أدوات رسومية، بالإضافة إلى قدرات الحقن).

---

## ✨ Key Features (المميزات الرئيسية)
- **🖥️ Centralized Web Dashboard:** Modern Dark Mode UI for full operation management. (واجهة تحكم مركزية عصرية).
- **💉 Multi-Injection System:** Support for Android (APK), Python, and Bash injection. (نظام حقن متعدد الصيغ).
- **🔮 Magic Bubbles:** Create custom control tools dynamically without coding the UI. (نظام الفقاعات لإنشاء أدوات مخصصة).
- **📡 TCP Listener:** Built-in raw shell listener. (مستمع مدمج للاتصالات العكسية).
- **📂 File Manager:** Upload, edit, and manage scripts/payloads directly. (مدير ملفات للتحكم بالسكربتات).
- **📊 Live Event Feed:** Real-time logging of commands and results. (سجل أحداث فوري).

---

## 🚀 Installation & Usage (التثبيت والتشغيل)

### Requirements (المتطلبات)
Ensure necessary libraries are installed:
```bash
pip install flask requests werkzeug
```
*(For Android Injector, Java and zipalign must be installed on the host machine - لأداة حقن الأندرويد يجب توفر الجافا)*

### Running the C2 (التشغيل)
```bash
python app.py --bluevenom
```
Or via the standalone version:
```bash
python BlueVenom_Standalone.py
```
Default Port: `2424` or `5000`.

---

## 🔮 Magic Bubbles System (نظام الفقاعات السحرية)

The most powerful feature in BlueVenom is transforming any Python script into a GUI control bubble.
(أقوى ميزة هي تحويل أي سكربت بايثون إلى زر تحكم في الواجهة).

### How to create a Bubble (كيفية الإنشاء):
1. Go to **"Scripts & Tools"** section (قسم الأدوات والسكربتات).
2. Upload your script (e.g., `stealer.py`).
3. Click the **"Magic Wand"** icon 🪄 next to the script.
4. Fill in the details: Title, Category, and Arguments.

### 🧠 Magic Keywords (الكلمات السحرية)
Use these special values in the **Arguments** field to make your commands dynamic:
(استخدم هذه القيم الخاصة في حقل المدخلات لجعل الأوامر ديناميكية):

| Keyword (الكلمة) | Description (الوصف) | Example (مثال) | Result (النتيجة) |
| :--- | :--- | :--- | :--- |
| **`{{variable}}`** | Creates an input field for the user to fill. (إنشاء حقل إدخال للمستخدم) | `--target {{ip}}` | User sees a text box for IP. |
| **`%no%`** | Sends the **Flag** only, without a value. (إرسال العلم فقط بدون قيمة) | `--verbose` (Value: `%no%`) | Sends `--verbose` only. |
| **`%null%`** | Completely ignores/removes the parameter. (تجاهل البراميتر تماماً) | `--option` (Value: `%null%`) | Nothing is sent. |
| **`%server%`** | Auto-replaced with current C2 URL. (استبدال تلقائي برابط السيرفر) | `--url` (Value: `%server%`) | `--url http://127.0.0.1:port` |
| **`%time%`** | Auto-replaced with Unix Timestamp. (استبدال بالطابع الزمني) | `--out log_%time%.txt` | `--out log_17345678.txt` |

---

## 💉 Injection System (نظام الحقن)

BlueVenom provides an integrated injection environment:
(يوفر بيئة حقن متكاملة):

1. **Android (APK):**
   - Automatic payload injection into legitimate APK files. (حقن تلقائي في تطبيقات أندرويد).
   - Supports custom Java payloads. (يدعم حمولات جافا مخصصة).
   - Tools required: `Apktool`, `Jarsigner`, `Zipalign`.

2. **Python/Bash:**
   - Embeds reverse shell logic into scripts with obfuscation. (دمج كود الاتصال العكسي مع التشفير).

---

## 🤖 Bot Management (إدارة البوتات)

- **Bot ID:** Unique identifier for each infected device. (معرف فريد لكل جهاز).
- **Last Seen:** UTC-synchronized connection status. (حالة الاتصال بتوقيت عالمي موحد).
- **Actions (الإجراءات):**
  - **Execute:** Send direct Shell commands. (إرسال أوامر مباشرة).
  - **Bubbles:** Use your created magic bubbles. (استخدام الفقاعات المخصصة).
  - **File Transfer:** Send/Receive files to/from the victim. (نقل الملفات من وإلى الضحية).

---

## ⚠️ Disclaimer (إخلاء مسؤولية)

**BlueVenom** is developed for **educational purposes and authorized penetration testing only**.
(تم تطويره للأغراض التعليمية واختبارات الاختراق المصرح بها فقط).

- The developer **@blue24bluer** is not responsible for any misuse or illegal activities. (المطور غير مسؤول عن أي سوء استخدام).
- Using this tool against systems you do not own or have permission to test is illegal. (استخدام الأداة ضد أنظمة لا تملك تصريحاً لها يعد غير قانوني).

---

<div align="center">
  <b>BlueVenom v5.0</b> - <i>The Future of C2 Management</i>
</div>
