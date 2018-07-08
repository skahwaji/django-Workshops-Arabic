<div dir='rtl' align='right'>

:construction: ورشة عمل (5) تعرّف على Visual Studio Code
===

تلخيص للورشات السابقة:
---
قمنا بالورشات السابقة التالية لحد الأن:

* [ورشة عمل (1) : بناء نظام بسيط لحجز الفنادق](https://github.com/shadimac/django-Workshops-Arabic/blob/master/Workshop(1)-Lists%20and%20Loops.md)
* [ورشة عمل (2) :إضافة إمكانية تأكيد الحجز عن طريق الرسائل](https://github.com/shadimac/django-Workshops-Arabic/blob/master/Workshop(2)-Send%20SMS.md)
* [ورشة عمل (3) توزيع الكود على Classes وتطبيق OOP](https://github.com/shadimac/django-Workshops-Arabic/blob/master/Workshop(3)-Classes%20and%20OOP.md)
* [ورشة عمل (4) البدء بمشاركة الكود على GitHub](https://github.com/shadimac/django-Workshops-Arabic/blob/master/Workshop(4)-Upload%20code%20to%20GitHub.md)

:computer_mouse:  شرح برنامج الورشة:

معظمكم سيبدأ يتساءل لماذا يجب أن نتعلم محرر جديد New Code Editor، وما الذي يفعله محرر لمايكروسوفت مع البايثون!

حسنا أولا أنت كمبرمج يجب عليك أن تكون على إطلاع على الأقل بمختلف الأدوات التي تحيط بك، لربما لا يجب أن تستعمل كل الأدوات ولكن على الأقل تتعلم الفرق بينها وما الذي يميز واحدة عن الأخرى أو حتى متى يمكنك أن تعمل على هذه أو تلك.

***
نبذة عن توجه Microsoft:
---

قامت شركة مايكروسوفت منذ مدة بعيدة بالتوجه نحو البرامج مفتوحة المصدر لكي ترضي أذواق المتعاملين في مجال برامج الكمبيوتر حول العالم الذين يريدون أن يحرروا البرامج ويجعلوها متاحة للجميع من ناحية استخدام ومن ناحية المصدر (Source Code) أي أن أي شخص مبرمج أو جهة مسؤولة عن تبني البرامج لها أن تطّلع على الكود الخاص بالبرنامج وحتى أن تقوم بالتعديل عليه وإنشاء نسخة جديدة محسنة أو حتى ذات ميزات جديدة.

أول خطوات مايكروسوفت كانت عند إنشائها للغة C# التي تعتبر أول لغة لمايكروسوفت مفتوحة المصدر أي تستطيع أي شركة أن تبني محرر للكود (Code Editor) ليقرأ ويترجم البرامج المكتوبة ب #C أي أن لغة من لغات مايكروسوفت أصبحت لا تعتمد فقط على MS Visual Studio كمحرر وحيد وأيضا لا تعتمد على Windows كنظام تشغيل.

ولكن هذا لم يكن كافياً ليقنع العالم أن مايكروسوفت فعلا جادة في التوجه للكود مفتوح المصدر.

بعد ذلك قامت الشركة بخطوة جريئة جدا وهي تحرير مكتبة البرامج الخاصة بها .NET Library لتصبح مفتوحة المصدر وأعطتها اسم جديد .NET Core بذلك أصبحت تستطيع الأن أن تنفذ وتبرمج برامج كاملة لميكروسوفت على محرر أكواد غير Visual Studio أو نظام تشغيل غير Windows.

وأخيرا ومنذ أيام قامت مايكروسوفت [ بالاستحواذ على أكبر موقع لاحتضان البرامج مفتوحة المصدر في العالم GitHub.](https://blog.github.com/2018-06-04-github-microsoft/)

***
ماذا عن Visual Studio Code - VSC؟
---
من ضمن الأدوات التي قدمتها مايكروسوفت للتوجه نحو دعم البرامج مفتوحة المصدر هو إنشائها لمحرر أكواد جديد (Code Editor) وقامت بتسميته تيمناً بالمحرر العريق Visual Studio وأضافت عليه كلمة Code، فأصبح [Visual Studio Code.](https://code.visualstudio.com/)

هذا المحرر خرج ليكون متاحاً على Windows و Linux و Mac وليكون أيضا محرر أكواد للكثير من اللغات، وأيضا ليحتضن امتدادات Extensions يستطيع المبرمجون حول العالم أن ينتجوها وتصبح جزءاً من هذا المحرر.

فإذا هو محرر جديد وخفيف وسريع ويدعم معظم اللغات الموجودة حاليا وعلى رأسها بايثون:

![vscode-extensions](https://github.com/abo3adel/django-Workshops-Arabic/blob/master/pictures/15.jpg)

ومن ضمن ميزاته أنه يسهل عملية التعامل مع برنامج إدارة الإصدارات git من خلال أوامر تنفذ من خلال قوائم كما سنرى في هذه الورشة.

والأهم من ذلك كله أن هذا المحرر (Code Editor) مجاني :smiley:

***
تطبيق الورشة:
---
أولا دعونا نحمّل البرنامج من هذا الموقع [code.visualstudio.com/](https://code.visualstudio.com/) وقم باختيار نظام التشغيل الخاص بك لذلك.

***
١. بايثون على VSC:
---
بعد تحميله يمكنك أن تتابع الفيديو التالي لنرى كيف يمكننا أن نحضّر VSC ليكون جاهزا لبرامج بايثون:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=_TAxNfwGznA
" target="_blank"><img src="http://img.youtube.com/vi/_TAxNfwGznA/0.jpg" 
alt="vscode init" width="360" height="240" border="10" /></a>

إذا هذه هي الامتدادات Extensions التي احتجناها أثناء تعريف VSC على لغة البايثون:
Material Icon Theme
Python

ملاحظة قد يظهر لك رسالة تخبرك عن وجود امتداد يهمك ليتم تثبيته، وهذه الرسائل قد تظهر كثيرا كلما اكتشف VSC أن هناك Extension يساعدك على العمل:

![vscode-pylint-error](https://github.com/abo3adel/django-Workshops-Arabic/blob/master/pictures/16.png)

هنا يخبرك بأن Python Linting أي الامتداد الذي يساعدك على اكتشاف الأخطاء أثناء كتابة الكود غير موجود، هل تريد أن تثبته؟ ما عليك إلا أن تختار Install وتنتظر حتى ينتهي من تثبيت ال Python Linting.

***
٢. تتبع برنامج بايثون وتصحيح الأخطاء على VSC:
---
والفيديو التالي سيقوم بتعريفك على آلية تتبع برامج بايثون لتصحيح الأخطاء من خلال VSC:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=CNC6v-hLmA8
" target="_blank"><img src="http://img.youtube.com/vi/CNC6v-hLmA8/0.jpg" 
alt="error handling with vs code" width="360" height="240" border="10" /></a>

***
٣. تعرف على git مع VSC:
---
وفي الفيديو التالي سنتعرف على أوامر git من خلال ال Terminal ومن خلال القوائم في VSC:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=5ntbprnXtiI
" target="_blank"><img src="http://img.youtube.com/vi/5ntbprnXtiI/0.jpg" 
alt="error handling with vs code" width="360" height="240" border="10" /></a>

***
الخلاصة:
---
إذا إعتمدت على VSC في برمجة البايثون سيكون لديك حرية في استخدام الامتدادات التي تدعم البايثون والتي هي في تطور مستمر وسيكون استخدام أوامر git أسهل مما تتصور.

أتمنى التوفيق للجميع من كل :heart: :blush:


</div>
