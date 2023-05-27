<div dir='rtl' align='right'>

:house: ورشة عمل (6) البدء مع django
===

مقدمة:
---
في هذه الورشة نخرج عن كون البايثون لغة تعمل لوحدها بحيث تقوم بالحسابات ثم تطبع النتائج على الشاشة، هنا نتعرف على أدوات تساعد في جعل البايثون لغة تدعم تكوين مواقع الويب وتساعد في نفس الوقت بالتعامل مع قواعد البيانات.
***

:computer_mouse: شرح برنامج الورشة:
---

ماهو ال Virtual Environment؟
---
البيئة الظاهرية أو ال virtual environment هي عبارة عن بيئة مصغرة عن البيئة التي تعمل بها عادة على نظام التشغيل خاصتك. يمكنك من خلالها أن تعمل بشكل منفصل عن نظام التشغيل والبرامج المثبته عليه من غير أن تؤثر في تلك البرامج.

لكي نفهم أكثر دعونا نأخذ هذه الحالة:
لو فرضنا أن لدينا تطبيق تم تثبيته على جهازنا يدعى Application1 وهذا التطبيق على فرض أنه يتعامل مع twilio النسخة ١ ، وأردنا نحن كمبرمجين بايثون أن نجرب twilio النسخة ٢. لو قمنا بتثبيت twilio نسخة ٢ على الجهاز من المحتمل أن Application1 سيتوقف عن العمل لأن نسخة twilio على النظام تم تبديلها بنسخة أحدث.

![enviroment-chart](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/17.png)

إذا ما العمل بهذه الحالة، يوجد الكثير من البرامج المثبتة على نظام التشغيل خاصتنا قد تتعارض مع نسخ أحدث نريد تجربتها من خلال برامج بايثون؟ في هذه الحالة نقوم فقط بعمل بيئة منفصلة عن بيئة نظام التشغيل تسمى Virtual Environment في داخل هذه البيئة يمكننا أن نثبت نسخ البرامج التي تحلو لنا من غير أن نؤثر على النسخ السابقة لنفس البرنامج على الجهاز.

![enviroment-chart2](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/18.png)

سنرى في تطبيق الورشة في الأسفل كيف ننشئ هذه البيئة الافتراضية VE.
***

ماهو ال django؟
---

لغة البايثون لها استخدامات كثيرة من ضمنها “دعم” بناء مواقع الويب والتعامل مع قواعد البيانات. ولكنها لا تمتلك كافة الأدوات لفعل ذلك فيلزمها ما يسمى بال framework لتسهل مهمتها.

ال django هو أحد هذه ال frameworks التي تسهل عملية بناء مواقع الويب عن طريق استقبال كافة أوامر الويب HTTP Request وتسهل التعامل مع قواعد البيانات وإعادة عرض المعلومات المطلوبة من جديد على صفحات ال HTML وكل ذلك من خلال تطبيق كافة أوامر لغة البايثون التي تعلمتها.

![webdev-chart2](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/19.png)

وال django كبقية البرامج لديه نسخ مختلفة منها لبايثون ٢ ومنها لبايثون ٣، ومن المحتمل أن نعمل على نسخ مختلفة ل django لبرامج مختلفة، فهنا يلزمنا أن نستعمل البيئة الافتراضية عند تثبيت والعمل على django حتى لا يحصل تداخل بين النسخ وأخطاء في نتائج البرامج.

هنا نرى ضرورة تكوين بيئة افتراضية قبل البدء بالعمل على django.
***

تطبيق الورشة:
---
كيفية إنشاء Virtual Environment - VE:
إذا تعرفنا على ال VE سنتعلم كيفية إنشاء هذه البيئة المنفصلة.

أولا يجب أن نقوم بتثبيت ال virtualenv على أجهزتنا من خلال مدير البرامج ال pip، لقد استخدمنا ال pip عندما قمنا بتثبيت ال twilio في درس إرسال الرسائل النصية كما تذكر.

</div>

```sh
pip install virtualenv
```

<div dir='rtl' align='right'>

![installing-virtualenv ](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/20.png)

إذا كانت ال virtualenv مثبتة لديك مسبقا فسيقوم ال pip بتحديثها غير ذلك سيقوم بتثبيتها من البداية.

إذا الأن بعد تثبيت برنامج ال virtualenv نحن جاهزون لكي ننشئ بيئة افتراضية خاصة بنا عن طريق الخطوات التالية:
* إنشاء فولدر للمشروع الخاص بنا
</div>

```sh
mkdir my_new_project 
```

<div dir='rtl' align='right'>

* تفعيل البيئة الافتراضية:
عن طريق أخر أمر virtualenv my_new_ve قمنا بإنشاء فولدر باسم my_new_ve داخل مشروعنا الجديد ليحمل ملفات البيئة الافتراضية الجديدة، داخل هذا الفولدر يوجد مجموعة فولدرات وملفات مختلفة قد تختلف بين Windows و Mac، ما يهمني هنا هو فولدر واحد يحتوى على أمر تفعيل البيئة الافتراضية، في Windows هو Scripts وفي Mac هو bin.

لتفعيل البيئة الافتراضية على Windows من داخل فولدر مشروعنا الجديد نفذ الأمر التالي:
</div>

```sh
c:\my_new_folder> .\ my_new_ve\Scripts\activate
(my_new_ve) c:\my_new_folder>
```

<div dir='rtl' align='right'>
لتفعيل البيئة الافتراضية على Mac من داخل فولدر مشروعنا الجديد نفذ الأمر التالي:
</div>

```sh
$ my_new_folder  . my_new_ve/bin/activate
(my_new_ve) $ my_new_folder
```

<div dir='rtl' align='right'>
إذا تم أمر التفعيل بنجاح سيظهر إسم البيئة الظاهرية my_new_ve تماما قبل اسم الفولدر كما هو ظاهر في الأعلى.

للخروج من هذه البيئة الافتراضية ما عليك إلا أن تعطي هذا الأمر من أي مكان في الترمنال و لا يشترط أن تكون في نفس فولدر المشروع:
</div>


```
deactivate
```

***
<div dir='rtl' align='right'>

إنشاء مشروع جديد من ضمن django:
---

إنشاء وتفعيل بيئة إفتراضية virtualenv خاصة بمشروع django:
---
قم بإنشاء فولدر وبيئة افتراضيه من خلال الأوامر التالية مع تفعيلها:

![v_env-activation](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/21.png)

لاحظ أن البيئة الافتراضية تم تفعيلها وأصبحت تسبق اسم الفولدر (new_ve)
***

تثبيت نسخة django الخاصة ب python 2:
---
الأن أصبحنا داخل بيئة افتراضيه اسمها new_ve، نستطيع الأن أن نثبت ال django لنبدأ العمل عليه، وهناك عدة ملاحظات مهمة هنا، أولا يجب أن نحدد أي نسخة من نسخ ال django يجب تثبتيه لأن أخر نسخة موجودة لا تعمل على بايثون ٢، النسخة من django التي يمكنها أن تعمل مع بايثون ٢ هي 1.11، لذلك سنقوم بالأمر التالي لتثبيت هذه النسخة من ال django بالتحديد، من جديد سنستعمل مدير البرامج pip لهذا الغرض، تأكد أنك داخل ملف المشروع الجديد الذي أنشأناه my_new_project:
</div>

```sh
pip install django==1.11
```

<div dir='rtl' align='right'>

![installing-django](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/22.png)

بهذا يصبح لدينا django framework من ضمن ال VE التي نعمل من خلالها، لتتأكد من ذلك قم بتنفيذ الأمر التالي:

![listing-files](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/23.png)

هل تلاحظ ملف django-admin الموجود في bin فولدر أو في Scripts فولدر علي Windows؟ هذا هو الملف الذي سنستخدمه الأن لإنشاء أول مشروع ل django، تذكر أننا فقط قمنا بتثبيت django ويلزمنا الأن أن ننشئ مشروع نعمل من خلاله.

***
بداية مشروع جديد ل django
---

لبداية مشروع جديد ل django داخل فولدرنا الخاص my_new_project وأيضا داخل بيئتنا الإفتراضية new_ve نبدأ بالأمر التالي:

</div>

```sh
django-admin.py startproject my_project
```

<div dir='rtl' align='right'>

![listing-new-files](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/24.png)

هنا لربما يبدأ البعض بالتخبط من خلال مجموعة الفولدرات التي تم إنشائها، لذلك سأعيد ترتيب الفولدرات:
</div>

```sh
my_new_project: هو الفولدر الرئيس للمشروع الذي يحتوي باقي الفولدرات
new_env: هو الفولدر الخاص بالبيئة الافتراضية
my_django_project: هنا سنضع ملفات مشروعنا بالكامل
```

<div dir='rtl' align='right'>
***
تشغيل django:
---
الان حان الوقت أن نقوم بتشغيل django لأول مرة. نستطيع أن ندخل الأن إلى فولدر my_django_project وننفذ الأمر التالي:
</div>

```sh
python manage.py runserver
```

<div dir='rtl' align='right'>

![running-django](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/25.png)

نلاحظ أن بايثون الأن قام بتشغيل ملف manag.py الخاص ب django مع أمر runserver الذي بدوره سيقوم بتحضير سيرفر محلي local server خاص بمشروعنا مع العنوان المذكور [http://127.0.0.1:8000/](http://127.0.0.1:8000/) وهذا هو عنوان جهازك المحلي 127.0.0.1 مع بورت port 8000 الخاص بمشروعنا. تجاهل الرسالة بالأحمر “You have 13 unapplied…” سنأتي لهذا الأمر لاحقاً.

لنتأكد من أن django يعمل علينا الأن أن نفتح أي متصفح، chrome مثلا ونطبع عنوان برنامجنا هناك:

![testing-django](https://github.com/skahwaji/django-Workshops-Arabic/blob/master/pictures/26.png)

***
رائع جدا ها نحن قمنا بتشغيل أول برنامج django :smile: :tada::confetti_ball::fireworks::sparkler:
---
الأن ما عليك إلا أن تطبق الورشة على فولدر منفصل ليس له علاقة بمشروع حجز الفنادق الخاص بورشاتنا فقط لتتمرن على إنشاء مشاريع جديدة ل django :smile: 

أتمنى التوفيق للجميع من كل :heart: :blush:

</div>
