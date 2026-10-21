# সোনা-রুপার হিসাবের খাতা — Android APK project

এই প্রজেক্টে আপনার HTML অ্যাপটি Android WebView-তে চালানোর ব্যবস্থা আছে। লাইভ TradingView কোটের জন্য ইন্টারনেট প্রয়োজন।

## মোবাইল দিয়ে APK বানানোর উপায় (GitHub Actions)

1. ZIP ফাইলটি ডাউনলোড করে ফোনে Extract করুন।
2. https://github.com এ সাইন ইন করে **New repository** তৈরি করুন (যেমন `sona-rupa-hisab`)।
3. repository-তে **Add file → Upload files** নির্বাচন করুন। Extract করা প্রজেক্টের ভেতরের সব ফাইল/ফোল্ডার আপলোড করুন। `.github/workflows/android.yml`-সহ লুকানো `.github` ফোল্ডারটি অবশ্যই অন্তর্ভুক্ত করতে হবে।
4. **Commit changes** করুন।
5. repository-র **Actions** ট্যাবে `Build Android APK` workflow চলবে। সবুজ সফল রান খুলে **Artifacts** অংশ থেকে `sona-rupa-hisab-debug-apk` ডাউনলোড করুন।
6. ডাউনলোড করা ZIP extract করে `app-debug.apk` ইনস্টল করুন। Android চাইলে এই উৎস থেকে অ্যাপ ইনস্টল করার অনুমতি দিন।

## গুরুত্বপূর্ণ
- এই চ্যাট থেকে আপনার GitHub অ্যাকাউন্টে সাইন ইন করা বা আপনার হয়ে repository তৈরি/ফাইল আপলোড করা সম্ভব নয়। তাই APK-টি এখনও বিল্ড করা হয়নি।
- এটি debug APK; Play Store-এ প্রকাশের জন্য আলাদা release signing দরকার।
- অ্যাপের হিসাব স্থানীয় WebView storage-এ থাকে। অ্যাপের ডেটা মুছে ফেললে হিসাব হারাতে পারে, তাই CSV ব্যাকআপ রাখুন।
