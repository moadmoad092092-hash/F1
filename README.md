# تحويل الموقع إلى تطبيق Android

هذا المشروع يحافظ على واجهة التحويل الأصلية ويضيف خادم Node.js محليًا يبني APK حقيقيًا. عند الضغط على «تحويل»، ينشئ الخادم مشروع Android WebView مؤقتًا، يضع اسم التطبيق والرابط بداخله، يشغّل Gradle، ويتحقق من وجود `app-release.apk` قبل إظهار «تنزيل APK».

## التشغيل

يتطلب البناء على الجهاز المضيف:

- Node.js 18 أو أحدث.
- Java 17.
- Android SDK مع `platforms;android-35` و`build-tools;35.0.0`.
- Gradle 8.7 أو أحدث، أو ضبط المسار عبر `GRADLE_BIN`.

مثال:

```bash
export ANDROID_HOME=/path/to/android-sdk
export GRADLE_BIN=/path/to/gradle
npm start
```

ثم افتح `http://localhost:3000`. لا يحتاج المشروع إلى قاعدة بيانات أو تسجيل دخول أو خدمة مدفوعة. يجب تشغيله عبر Node.js، لأن استضافة ملفات HTML وحدها لا تستطيع تنفيذ Gradle أو إنشاء APK.
