<p align="center"><img src="icon.png" width="96" alt="OxideCut"></p>

# OxideCut

Free laser design and control program for GRBL machines, for Windows. English and Arabic (right-to-left) interface.

**Download:** go to [Releases](../../releases/latest) and get `OxideCut-Setup-<version>.exe`. It installs for your user only and needs no administrator rights.

OxideCut is **free to use, but not open source**: the source code is not published and the program may not be modified or redistributed (see [LICENSE.txt](LICENSE.txt)).

## What it does

- Draw shapes, text (Arabic included), QR codes and barcodes, or import SVG, DXF and pictures.
- Boolean operations, offset, fillet, arrays, text on a path, auto-nesting, cut tabs, guides and rulers.
- Layers with speed, power, passes, kerf, lead-in, fill and image modes.
- Toolpath preview with time estimate, framing, and G-code export for GRBL.
- Connect to a real machine over USB or try everything on the built-in virtual machine.
- Export the layout as SVG or DXF.
- Updates from inside the program (Help > Check for updates). Only files signed by the author are installed.

## Safety

A laser can burn, blind and start fires. Wear eye protection, ventilate, never leave a running job unattended, and check the toolpath, speed and power before every job. OxideCut was tested in simulation and with a virtual machine; behaviour on your hardware may differ. See the license for the full terms.

## Install from PowerShell (optional)

Downloads the latest installer and installs it silently for your user (no administrator rights):

```powershell
$r = Invoke-RestMethod "https://api.github.com/repos/abduhalmawla-tech/OxideCut/releases/latest"
$a = $r.assets | Where-Object name -like "OxideCut-Setup-*.exe" | Select-Object -First 1
$f = Join-Path $env:TEMP $a.name
Invoke-WebRequest $a.browser_download_url -OutFile $f
& $f /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

Useful options: `/DIR="D:\OxideCut"` (install folder), `/LANG=arabic` (installer language).
To remove it silently: `& "$env:LOCALAPPDATA\Programs\OxideCut\unins000.exe" /VERYSILENT`
(use your install folder if you chose another one). Your settings in `%APPDATA%\OxideCut` are kept.

## Windows warning

The installer is not signed with a paid code-signing certificate, so Windows SmartScreen may say "unknown publisher". Choose **More info > Run anyway** if you downloaded it from this page.

## Bugs and ideas

Use [Issues](../../issues). Please do not post private project files.

---

<div dir="rtl" align="right">

# OxideCut

برنامج مجاني لتصميم وتشغيل ماكينات الليزر (GRBL) على Windows، بواجهة عربية (من اليمين إلى اليسار) وإنجليزية.

**التحميل:** من صفحة [Releases](../../releases/latest) حمّل `OxideCut-Setup-<الإصدار>.exe`. يثبّت للمستخدم الحالي ولا يحتاج صلاحيات مدير.

OxideCut **مجاني الاستعمال لكنه ليس مفتوح المصدر**: الكود غير منشور، ولا يجوز تعديل البرنامج أو إعادة توزيعه (انظر [LICENSE-ar.txt](LICENSE-ar.txt)).

## ما يفعله

- رسم الأشكال والنصوص (بما فيها العربي) ورموز QR والباركود، أو استيراد SVG وDXF والصور.
- عمليات منطقية، إزاحة، تدوير الزوايا، مصفوفات، نص على مسار، ترتيب ذكي، علامات القص، أدلة ومساطر.
- طبقات بالسرعة والقوة والتمريرات وعرض القص ومسار الدخول والتعبئة ووضع الصور.
- معاينة المسار مع الوقت المقدّر وتأطير وتصدير G-code لـ GRBL.
- الاتصال بجهاز حقيقي عبر USB أو التجربة على جهاز افتراضي مدمج.
- تصدير التصميم بصيغة SVG أو DXF.
- التحديث من داخل البرنامج (مساعدة ← بحث عن تحديثات)، ولا يُثبَّت إلا ما وقّعه المطوّر.

## السلامة

الليزر قد يحرق ويعمي ويسبب حرائق. ارتدِ حماية للعينين، وهوِّ المكان، ولا تترك مهمة تعمل دون مراقبة، وافحص المسار والسرعة والقوة قبل كل مهمة. جُرّب البرنامج بالمحاكاة وبجهاز افتراضي، وقد يختلف سلوكه على جهازك. التفاصيل في الترخيص.

## التثبيت من PowerShell (اختياري)

ينزّل آخر مثبّت ويثبّته بصمت للمستخدم الحالي (بدون صلاحيات مدير). الأوامر نفسها المكتوبة أعلاه بالإنجليزية، شغّلها في PowerShell.

خيارات مفيدة: `/DIR="D:\OxideCut"` لتحديد مجلد التثبيت، و`/LANG=arabic` للغة المثبّت.
للإزالة بصمت: `& "$env:LOCALAPPDATA\Programs\OxideCut\unins000.exe" /VERYSILENT` (استعمل مجلد تثبيتك إن اخترت غير الافتراضي). إعداداتك في `%APPDATA%\OxideCut` تبقى.

## تحذير Windows

المثبّت غير موقّع بشهادة مدفوعة، لذلك قد يقول SmartScreen «ناشر غير معروف». اختر **مزيد من المعلومات ← تشغيل على أي حال** إن حمّلته من هذه الصفحة.

## الأخطاء والأفكار

استعمل [Issues](../../issues). من فضلك لا تنشر ملفات مشاريعك الخاصة.

</div>
