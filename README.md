# دوره آموزش برنامه نویسی وب
وبسایتی که برای مطالب ازش کمک میگیریم:
https://www.learn-html.org
## مقدمه
<div>
    <img height="300" alt="image" src="https://github.com/user-attachments/assets/25f72354-3147-4362-ae0e-858cd8c0807f" />
    <img height="300" alt="image" src="https://github.com/user-attachments/assets/e8878395-a53c-4e6f-b6be-9a9c68417b33" />
</div>

- پسوند فایل های هر نوع `html.` یا `css.` یا `js.` باید باشه.
- برای نوشتن آنلاین کد های وب میتوانید سرچ کنید `run html css js online` و یکی از وبسایت های به دست آمده را استفاده کنید.
- برای نوشتن کد ها در ویندوز میتوانید از هر ویرایشگر نوشته دلخواه مثل `notepad` یا [vscode](https://code.visualstudio.com/Download) استفاده کنید. 

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- اطلاعات هد یا همان سر داخل اینجا نوشته میشود -->
    </head>
    <body>
        <!-- اطلاعات بادی یا همن بدنه داخل اینجا نوشته میشود -->
    </body>
</html>
```
- بخش head شامل اطلاعاتی هست که بیشترشون ممکنه دیده نشوند ولی مرورگر و موتور های جست و جو به آن ها نیاز دارند. مثل: عنوان تب صفحه، آیکون تب صفحه، نام نویسنده، ...
- بخش body شامل اطلاعاتی هست که برای کاربر نمایش داده میشوند مثل تیتر ها، پاراگراف ها، عکس ها، لینک ها، ...

<img width="1280" height="688" alt="اhtml template from w3schools" src="https://github.com/user-attachments/assets/b244908e-4e8a-4da5-a6fc-4ac94ee28ea9" />

تنظیم عنوان تب و نوشتن پاراگراف با تگ های `<title>` و `<p>` :
```html
<!DOCTYPE html>
<html>
    <head>
        <title>عنوان دلخواه برای تب در مرورگر</title>
    </head>
    <body>
        <p>یک پاراگراف از نوشته های دلخواه</p>
    </body>
</html>
```
## تگ ها معروف و پرکاربرد تر:
- تگ کامنت که برای یادداشت گذاری داخل کد هامون استفاده میشه و چیزی رو توی صفحه برای کاربر نمایش نمیده:
```html
<!-- some comment here -->
```
- تگ های h1 تا h6: تیتر ها از بزرگ ترین تا کوچک ترین
```html
<h1>hello</h1>
<h2>hello</h2>
<h3>hello</h3>
<h4>hello</h4>
<h5>hello</h5>
<h6>hello</h6>
```
- تگ hr: کشیدن خط افی
```html
<hr>
```
- تگ br: گذاشتن یک خط خالی
```html
<br>
```
- تگ a برای لینک کردن به یک آدرس دلخواه
```html
<a href="https://digikala.com">لینک به یه وبسایت</a>
```
- تگ img برای قرار دادن عکس در صفحه (صفت های width و height برای تنظیم عرض و ارتفاع به کار میروند که میتوان یک یا هر دوی آن ها را تنظیم نمود):
```html
<img src="https://picsum.photos/536/354" height="300" width="500">
```
- تگ ol برای لیست شماره گذاری شده (برای هر آیتم جدید در لیست یک تگ li میگذاریم):
```html
<ol>
    <li>cat</li>
    <li>dog</li>
    <li>chicken</li>
<ol>
```

- تگ ul برای لیست بدون شماره (برای هر آیتم جدید در لیست یک تگ li میگذاریم):
```html
<ul>
    <li>cat</li>
    <li>dog</li>
    <li>chicken</li>
<ul>
```
- نوشتن یک تگ داخل تگ دیگر. مثلا یک لینک با تگ a را داخل یک تگ p مینویسیم:
```html
<p>this is a link of <a href="https://digikala.com">digikala</a> that we have written here.</p>
```
- تگ div و span برای نوشتن یا گروه بندی مجموعه ای از تگ های دیگر به کار میروند. تگ div از نوع block-level هست و تمام فضای در دسترس تا انتهای خط رو برای خودش اشغال میکنه. تگ span از نوع inline-level هست و فقط به اندازه نوشته داخلش فضا اشغال میکنه. مثال استفاده:
```html
<div style="background-color: gold;">
    <a href="https://digikala.com">دیجی کالا</a>
    <br>
    <a href="https://divar.ir">دیوار</a>
    <br>
    <a href="https://torob.com">ترب</a>
</div>

<span style="background-color: aqua;">
    <a href="https://digikala.com">دیجی کالا</a>
    <br>
    <a href="https://divar.ir">دیوار</a>
    <br>
    <a href="https://torob.com">ترب</a>
</span>
```
## قالب نوشتار CSS
از css برای تعیین استایل های وبسایتمون استفاده میکنیم.

3 راه برای تعیین استایل وجود داره. فرض کنید میخوایم رنگ پس زمینه تعیین کنیم:
1. داخل attribute تگ که در body قرار داره مینویسیم:
```html
<!DOCTYPE html>
<html>
    <head>
        <title>عنوان دلخواه برای تب در مرورگر</title>
    </head>
    <body>
        <h1>تیتر بزرگ دلخواه</h1>
        <p>پاراگراف اول از نوشته های دلخواه</p>
        <p style="background-color: green;">پاراگراف دوم از نوشته های دلخواه</p>
        <p>پاراگراف سوم از نوشته های دلخواه</p>
    </body>
</html>
```
به این صورت در کد بالا فقط پاراگراف مشخص شده پس زمینه سبز به خود میگیرد. مشابها میشد از رنگ های دیگه استفاده کرد یا استایل رو داخل تگ های دیگه مثل h1 یا body و ... هم نوشت. (نکته: به نحوه نوشتن استایل توجه کنید و نقطه ویرگول پایانی و 2نقطه قبل از رنگ را فراموش نکنید)

2. داخل تگ style که در head نوشته میشود میتوانیم برای همه تگ ها از یک نوع خاص استایل تعریف کنیم:
```html
<!DOCTYPE html>
<html>
    <head>
        <title>عنوان دلخواه برای تب در مرورگر</title>
        <style>
            p {
                background-color: green;
            }

            h2 {
                background-color: yellow;
            }
        </style>
    </head>
    <body>
        <h1>تیتر بزرگ دلخواه</h1>
        <h2>تیتر متوسط اول</h2>
        <p>پاراگراف اول از نوشته های دلخواه</p>
        <p>پاراگراف دوم از نوشته های دلخواه</p>
        <p>پاراگراف سوم از نوشته های دلخواه</p>
        <h2>تیتر متوسط دوم</h2>
        <p>پاراگراف چهارم از نوشته های دلخواه</p>
        <p>پاراگراف پنجم از نوشته های دلخواه</p>
        <p>پاراگراف ششم از نوشته های دلخواه</p>
    </body>
</html>
```

به این ترتیب با نوشتن کد بالا همه تگ های نوع p رنگ پس زمینه سبز و همه تگ های نوع h2 پس زمینه زرد میگیرند. (نکته: به قالب نوشتاری مثل آکولاد های آغازین و پایانی توجه کنید)

3. محتویات تگ style رو به جای نوشتن در head ، در یک فایل css جداگانه مینویسیم و فقط کافی هست که با تگ link آن را به فایل html خود متصل کنیم.

فایل styles.css :
```css
p {
    background-color: green;
}

h2 {
    background-color: yellow;
}
```

فایل index.html:
```html
<!DOCTYPE html>
<html>
    <head>
        <title>عنوان دلخواه برای تب در مرورگر</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
        <h1>تیتر بزرگ دلخواه</h1>
        <h2>تیتر متوسط اول</h2>
        <p>پاراگراف اول از نوشته های دلخواه</p>
        <p>پاراگراف دوم از نوشته های دلخواه</p>
        <p>پاراگراف سوم از نوشته های دلخواه</p>
        <h2>تیتر متوسط دوم</h2>
        <p>پاراگراف چهارم از نوشته های دلخواه</p>
        <p>پاراگراف پنجم از نوشته های دلخواه</p>
        <p>پاراگراف ششم از نوشته های دلخواه</p>
    </body>
</html>
```
توجه کنید که اگر اسم فایل css خودتون رو چیز دیگری نوشته بودید هم باید عینا همان اسم را در تگ link به کار ببرید. بخش `stylesheet` هم نمایانگر این است که نوع فایل لینک شده، استایل های css است.

### استایل های CSS
حالا که قالب نوشتار کلی CSS رو یاد گرفتید میتونیم استایل های پر کاربرد تر رو معرفی کنیم.

- تعیین رنگ پس زمینه با background-color:
```css
background-color: red;
```
- تعیین محل قرار گیری نوشته (وسط یا چپ یا راست):
```css
text-align: center; /* وسط چین کردن نوشته */
text-align: left; /* چپ چین کردن نوشته */
text-align: right; /* راست چین کردن نوشته */
text-align: justify;   /* کشیده کردن متن بین دو طرف */
```
- کامنت گذاری: همانطور که در کد بالا میبینید نوشته های قرار گرفته داخل `/* */` کامنت در نظر گرفته میشوند و اجرا نمیشوند.
- تنظیم راست به چپ یا چپ به راست بودن نوشته به صورت خودکار:
```css
unicode-bidi: plaintext;
```
- تعیین نوع display به block یا inline:
```css
display: block; /* تمام فضا تا انتهای خط را اشعال میکند */
display: inline; /* فقط به اندازه خودش فضا اشغال میکند */
display: none; /* حذف کامل باکس نوشته که باعث پنهان شدنش میشود */
```
- رنگ نوشته با color:
```css
color: #ff0000; /* تعیین کد رنگ */
color: red; /* تعیین اسم رنگ */
color: rgb(255,0,0); /* تعیین مقدار قرمز و سبز و آبی */
```
هر کدوم از مدل های بالا رو که بخوایم میتونیم برای تعیین رنگ استفاده کنیم. مشابها همه این مدل ها برای سایر استایل هایی که مربوط به تعیین رنگ هستند قابل استفاده اند.

- تعیین اندازه height و width عناصر موجود در صفحه:
```css
width: 200px; /* تعیین عرض */
height: 150px; /* تعیین ارتفاع */
width: 50%; /* درصد نسبت به والد */
```
- تعیین شفافیت یا opacity (یک عدد بین صفر تا 1):
```css
opacity: 0.5; /* نصف شفاف */
```
- تعیین فونت استفاده شده با font-family:
```css
font-family: serif; /* دارای انتهای تزئینی و رسمی */
font-family: sans-serif; /* ساده، تمیز و بدون تزئینات پایانی */
font-family: monospace; /* دارای عرض یکسان برای همه حروف */
font-family: cursive; /* شبیه دست‌نویس و روان */
font-family: fantasy; /* تزئینی و غیررسمی */
```
- تعیین سایز فونت با font-size:
```css
font-size: 16px;
```
- تعیین ضخامت نوشته با font-weight:
```css
font-weight: 100; /* بسیار نازک */
font-weight: 200; /* نازک */
font-weight: 300; /* کمی نازک */
font-weight: 400; /* وزن عادی متن */
font-weight: 500; /* کمی کلفت‌تر از عادی */
font-weight: 600; /* نیمه‌کلفت */
font-weight: 700; /* کلفت */
font-weight: 800; /* بسیار کلفت */
font-weight: 900; /* بیشترین ضخامت */
font-weight: bold; /* همان حدود 700 */
font-weight: normal; /* همان حدود 400 */
```
- تعیین استایل نوشته با font-style:
```css
font-style: normal; /* حالت عادی و استاندارد متن */
font-style: italic; /* کج یا ایتالیک */
```
- تعیین فاصله بین خطوط نوشته با line-height:
```css
line-height: 1;   /* خطوط چسبیده به هم */
line-height: 1.2; /* مقدار پیش‌فرض تقریبی مرورگر */
line-height: 1.5; /* خوانایی بهتر، مقدار رایج */
line-height: 1.8; /* فاصله زیاد و متن بازتر */
```
- تعیین فاصله بین حروف با letter-spacing:
```css
letter-spacing: 0px;   /* فاصله عادی بین حروف */
letter-spacing: 1px;   /* کمی فاصله بیشتر */
letter-spacing: 2px;   /* فاصله مشخص و قابل توجه */
letter-spacing: -1px;  /* کمی فشرده‌تر شدن حروف */
letter-spacing: normal; /* مقدار پیش‌فرض مرورگر */
```
### نحوه استفاده از id
با تنظیم id های منحصر به فرد برای تگ های دلخواه میتوانیم برای آن تگ به خصوص استایل تعریف کنیم یا لینک مخصوص به آن ایجاد کنیم. نمونه:
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            #my-id {
                background-color: blue; /* تنها برای تگ با آیدی تعیین شده کار میکند */
            }
        </style>
    </head>
    <body>
        <p>یک پاراگراف از نوشته های دلخواه</p>
        <p id="my-id">یک پاراگراف از نوشته های دلخواه</p>
        <p>یک پاراگراف از نوشته های دلخواه</p>
        <a href="#my-id">لینک به آیدی تعیین شده</a> <!-- درصورتی که حجم مطالب زیاد باشد با کلیک بر روی آن به تگ با آیدی مورد نظر میرود -->
    </body>
</html>
```
### نحوه استفاده از class
گاهی قصد داریم یک تم تکراری را برای تعدادی از بخش های مشابه اعمال کنیم. در این صورت از class استفاده میکنیم. توجه کنید که استفاده از آن مشابه id هست با این تفاوت که ابتدای id در css علامت # و ابتدای class علامت نقطه را میگذاریم. همچنین اگر بخواهیم از ترکیب چند class استفاده کنیم میتوانیم بین آنها فاصله بگذاریم. نمونه:

html:
```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2 id="titr1" class="rast-chin">سلام</h2>
    <h2 id="titr2" class="rast-chin">مثال</h2>
    <h2 class="rast-chin">سگ</h2>
    <h2 class="rast-chin">گربه</h2>
    
    <h2 class="chap-chin kam-rang">انسان</h2>
    <h2 class="chap-chin kam-rang">توپ</h2>
    <h2 class="chap-chin">پنیر</h2>
    <h2 class="chap-chin">شکر</h2>
</body>
</html>
```

css:
```css
#titr1 {
    background-color: aqua;
}

#titr2 {
    background-color: chartreuse;
}

.chap-chin {
    text-align: left;
}

.rast-chin {
    text-align: right;
}

.kam-rang {
    opacity: 0.5;
}
```

### آموزش box model
<img width="1920" height="1080" alt="box model" src="https://github.com/user-attachments/assets/5a75f596-757f-4fb8-8e5d-db4b862cf46c" />

- محتوای متنی -> content
- فاصله نوشته تا مرز -> padding
- مرز -> border
- فاصله بیرون مرز -> margin

### مرز یا border
با استفاده از `border-style` میتوانید نوع مرز بخش مورد نظر را انتخاب کنید. نمونه:
```css
border-style: none;    /* بدون خط دور */
border-style: solid;   /* خط ساده و یک‌دست */
border-style: dashed;  /* خط خط‌چین (خط‌های کوتاه جدا از هم) */
border-style: dotted;  /* خط نقطه‌چین */
border-style: double;  /* خط دوتایی موازی */
border-style: groove;  /* شیار سه‌بعدی (ظاهر فرو رفته) */
border-style: ridge;   /* برآمده سه‌بعدی (بر عکس groove) */
border-style: inset;   /* ظاهر سه‌بعدی فرو رفته برای کل عنصر */
border-style: outset;  /* ظاهر سه‌بعدی برآمده برای کل عنصر */
border-style: hidden;  /* مشابه none ولی در جدول‌ها رفتار خاص دارد */
```
با استفاده از `border-width` میتوانید ضخامت مرز رو تعیین کنید. مثلا:
```css
border-width: 2px;
```
با استفاده از `border-color` میتوانید رنگ مرز را تعیین کنید. مثلا:
```css
border-color: red;
```
اگر بخواهید برای بالا، پایین، چپ یا راست مرز، شکل های متفاوتی انتخاب کنید میتوانید از استایل های زیر استفاده کنید:
```css
border-top-style: dotted;    /* استایل مرز بالا */
border-right-style: solid;   /* استایل مرز راست */
border-bottom-style: dotted; /* استایل مرز پایین */
border-left-style: solid;    /* استایل مرز چپ */
```
برای گرد کردن گوشه border میتوانید از استایل `border-radius` استفاده کنید. عدد بزرگتر به معنای انحنای بیشتر خواهد بود. مثلا:
```css
border-radius: 5px;
```
### حاشیه بیرونی یا margin
به فضای خالی بیرون تگ margin گفتته میشه. میشه margin همه جهات رو یکجا تعیین کرد. مثلا:
```css
margin: 20px;
```
یا اینکه برای بالا، پایین، چپ یا راست به طور جداگانه تعیین کرد:
```css
margin-top: 100px;     /* فاصله بیرونیِ بالا */
margin-bottom: 100px;  /* فاصله بیرونیِ پایین */
margin-right: 150px;   /* فاصله بیرونیِ راست */
margin-left: 80px;     /* فاصله بیرونیِ چپ */
```
### حاشیه داخلی یا padding
به فضای خالی داخل جعبه که بین content و border قرار میگیره padding میگیم. میتونیم اون رو برای همه جهات یکجا تعیین کنیم. مثلا:
```css
padding: 10px;
```
یا این که برای جهت های مختلف جداگونه تعیین کنیم:
```css
padding-top: 50px;     /* فاصله داخلیِ بالا */
padding-right: 30px;   /* فاصله داخلیِ راست */
padding-bottom: 50px;  /* فاصله داخلیِ پایین */
padding-left: 80px;    /* فاصله داخلیِ چپ */
```
### استفاده از فونت های بیشتر
اگه بخواهید از فونت های متعدد تری استفاده کنید برای مثال میتونید به سایت زیر از گوگل برید و با توجه به دستور عمل های نوشته شده داخلش، یک فونت رو داخل css یا داخل head از html اضافه کنید:
- fonts.google.com
### گرفتن لینک برای سایتی که درست کردیم
میتونید از سایت های زیر استفاده کنید:
- github.com
- cloudflare.com
