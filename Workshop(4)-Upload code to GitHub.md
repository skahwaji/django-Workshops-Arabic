
<h2>
<p dir='rtl' align='right'>
:construction: ورشة عمل (4) البدء بمشاركة الكود على GitHub 
</p>
</h2>

<h2>
<p dir='rtl' align='right'>
:computer_mouse: شرح برنامج الورشة:
</p>
</h2>

<p dir='rtl' align='right'>
من المهم أن تتعرف على طريقة حفظ إصدارات الكود المختلفة حتى تتابع تقدمك في أي مشروع وخصوصا في الورش التي نعمل عليها حاليا. في هذه الورشة سنقوم بحفظ ملفات برنامجنا على مستودع بعيد لكي يسهل علي متابعة تقدمكم.
</p>

<h3>
<p dir='rtl' align='right'>
:page_with_curl: ملف البرنامج:
</p>
</h3>

<p dir='rtl' align='right'>
في الورشة السابقة تكوّن عندنا مجموعة ملفات، حان الوقت لإدخال إدارة الإصدارات لمشروعنا الصغير :smile: 
</p>

<p dir='rtl' align='right'>
<br> •	hotel.py
<br> • customer.py
<br> • reservation.py
<br> •	notification.py
<br> •	tester.py
<br> • main.py
</p>

![alt text](pictures/1.png "")

<h2>
<p dir='rtl' align='right'>
:wrench:  تطبيق الورشة
</p>
</h2>

<p dir='rtl' align='right'>
في هذه الورشة سنقوم بإضافة ملفات برنامجنا على مستودع محلي local repo ثم سنقوم بترحيل الملفات إلى مستودع بعيد على GitHub: 
</p>

<h3>
<p dir='rtl' align='right'>
إنشاء مستودع repo محلي:
</p>
</h3>

<p dir='rtl' align='right'>
أولا انتقل إلى الفولدر الخاص بالمشروع الذي عملت عليه في الورشات السابقة:
ومن ثم يجب أن ننشئ مستودع محلي local repo  عن طريق الأمر التالي:
</p>

    git init

![alt text](pictures/2.png "")

<h3>
<p dir='rtl' align='right'>
إضافة ملفات البرنامج للمستودع المحلي local repo:
</p>
</h3>

<p dir='rtl' align='right'>
إذا يجب أن ننفذ إضافة الملفات عن طريق الأمر:
</p>

    git add . 

![alt text](pictures/3.png "")

<p dir='rtl' align='right'>
إذا كان هناك  ملفات لا تريد أن تشملها من ضمن الأمر السابق مثل ملفات التوثيق documents أو ملفات نصوص عادية ليس لها علاقة بالكود يمكن إضافتها ل ملف .gitignore
</p>

<p dir='rtl' align='right'>
بعد إضافة الملفات أصبحنا جاهزين لتثبيت الملفات على المستودع المحلي عن طريق:
</p>

    git commit -m “initial commit”

![alt text](pictures/4.png "")

<h2>
<p dir='rtl' align='right'>
: العمل مع المستودعات البعيد
</p>
</h2>


<p dir='rtl' align='right'>
 حان الوقت لنتعرف على توأم جت git ألا وهو GitHub، وهو موقع على الأنترنت يتيح لك من خلال أوامر جت أن تضع تاكود الخاص بك على الإنترنت لتشاركه مع الجميع لأغراض مختلفة.
    </p>
<p dir='rtl' align='right'>
يجب أن نحصل أولا على حساب على جت هب، لإنشاء حساب لك على GitHub إذا لم تكن أنشأت واحدا من قبل تابع الفيديو التالي:
</p>


<iframe width="560" height="315" src="https://www.youtube.com/embed/pJ6RGrdb_uw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


<p dir='rtl' align='right'>
 الأن أصبحنا جاهزون لنقوم بتكوين أول مشروع لنا على GitHub من خلال الخطوات التالية:
</p>

<h4>
<p dir='rtl' align='right'>
 اختر Start a project من الصفحة الرئيسية أو إذا كان لديك مشاريع سابقة فقط اضغط على New repository من الصفحة الرئيسية لحسابك: 
</p>
</h4>

![alt text](pictures/5.jpg "")

 <h4>
<p dir='rtl' align='right'>
 سيطلب منك اسم المشروع، فقط زوده باسم المشروع بدون أي خيارات أخرى ثم اضغط على Create repository:
</p>
</h4>

![alt text](pictures/6.png "")

<p dir='rtl' align='right'>
بعدها ستجد صفحة المشروع الجديد ولأنه فارغ سيعطيك بعض المعلومات لكي تبدأ، إختر HTTPS  كوسيلة للتواصل مع المشروع:
</p>

![alt text](pictures/7.png "")

<p dir='rtl' align='right'>
    وبما إننا لدينا مستودع Repo موجود على فما علينا إلا أن نربط هذا المستودع من GitHub مع المستودع المحلي     Local Repo الذي لدينا عن طريق تنفيذ الأوامر في الصورة أعلاه، طبعا هذه الأوامر لها علاقة بحسابي، يجب عليك أن تنفذ الأوامر الخاصة بك.
</p>

<p dir='rtl' align='right'>
    توجه للمستودع الذي قمت بعمله في وقم بفحص إذا كان مستودعك مرتبط بأي مستودع على الإنترنت Remote Repo:
</p>

![alt text](pictures/8.png "")

<p dir='rtl' align='right'>
إذا لم يظهر شيء بعد أمر git remote تستطيع أن تتأكد بأن المستودع المحلى الذي لديك غير مرتبط بأي مستودع على ال GitHub أو أي سيرفر أخر.
نستطيع الأن أن ننفذ الأوامر التي نسخناها من مشروعنا الجديد على GitHub هذ الأمر سيقوم بربط مستودعنا المحلي مع المستودع البعيد remote repo:
</p>

    git remote add origin https://github.com/shadimac/hotel_reservation.git

![alt text](pictures/9.png "")

<p dir='rtl' align='right'>
الأن بعد الربط  نرى أنه أصبح لدينا فرع جديد يدعى origin:
</p>

<p dir='rtl' align='right'>
نستطيع أن نتأكد من إضافة المستودع من على Remote Repo علي مستودعنا المحلي Local Repo عن طريق الأمر التالي:
</p>

    git log --oneline

![alt text](pictures/10.png "")

<p dir='rtl' align='right'>
ما علينا الأن إلا أن نرسل كافة الملفات التي لدينا من المستودع المحلي إلى المستودع البعيد لغرض تخزينها هناك:
</p>

![alt text](pictures/11.png "")

![alt text](pictures/12.png "")

<p dir='rtl' align='right'>
لن يتم دفع الملفات إلى المستودع البعيد إلا بعد أن يحصل منك على إسم المستخدم وكلمة السر لحسابك على ال GitHub:
</p>

![alt text](pictures/13.png "")

<p dir='rtl' align='right'>
هنا تم قبول أمر رفع الملفات على GitHub ولنتأكد من ذلك نستطيع أن نذهب لموقع GitHub ونتأكد من ذلك فسنجد الملفات مدرجة هناك:
</p>

![alt text](pictures/14.png "")

<p dir='rtl' align='right'>
بهذا أصبحت ملفاتك كلها موجودة على GitHub وتستطيع أن تشاركها مع الجميع، بقي أن تعرف في حين أحدثت تعديل على المستودع المحلي Local Repo ما عليك إلا أن تنفذ الأمر التالي لنقل الملفات إلى المستودع البعيد Remote Repo
</p>

    git push -u origin master


<h3>
<p dir='rtl' align='right'>
أتمنى التوفيق للجميع من كل :heart: :blush:
</p>
</h3>
