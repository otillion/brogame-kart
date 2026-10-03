# BroGame Game Kart

بطاقة الولاء لمحل BroGame (ميزيتلي / ميرسين): كل ساعة لعب = طابة، ٦ طابات = ساعة مجانية.

## الروابط

- صفحة الزبون (للـ QR والـ NFC): https://otillion.github.io/brogame-kart/
- شاشة الكود (تابلت الكاشير): https://otillion.github.io/brogame-kart/#screen
- لوحة المالك: https://otillion.github.io/brogame-kart/#admin

شاشة الكود ولوحة المالك بيفتحوا بس بحساب `broogame10@gmail.com`.

## كيف مبني

- الاستضافة: GitHub Pages (هالمستودع).
- تسجيل الدخول والبيانات: Firebase مشروع `brogame-kart` على حساب broogame10، الخطة المجانية Spark.
- `firestore.rules`: قواعد الحماية. نسخة منها منشورة بـ Firebase Console → Firestore → Rules. إذا عدّلتها هون، انسخها والصقها هناك واضغط Publish.

## الحماية

- الكود بيتغيّر كل ٢٠ ثانية، صالح ٣٠ ثانية، وبينستعمل مرة وحدة بس.
- طابة وحدة كل ٥٠ دقيقة لكل حساب، وحد أقصى ٦.
- بس صاحب المحل بيعطي الساعة المجانية.

## تغيير الإعدادات

بملف `index.html` ← `const CONFIG`: `ownerEmails`، `starsForReward`، `codeSeconds`، `codeValidSeconds`، `cooldownMinutes`.
نفس الأرقام لازم تتغيّر بـ `firestore.rules` كمان (الإيميل، `6`، `30, 's'`، `50, 'm'`).

إذا بتضيف دومين جديد للموقع، زيده بـ Firebase → Authentication → Settings → Authorised domains.
