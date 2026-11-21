MEDO CHAT — شات للمبرمجين (موقع ثابت + Firebase)

ليه Firebase؟
GitHub Pages بيستضيف ملفات ثابتة بس (مفيش سيرفر). فالحسابات والرسايل اللحظية بتتخزن في
Firebase (الخطة المجانية Spark كفاية لك ولأصحابك). الموقع كله ملف واحد: index.html

1) إعداد Firebase (مرة واحدة، من المتصفح)
   - console.firebase.google.com ← Add project
   - Build ← Authentication ← Get started ← Email/Password ← Enable
   - Build ← Firestore Database ← Create database (Production mode)
   - Firestore ← Rules ← امسح اللي موجود والصق محتوى firestore.rules ← Publish
   - Project settings ← Your apps ← أيقونة </> (Web) ← انسخ firebaseConfig
   - افتح index.html والصق القيم مكان CFG (apiKey, authDomain, projectId, appId)
   - Authentication ← Settings ← Authorized domains ← ضيف  اسمك.github.io

2) الرفع على GitHub Pages من تريمكس
   pkg install git
   git config --global user.name "اسمك"
   git config --global user.email "ايميلك"
   mkdir medo-chat && cd medo-chat      # حط index.html هنا
   git init && git add . && git commit -m "Medo Chat"
   git branch -M main
   git remote add origin https://github.com/USERNAME/medo-chat.git
   git push -u origin main               # الباسورد = Personal Access Token
   بعدها على GitHub: Settings ← Pages ← Deploy from a branch ← main / root
   الرابط: https://USERNAME.github.io/medo-chat/

3) للتجربة بدون Firebase: افتح الرابط وضيف في آخره  ?demo

اللي موجود: حسابات (username + باسورد) • محادثات فردية وجروبات • رسايل لحظية •
علامات القراءة ✓✓ • مؤشر "يكتب…" • متصل/آخر ظهور • عدّاد غير مقروء • رد/تعديل/حذف/تفاعلات •
صور • بلوكات كود بتلوين ونسخ • 4 ثيمات • إشعارات وصوت • يشتغل على الموبايل والكمبيوتر.
اللي مش موجود لسه: مكالمات صوت/فيديو، رسايل صوتية، تشفير طرف-لطرف.
ملاحظة: الصور بتتضغط وتتخزن جوه الرسالة (عشان Storage محتاج خطة مدفوعة).
