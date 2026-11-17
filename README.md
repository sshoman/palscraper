# palscraper
Free app to get you unlimited leads to sell to تطبيق مجاني للحصول على ارقام وايميلات زبائن جدد

It looks past the normal signals such as company & job title, for interpersonal signals that might affect the approach such as Racial Race, Hometown Politics...etc
Runs with minimal input, controls the browser fully without assistant. Save to scrape 100s of leads a day without guardrails. 

-------------------------------------------------------

5 examples to get you started, that you can use right now يحتوي اربع قوائم جاهزة للاستعمال الان، انظر ملفات الاكسل بالاعلى
(look at the .csv & .xlsx files above)

1. WWFF 2025: 14,000 Startups that raised more than 100k in 2024 worldwide. Divided by region from Middle East, EU, Southeast Asia to South America.
2. Chamber Of Commerce 2026: Updated list of ~5000 companies registered locally. Jan 2026 update.  
3. Bridal EUMA 2025: 1000s of Bridal Shops in Europe and Middle East. You can adjust business type in the app to other types of shops. 
4. Hardware 2025: 1000s of small businesses that sell physical products.
5. New US Q325: Tracking newly registered business in the US Summer 2025.
---

App #1: ## OldScraper25

### English

OldScraper25 is a command-line Google Maps lead scraper. Enter a search such as `dentists in Ramallah` or `hardware stores in Berlin`. The app opens Google Maps in Chrome, visits result pages, and collects the business name, address, website, phone number, available email addresses, and Google Maps link. When an email is not available in the listing, it can check the linked business website.

The app saves the results as a timestamped CSV file and creates a text report with a short sample of the results. It can also save browser cookies and storage in `maps_session.pkl` for later sessions.

#### Setup And Use

Requirements:
- Python 3.9 or newer
- Google Chrome installed
- Internet connection

1. Download `oldscraper25/palscraper.zip` and extract it into the `oldscraper25` folder. You should see `ms.py` and `run.bat` beside `requirements.txt`.
2. Open a terminal in that folder.
3. Create and activate a virtual environment, then install the packages:

Windows PowerShell:
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
```

Linux or macOS:
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

4. Start the app:

Windows:
```powershell
py ms.py
```

Linux or macOS:
```bash
python3 ms.py
```

5. Enter a Google Maps search query when asked. Choose a scraping mode. Mode 1 is the recommended resilient mode, mode 2 runs one standard attempt, and mode 3 uses the legacy flow.

The CSV and report are saved in the folder where the script is running. The CSV columns are name, address, website, phone, emails, and google_link. Email addresses in one cell are separated by semicolons.

#### Notes

- The first run needs an internet connection. WebDriver Manager downloads the matching Chrome driver automatically.
- The Windows `run.bat` launcher requests administrator privileges. Running `py ms.py` directly is usually enough and does not require that elevation.
- The automated Chrome window uses browser automation flags that change some browser security settings. Do not sign in to personal accounts in that window or use it for normal browsing.
- `maps_session.pkl` can contain cookies and browser storage. Keep it private and do not upload or share it.
- Google Maps or a business website may block automated requests or change its page layout. Results are not guaranteed. Stop or wait when a CAPTCHA or access block appears.
- Use the app only where you have permission. Follow Google Maps and website terms, privacy laws, and rules for collecting and using contact details.

### العربية

OldScraper25 هو برنامج يعمل من خلال سطر الأوامر لجمع بيانات الأنشطة التجارية من خرائط Google. اكتب عبارة بحث مثل `أطباء أسنان في رام الله` أو `محلات أدوات في برلين`. يفتح البرنامج خرائط Google في متصفح Chrome، ويفتح صفحات النتائج، ثم يجمع اسم النشاط التجاري والعنوان والموقع الإلكتروني ورقم الهاتف وعناوين البريد الإلكتروني المتاحة ورابط النشاط على خرائط Google. إذا لم يظهر البريد الإلكتروني في صفحة النشاط، يمكنه فحص الموقع الإلكتروني المرتبط به.

يحفظ البرنامج النتائج في ملف CSV باسم يتضمن التاريخ والوقت، وينشئ تقريراً نصياً يحتوي على عينة من النتائج. ويمكنه أيضاً حفظ ملفات تعريف الارتباط وبيانات المتصفح في ملف `maps_session.pkl` لاستخدامها في الجلسات التالية.

#### التثبيت والاستخدام

المتطلبات:
- Python إصدار 3.9 أو أحدث
- تثبيت متصفح Google Chrome
- اتصال بالإنترنت

1. حمّل الملف `oldscraper25/palscraper.zip` وفك ضغطه داخل مجلد `oldscraper25`. يجب أن يظهر الملفان `ms.py` و`run.bat` بجانب ملف `requirements.txt`.
2. افتح نافذة الأوامر داخل هذا المجلد.
3. أنشئ بيئة Python مستقلة وثبّت المكتبات:

Windows PowerShell:
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
```

Linux أو macOS:
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

4. شغّل البرنامج:

Windows:
```powershell
py ms.py
```

Linux أو macOS:
```bash
python3 ms.py
```

5. أدخل عبارة البحث في خرائط Google عندما يطلبها البرنامج، ثم اختر وضع التشغيل. الوضع 1 هو الوضع الموصى به مع إعادة المحاولة والتعافي من الأخطاء، والوضع 2 ينفذ محاولة عادية واحدة، والوضع 3 يستخدم طريقة التشغيل القديمة.

يحفظ البرنامج ملفات CSV والتقرير النصي في المجلد الذي شغّلت منه البرنامج. يحتوي ملف CSV على الأعمدة التالية: الاسم، العنوان، الموقع الإلكتروني، الهاتف، البريد الإلكتروني، ورابط خرائط Google. إذا وُجد أكثر من بريد إلكتروني، تُفصل العناوين بفاصلة منقوطة.

#### ملاحظات

- يحتاج التشغيل الأول إلى اتصال بالإنترنت. تقوم مكتبة WebDriver Manager بتنزيل إصدار ChromeDriver المناسب تلقائياً.
- ملف `run.bat` مخصص لنظام Windows ويطلب صلاحيات المسؤول. تشغيل الأمر `py ms.py` مباشرة يكفي عادةً ولا يحتاج إلى هذه الصلاحيات.
- يستخدم متصفح Chrome الآلي إعدادات تغيّر بعض خصائص أمان المتصفح. لا تسجّل الدخول إلى حساباتك الشخصية في هذه النافذة ولا تستخدمها للتصفح العادي.
- قد يحتوي ملف `maps_session.pkl` على ملفات تعريف الارتباط وبيانات المتصفح. احتفظ به بشكل خاص ولا ترفعه أو تشاركه.
- قد تمنع خرائط Google أو المواقع التجارية الطلبات الآلية، وقد يتغير شكل صفحاتها. لا توجد ضمانات لعدد النتائج. أوقف التشغيل أو انتظر عند ظهور CAPTCHA أو رسالة حظر.
- استخدم البرنامج فقط عندما يكون لديك إذن بذلك. التزم بشروط خرائط Google والمواقع التي تزورها، وبقوانين الخصوصية وقواعد جمع بيانات الاتصال واستخدامها.

