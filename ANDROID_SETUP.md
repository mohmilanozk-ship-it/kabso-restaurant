# إعداد Android
- أنشئ مشروع Flutter Android قياسياً أو نفّذ `flutter create .` داخل هذا المجلد بعد تثبيت Flutter.
- عيّن `applicationId` فريداً في `android/app/build.gradle` قبل النشر.
- أضف الشعار إلى موارد Android وأنشئ launcher icon عبر flutter_launcher_icons عند تجهيز الهوية النهائية.
- أنشئ keystore خارج المستودع، واربطه بملف `key.properties` غير المرفوع إلى Git.
- لا تستخدم `DEMO_USER_ID` للإنتاج؛ اربط تسجيل الدخول الحقيقي واحصل على user ID من جلسة موثقة.

- أضيفت شاشة تسجيل/إنشاء حساب تجريبية متصلة بنقاط `/api/auth/register` و`/api/auth/login`. كلمة المرور المطلوبة 10 محارف على الأقل. لا يوجد OTP أو استعادة كلمة مرور بعد.
- لا تستخدم عنوان HTTP غير المشفر في الإنتاج؛ اضبط API على HTTPS.
