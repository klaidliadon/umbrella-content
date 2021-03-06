---
index: 9
title: Orbot و Orfox
---
Orbot و Orfox
---

مرورگر وب پیشرفته حریم خصوصی برای آندروید

** درسی برای خواندن: [اینترنت] (چتر: // درس / اینترنت)، [تلفن های همراه] (چتر: // درس / تلفن همراه) **
** سطح **: مبتدی
** زمان لازم **: 15 دقیقه
** منتشر شده: آوریل 2018
** منابع: ** برنامه ریز امنیتی (آزمایشگاه شهروندی)، [Orbot و Orfox] (https://securityplanner.org/#/tool/orbot-and-orfox)؛ امنیت در جعبه، [ORBOT برای آندروید] (https://securityinabox.org/en/guide/orbot/android/)، پروژه گاردین، [Orbot v16: کاملا جدید و آسانتر برای استفاده!] (https : //guardianproject.info/2018/01/05/orbot-v16-a-whole-new-look-and-easier-to-use/)

** استفاده از Orbot و Orfox با هم به شما خواهد داد: **
- توانایی پنهان کردن هویت آنلاین خود را از وب سایت ها و سایر خدمات هنگام استفاده از برنامه های خاص اندروید.
- توانایی پنهان کردن فعالیت های مرور شما هنگام استفاده از Orfox.
- توانایی دور زدن سانسور اینترنت و فیلترینگ آنلاین هنگام استفاده از Orfox.

** محل دانلود: ** [Orbot] (https://play.google.com/store/apps/details؟id=org.torproject.android) و [Orfox] (https://play.google.com/ فروشگاه / برنامه / جزئیات؟ id = info.guardianproject.orfox) در فروشگاه Google Play.
** نرم افزار مورد نیاز: ** با دستگاه (Orbot) . Android 4.0.3 و بالاتر (Orfox)
** نسخه مورد استفاده در این راهنما **: نسخه 16 (Orbot) Fennec-52.7.3esr / TorBrowser-7.5.3 / Orfox-1.5.2-RC-1 (Orfox)
** مجوز **: FOSS (در اصل GPLv2)


# 1. معرفی

Orbot به برنامه های دیگر در دستگاه های اندروید اجازه می دهد از شبکه اینترنتی Tor به طور ایمن از اینترنت استفاده کنند. (بیشتر بدانید در مورد [** Tor **] (چتر: // درس / اینترنت / 1).) Orfox یک نسخه از مرورگر Tor برای آندروید است که از Orbot برای اتصال به شبکه Tor استفاده می کند.

به یاد داشته باشید، اگر از Orfox برای بازگشت به محتویاتی که قبلا بدون استفاده از Orfox ایجاد کرده اید، مانند پست وبلاگ، سایت هایی که محتوای سایت را ذخیره می کنند، هنوز مکان واقعی شما را می دانند.

اگر میخواهید هنگام استفاده از Orfox ناشناس ماندن قویتری داشته باشید:

*   هرگز به حسابهای ساخته شده با نام واقعی خود دسترسی نداشته باشید.
*   هرگز اطلاعات شخصی خود را ندهید
*   کارهایی که زمانی که سعی ندارید ناشناس باشید انجام می دهید، اجتناب کنید.


# 2. Orbot را نصب و پیکربندی کنید


## 2.1 نصب Orbot

** مرحله 1: ** بر روی دستگاه Android خود، ** دانلود ** و ** نصب برنامه ** از [فروشگاه Google Play] (https://play.google.com/store/apps/details؟id = org.torproject.android) روی نصب فشار دهید.

! [] (orbot-and-002.png)

** توجه: ** همچنین می توانید** Orbot ** را از فروشگاه شخص ثالث [F-Droid] (https://guardianproject.info/fdroid/) دانلود کنید.


## 2.2 پیکربندی اوربوت

** مرحله 1: ** روی ** بازکردن کلیک کنید **

! [] (orbot-and-005.png)

** مرحله 2: ** روی صفحات خوش آمدید در جادوگر راه اندازی بکشید ، و یا فلش بعدی را لمس کنید.

! [] (orbot-and-006.png)! [] (orbot-and-007.png)

** مرحله 3: ** اگر دسترسی شما به شبکه Tor ممکن است مسدود شود، ممکن است لازم باشد از یک پل استفاده کنید.

! [] (orbot-and-009.png)

! [] (orbot-and-010.png)

اگر مطمئن نیستید که به یک پل نیاز دارید، ابتدا بدون آن را امتحان کنید. برای کسب اطلاعات بیشتر در مورد پل ها، * پیکربندی پیشرفته اوربوت: * استفاده از پل تور *را در زیر بخوانید.

** مرحله 4: ** اگر میخواهید به یک برنامه مسدود شده دسترسی پیدا کنید، با کلیک روی ** انتخاب برنامه **، از Orbot به عنوان یک VPN (شبکه خصوصی مجازی) استفاده کنید.

! [] (orbot-and-008.png)

برنامه های مشخصی را که می خواهید با ** Orbot ** استفاده کنید را انتخاب کنید و روی باشه کلیک کنید.

> "به جای ارتقاء نوعی جادوی خودکار، تور را برای تمام دستگاه من فعال کن"، ما می خواهیم روی راه هایی برای فعال کردن برنامه های خاص برای رفتن از طریق Tor تمرکز کنیم، تا بتوانیم اطمینان یابیم که تا حد امکان امن است. " پروژه نگهبان، [27 اکتبر 2017] (https://guardianproject.info/2017/10/27/no-more-root-features-in-orbot-use-orfox-vpn-instead/)

توجه داشته باشید که بسیاری از برنامه ها، مانند آنهایی که نیاز به ورود به سیستم دارند، ناشناس بودن شما را تضعیف می کنند، حتی اگر ترافیک اینترنتی از طریق Orbot تونل شود. این مرحله به شما کمک خواهد کرد اگر یک فایروال یا یک فیلتر یک برنامه خاص را مسدود کند، اما شما را ناشناس نگذارد.


! [] (orbot-and-011.png)

! [] (orbot-and-012.png)

هنگامی که کار شما با تنظیمات انجام می شود، صفحه غیر فعال * Orbot ** به شما نمایش داده می شود.

! [] (orbot-and-013.png)

# 3. شروع به استفاده از Orbot کنید

** مرحله 1: ** نماد خاکستری اوربوت را در مرکز صفحه لمس کنید تا زرد رنگ شود.

! [] (orbot-and-014.png)

** مرحله 2: ** هنگام اتصال، Orbot سبز می شود.

! [] (orbot-and-015.png)

** مرحله 3: ** برای قطع کردن آن نماد سبز را لمس کنید تا خاکستری شود، یا روی نماد منو در سمت راست بالای صفحه کلیک کنید و روی خروج ضربه بزنید تا از برنامه خارج شوید.

! [] (orbot-and-019.png)

** مرحله 4: ** جهانی(اتوماتیک) را  * برای انتخاب یک لیست از مکان هایی که ممکن است ترافیک اینترنتی شما از آنجا باشد،لمس کنید.

! [] (orbot-and-022.png)

** مرحله 5.  حالت VPN * را برای دسترسی به برنامه های ذکر شده توسط تونل زدن ترافیک اینترنت خود از طریق Orbot روی روشن بگذارید. با کلیک بر روی * برنامه های فعال * فعال در پایین صفحه  برنامه های بیشتری را به لیست اضافه کنید.


# 4. پیکربندی پیشرفته Orbot : از یک پل تور استفاده کنید

اگر دسترسی Tor محدود شده باشد یا شما مایل به مخفی کردن این واقعیت باشید که از Tor استفاده می کنید، می توانید Orbot را برای استفاده از * پل ها پیکربندی کنید. اطلاعات بیشتر در مورد پل ها در راهنمای [تور برای لینوکس] (چتر: // درس / تور برای لینوکس).

** مرحله 1: ** روی نماد منو در بالا سمت راست ضربه بزنید و * تنظیمات * را انتخاب کنید. حرکت به سمت پایین تا به * پل ها * برسید. جعبه کنار * استفاده از پل ها را تیک بزنید*

! [] (orbot-and-025.png)

** مرحله 2: ** اگر شما می دانید * آدرس IP * یک * پل * که می خواهید استفاده کنید را میدانید، روی * آدرس IP و پورت پل * ضربه بزنید. آدرس IP را وارد کنید و روی باشه ضربه بزنید.

! [] (/ media / orbot-and-026.png)

** مرحله 3: **  برای شروع استفاده از * پل * ** Orbot ** را  راه اندازی مجدد کنید.

شما می توانید اطلاعات بیشتر در مورد پل ها را در وب سایت پروژه Tor ببینید (https://bridges.torproject.org/).


# 5. نصب Orfox

** مرحله 1: ** در دستگاه انروید خود، ** دانلود ** و ** نصب برنامه ** از [فروشگاه Google Play] (https://play.google.com/store/apps/details؟id = info.guardianproject.orfox) انجام دهید.

** توجه: ** ** Orfox ** همچنین می توانید از فروشگاه شخص ثالث [F-Droid] (https://guardianproject.info/fdroid/) دانلود کنید.

** مرحله 2: ** برای باز کردن Orfox، ** نماد برنامه را لمس کنید.

** Orfox ** به شما امکان اتصال به _https: //check.torproject.org_ را میدهد تا اطمینان حاصل شود که اتصال آن به شبکه ** Tor ** کار می کند. اگر می تواند اتصال برقرار کند، پیامی به شما می گوید که مرورگر شما برای استفاده از Tor_ پیکربندی شده است. اگر ** Orfox ** نمی تواند به وب سایت متصل شود، یک پیام خطا را در مرورگر مشاهده خواهید کرد. اگر این اتفاق می افتد، بررسی کنید که Orbot در حال اجرا باشد.

** مرحله 3: ** برای مرور به وب سایت، *روی * منطقه را در بالای صفحه ضربه بزنید و آدرس مورد نظر خود را تایپ کنید.  * برو * بر روی صفحه کلید صفحه نمایش خود را فشار دهید.


# 6. پاک کردن سابقه مرورگر خود در Orfox 

** مرحله 1: ** به صورت دستی سابقه مرور و حافظه پنهان خود را پاک کنید و وبسایتی را که در Orfox بازدید کرده اید، پنهان کنید. در نماد منوی اصلی با سه نقطه در گوشه بالا سمت چپ ضربه بزنید، سپس روی * تنظیمات * ضربه بزنید.

** مرحله 2: روی * پاک کردن داده های خصوصی، * ضربه بزنید* سپس روی * پاک کردن داده ها، * برای حذف داده ها از دسته های ذکر شده  ضربه بزنید.

نکته: هنگامی که این را تنظیم کنید، نمیتوانید دکمه بازگشت را برای مشاهده صفحات وب که قبلا بازدید کرده اید، فشار دهید.

** مرحله 3: ** به منو * تنظیمات بروید و * حریم خصوصی را انتخاب کنید. * پاک کردن اطلاعات خصوصی در خروج* را انتخاب کنید تا به طور خودکار داده های خصوصی را هنگام خروج از برنامه از طریق منوی اصلی پاک کنید.

توجه داشته باشید: انتخاب * تب جدید خصوصی * از منوی اصلی نیز از ضبط هر سابقه مرور در Orfox جلوگیری میکند. فایل هایی که شما دانلود می کنید و صفحات وبی که شما نشانه گذاری میکنید هنوز در دستگاه شما ذخیره می شود.

# 7. تنظیم کردن امنیت مرورگر خود

Orfox دارای ویژگی کشویی امنیتی است که به شما اجازه می دهد بین استاندارد، امن تر و امن ترین تنظیمات امنیتی انتخاب کنید. روی آیکون منوی اصلی با سه نقطه در گوشه بالا سمت راست ضربه بزنید، سپس روی * تنظیمات Orfox * ضربه بزنید. تنظیمات امن تر و امن تر باعث بروز برخی مشکلات در ویژگی های وب می شود، اما شما کمتر در معرض آسیب پذیری قرار می گیرید که هکرها بتوانند به شما حمله کنند.