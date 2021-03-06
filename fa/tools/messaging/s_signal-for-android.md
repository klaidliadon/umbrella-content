---
index: 16
title: سیگنال برای آندروید
---
سیگنال برای آندروید
==============================
پیام های ایمن

** درسی برای  خواندن: [ارسال پیام] (چتر: // درس / ارسال یک پیام) **
** سطح **: مبتدی و متوسط
** زمان مورد نیاز **: 15-20 دقیقه
** منتشر شده: آوریل 2018 (برخی از تاریخ تصاویر از نسخه های قبلی است)
** منابع: ** EFF، Surveillance Self-Defense [نحوه استفاده از Signal for Android] (https://ssd.eff.org/en/module/how-use-signal-android)؛ امنیت در جعبه [SIGNAL FOR ANDROID] (https://securityinabox.org/en/guide/signal/android/).

** استفاده از سیگنال توانایی زیر را به شما خواهد داد: **

- توانایی فرستادن پیامهای گروهی، متن، تصویر و ویدئو با رمزگذاری سرتاسر و مکالمات تلفنی با دیگر کاربران سیگنال به صورت رمزگذاری شده است.

** محل دانلود **: فروشگاه گوگل پلی(https://play.google.com/store/apps/details؟id=org.thoughtcrime.securesms).

** سیستم مورد نیاز **: اندروید 2.3 و بالاتر، با سرویس های گوگل پلی (شما باید یک حساب Google داشته باشید که با نصب برنامه پیوند دارد).

** نسخه مورد استفاده در این راهنما **: سیگنال 3.31.3

** مجوز: ** GPLv3

** خواندن موارد دیگر **:

*   [http://support.whispersystems.org/](http://support.whispersystems.org/)
*   [https://signal.org/blog/standalone-signal-desktop/](https://signal.org/blog/standalone-signal-desktop/)
*   [https://whispersystems.org/blog/signal-video-calls/](https://whispersystems.org/blog/signal-video-calls/)


معرفی
-----------------
سیگنال نرم افزار رایگان و منبع باز برای آندروید، iOS و دسکتاپ است که از رمزنگاری سرتاسر استفاده می کند، به کاربران اجازه می دهد پیام های گروهی، متن، عکس و ویدئو رمزگذاری شده را به طور کامل ارسال و مکالمات تلفنی رمزگذاری بین کاربران سیگنال وجود دارد

اگرچه سیگنال از شماره تلفن به عنوان مخاطب استفاده می کند، تماس های رمزگذاری شده و پیام ها در واقع از اتصال داده شما استفاده می کنند؛ بنابراین هر دو طرف گفتگو باید دسترسی به اینترنت را در دستگاه های تلفن همراه خود داشته باشند. با توجه به این، کاربران سیگنال هزینه های SMS و MMS را برای این نوع مکالمات تلفنی تحمل نمی کنند.

در اندروید، سیگنال می تواند به عنوان برنامه پیام رسانی متنی پیش فرض شما جایگزین شود، بنابراین در سیگنال امکان ارسال پیام های رمزگذاری نشده وجود دارد.

توجه داشته باشید:
* سیگنال مانع از دسترسی دیگران به محتوای پیام ها و تماس های صوتی شما می شود، اما این واقعیت را که شما از پیام های رمز شده یا برقراری تماس های صوتی رمزگذاری شده استفاده میکنید را پنهان نمی کند. در برخی کشورها ابزارهای رمزنگاری مانند Signal ممکن است توجه را جلب کنند یا محدودیت های قانونی را نقض کنند.
* سیستم های نجوای باز، سازندگان سیگنال، از زیرساخت های شرکت های دیگر (گوگل در آندروید) استفاده می کنند تا زمانی که یک پیام جدید دریافت می کنند، هشدار برای کاربران خود را ارسال کنند. این بدان معنی است که بعضی از ابردادها یا اطلاعاتی در مورد اینکه چه کسی پیامی دریافت می کند و زمان دریافت آن ممکن است به این شرکت ها نشت کند.

نصب سیگنال بر روی گوشی آندروید خود
----------------------------------------
### مرحله 1: دانلود و نصب سیگنال

در دستگاه اندروید خود، وارد فروشگاه گوگل پلی شوید و «سیگنال» جستجو کنید. [سیگنال ساخته شده توسط سیستم نجوای باز] (https://play.google.com/store/apps/details؟id=org.thoughtcrime.securesms) را انتخاب کنید.

بعد از اینکه روی «نصب» ضربه بزنید، یک لیست از عملکردهای اندروید را مشاهده خواهید کرد که Signal باید برای عمل کردن باید به آن دسترسی داشته باشد. روی "پذیرش" کلیک کنید.

پس از دریافت سیگنال، برای باز کردن برنامه، روی "باز کردن" ضربه بزنید.

### مرحله 2: شماره تلفن خود را ثبت و تایید کنید

اکنون صفحه زیر را مشاهده خواهید کرد. شماره تلفن همراه خود را وارد کنید و روی "ثبت نام" ضربه بزنید.

! [] (tool_signalandroid_resized000_0.png)

از شما خواسته می شود شماره تلفن خود را تأیید کنید. روی «ادامه» کلیک کنید.

! [] (tool_signalandroid_resized001_0.png)

برای تأیید شماره تلفن شما، متن SMS با کد شش رقمی ارسال می شود. از آنجا که سیگنال می تواند به پیام های متنی SMS شما دسترسی پیدا کند، پس از دریافت کد و ثبت نام شما، به طور خودکار شناسایی می شود.

! [] (tool_signalandroid_resized002_0.png)

پس از اتمام این فرآیند، شما از پرسیده می شود که آیا شما سیگنال را به عنوان برنامه پیش فرض اس ام اس خود می خواهید. این می تواند برای حفظ تمام پیام های شما در یک مکان مفید باشد. توجه داشته باشید که اگر شما این را قبول کنید، پیام هایی که به مخاطبینی فرستاده شود که سیگنال را نصب نکرده اند (حتی اگر آنها را از طریق برنامه سیگنال ارسال کنید) رمزگذاری نخواهند شد.



استفاده از سیگنال
------------------------------

برای استفاده از سیگنال، با فردی که تماس می گیرید باید سیگنال را نصب کرده باشد. اگر سعی کنید یک پیام را برای کسی با برنامه سیگنال بفرستید و سیگنال نصب نداشته باشد، یک پیام متنی بدون رمزگذاری ارسال می کنید. اگر سعی می کنید با فرد تماس بگیرید، یک تماس تلفنی استاندارد ارائه می شود.

سیگنال لیستی از سایر کاربران سیگنال در مخاطبین شما فراهم می کند. برای انجام این کار، داده هایی که شماره تلفن های موجود در لیست مخاطبین شما را به سرورهای سیگنال ارسال می کنند، تقریبا بلافاصله حذف می شوند.

### نحوه ارسال یک پیام رمز شده

روی نماد مداد در گوشه پایین سمت راست صفحه ضربه بزنید

! [] (tool_signalandroid_resized003_0.png)

شما لیستی از تمام کاربران سیگنال ثبت شده در مخاطبین خود را مشاهده خواهید کرد. شما همچنین می توانید شماره تلفن یک کاربر سیگنال که در مخاطبین شما نیست را وارد کنید. هنگامی که یک مخاطب را انتخاب میکنید، برای تماس با شما به صفحه پیام نوشتاری ارسال می شود. توجه داشته باشید که برای کاربران سیگنال، متن "ارسال پیام سیگنال" را مشاهده خواهید کرد - به این معنی که پیام رمزگذاری می شود. در این صفحه، نماد "تلفن" در گوشه سمت راست بالای صفحه نشان می دهد که شما می توانید یک تماس صوتی رمز شده را با استفاده از سیگنال نیز ایجاد کنید. از این صفحه می توانید پیام های متنی، تصویری و یا ویدئویی رمزگذاری شده را به طور کامل ارسال کنید.

! [] (tool_signalandroid_resized006.png)

برای کاربرانی که سیگنال نصب نداشته باشند، متن "ارسال SMS غیر امن" را مشاهده خواهید کرد که پیام را با رمزگذاری ارسال نخواهد کرد. در این صفحه، نماد "تلفن" در گوشه سمت راست بالای صفحه تماس تلفنی منظم و بدون رمزنگاری را ایجاد می کند.

! [] (tool_signalandroid_resized004_0.png)

### چگونه یک تماس رمز شده بگیریم

برای ایجاد یک تماس رمز شده با یک مخاطب، آن مخاطب را انتخاب کنید و سپس روی نماد تلفن ضربه بزنید. شما می دانید که اگر یک نماد قفل کوچکی در کنار آیکون تلفن مشاهده کنید، مخاطبین شما می تواند تماس های دریافتی را بپذیرد.

! [] (tool_signalandroid_resized006-1.png)

هنگامی که یک تماس برقرار شد، تماس شما رمزگذاری می شود.

### چگونه یک تماس ویدئویی رمز شده را آغاز کنید

برای ایجاد یک تماس ویدئویی رمزگذاری شده، به سادگی با شخص دیگری تماس بگیرید که در بالا توضیح داده شود:

! [] (tool_signalandroid_initial_video_screen.png)

و روی نماد دوربین ویدیویی ضربه بزنید. ممکن است مجبور شوید سیگنال را برای دسترسی به ویدیو از دوربین خود مجاز بدانید. این ویدیو را با دوستانتان به اشتراک می گذارد (ممکن است دوست شما همین کار را انجام دهد).

### چگونگی شروع چت گروهی رمز شده

شما می توانید پیام گروهی رمزگذاری شده را با ضربه زدن بر آیکون سرریز (سه نقطه در گوشه سمت راست بالای صفحه) و انتخاب «گروه جدید» ارسال کنید.

! [] (tool_signalandroid_resized020_0.png)

در صفحه زیر، شما می توانید گروه  را نام گذاری کنید و شرکت کنندگان را به آن اضافه کنید.

! [] (tool_signalandroid_resized021_0.png)

! [] (tool_signalandroid_resized016_0.png)

پس از اضافه کردن شرکت کنندگان، می توانید روی علامت چک در گوشه سمت راست بالای صفحه ضربه بزنید. این گپ گروهی را آغاز خواهد کرد.

! [] (tool_signalandroid_resized019_0.png)

اگر می خواهید آیکون گروه را تغییر دهید، اعضا را اضافه یا حذف کنید، با ضربه زدن بر روی آیکون سرریز (سه نقطه در گوشه سمت راست بالای صفحه) و «به روزرسانی گروه » را از صفحه چت گروهی انتخاب کنید.

### بی صدا کردن مکالمات

گاهی اوقات مکالمات می تواند منحرف شود. یکی از ویژگیهایی که مخصوصا برای گروههای چت مفید است، خنثی شدن اعلانها است، بنابراین هر بار که یک پیام جدید ایجاد میشود، یک اعلان جدید را مشاهده نخواهید کرد. این را می توان از طریق صفحه نمایش چت گروهی با ضربه زدن به آیکون سرریز (سه نقطه در گوشه سمت راست بالای صفحه) و انتخاب "نادیده گرفتن اعلان ها" انجام دهید. پس از آن می توانید انتخاب کنید که برای چه مدت شما مایل هستید فعال نباشد. این می تواند در مورد مکالمات فردی نیز مورد استفاده قرار گیرد.

### چگونگی تأیید مخاطبین خود

در این مرحله، شما می توانید صحت فردی که با او در حال صحبت کردن هستید را تأیید کنید تا مطمئن شوید که کلید رمزگذاری آنها با کلید شخصی دیگر در زمانی که برنامه شما آن را دانلود کرده است(فرآیندی که به آن تأیید کلید میگویند) دستکاری یا جایگزین نشده باشد. تأیید پروسه ای است که زمانی رخ می دهد که شما به صورت فیزیکی با فردی که صحبت می کنید، در ارتباط باشید.

اول، صفحه ای را باز کنید، جایی که در آن شما بتوانید برای مخاطب خود پیام بفرستید، همانطور که در بالا توضیح داده شد. از این صفحه، نماد سرریز(سه نقطه در گوشه سمت راست بالای صفحه) را ضربه بزنید و «تنظیمات مکالمه» را انتخاب کنید.

! [] (tool_signalandroid_resized010_0.png)

از صفحه زیر، روی «تأیید شماره ایمنی » را لمس کنید.

! [] (tool_signalandroid_resized011_0.png)

حالا شما به یک صفحه نمایش می روید که یک کد QR و یک لیست از شماره های ایمنی را نشان می دهد. این کد برای هر تماسی که با آن فرد برقرار میکنید، منحصر به فرد است. مخاطب خود را به صفحه مربوطه برای مکالمه او با شما انتقال دهید، به طوری که آنها یک کد QR نمایش داده شده در صفحه نمایش خود داشته باشند.

! [] (tool_signalandroid_resized012_0.png)

روی دستگاه خود برگردید، بر روی کد QR خود ضربه بزنید، که از دوربین برای اسکن کد QR که روی صفحه نمایش مخاطب شما نمایش داده می شود، استفاده می شود. دوربین خود را روبه روی کد QR بگیرید:

! [] (tool_signalandroid_resized014.png)

امیدوارم دوربین شما بارکد را اسکن کرده و علامت چک را نشان دهد، مانند این:

! [] (tool_signalandroid_resized015.png)

این نشان می دهد که شما تماس خود را با موفقیت تایید کرده اید. اگر به جای این چیز دیگری روی صفحه شما ظاهر شود، چیزی اشتباه پیش رفته است:

! [] (tool_signalandroid_resized013.png)

ممکن است بخواهید از بحث در مورد موضوعات حساس جلوگیری کنید تا زمانی که کلید آن شخص تایید نشده باشد.

_ توجه برای کاربران قدرتمند: روی صفحه نمایش کد QR خود نیز دارای آیکون برای به اشتراک گذاشتن شماره ایمنی خود در گوشه سمت راست است. تأیید صحت شخصی روش متداول است، اما شما ممکن است قبلا تماس خود را با استفاده از یک برنامه امن دیگر مانند PGP تایید کرده باشید. از آنجایی که قبلا تماس خود را تایید کرده اید، می توانید با اعتماد به نفس در این نرم افزار برای اعتبار سنجی ایمنی در سیگنال، بدون نیاز به حضور فیزیکی در کنار مخاطب خود، از اعتبار استفاده کنید. در این مورد می توانید شماره ایمنی خود را با این برنامه با ضربه زدن بر روی آیکون "اشتراک" به اشتراک بگذارید و با شماره ایمنی خود تماس بگیرید.

### ناپدید شدن پیام ها

سیگنال دارای یک ویژگی به نام ناپدید شدن پیام ها است که تضمین می کند که پیام ها از دستگاه شما و دستگاه مخاطب شما در زمان انتخاب شده پس دیدن پیام، حذف می شود. برای فعال کردن  ناپدید شدن پیام ها برای یک مکالمه، صفحه ای را باز کنید که در آن شما بتوانید به مخاطب خود پیام بفرستید. از این صفحه، آیکون سرریز (سه نقطه در گوشه سمت راست بالای صفحه) را ضربه بزنید و "ناپدید شدن پیامها" را انتخاب کنید.

! [] (tool_signalandroid_resized022_0.png)

یک صفحه جدید ظاهر خواهد شد که به شما اجازه می دهد تا انتخاب کنید که پیام ها با چه سرعتی ناپدید شوند:

! [] (tool_signalandroid_resized009.png)

پس از انتخاب گزینه، باید اطلاعاتی را در گفتگو ببینید که پیامهای ناپدید شده فعال شده اند.

! [] (tool_signalandroid_resized008_0.png)

شما هم اکنون می توانید اطمینان حاصل کنید که پیام های شما بعد از مقدار انتخاب شده پس از دیده شدن برداشته می شوند.