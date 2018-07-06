<div dir='rtl' align='right'>
 
 # :house: ورشة عمل (7) التعرف على Model Template View - MTV


# مقدمة:
في هذه الورشة نخرج عن كون البايثون لغة تعمل لوحدها بحيث تقوم بالحسابات ثم تطبع النتائج على الشاشة، هنا نتعرف على أدوات تساعد في جعل البايثون لغة تدعم تكوين مواقع الويب وتساعد في نفس الوقت بالتعامل مع قواعد البيانات.

 # :computer_mouse: شرح برنامج الورشة: 

## ما هو ال Model Template View - MTV ؟
فيما يلي فيديو يوضح مبدأ ال MTV:

[![YT](http://img.youtube.com/vi/4LCzQuN457o/0.jpg)](http://www.youtube.com/watch?v=4LCzQuN457o)

## تكوين مشروع django من الصفر ( مراجعة):

[![YT](http://img.youtube.com/vi/kFLSUaq_TGk/0.jpg)](http://www.youtube.com/watch?v=kFLSUaq_TGk)

## فيديو يوضح التعرف على ملفات django:

[![YT](http://img.youtube.com/vi/934LdMzrN3I/0.jpg)](http://www.youtube.com/watch?v=934LdMzrN3I)

## فيديو يوضح مبدأ ال HTTP Request/Response و ال URL Mapping في django:

[![YT](http://img.youtube.com/vi/vIGBfSPfhtY/0.jpg)](http://www.youtube.com/watch?v=vIGBfSPfhtY)

# تطبيق الورشة:
إذا تعرفنا عن طريق الفيديوهات السابقة ما معنى ال MTV  وكيف ننشئ view الذي هو حقيقة عبارة عن دالة داخل البرنامج لنقوم بخدمة ال HTTP Request القادمة من المتصفح عبر ال URL mapping. نريد أن نبدأ بالتطبيق لترسخ المعلومة.

## إحضار ملفات المشروع الحالية:
أولا بعد عمل مشروع ال  django نريد أن نحضر ملفاتنا من الورشات السابقة ال classes:
</div>


    • hotel.py
    • customer.py
    • reservation.py
    • notification.py
    • tester.py
    • main.py

<div dir='rtl' align='right'>
أنشئ فولدر جديد سمه controllers تحت hotel_system، تذكر أن لدينا فولدرين باسم hotel_system أن أتكلم عن الفولدر الثاني الداخلي. 

بعد إنشاء الفولدر قم بنقل كافة ملفاتك  ال classes لهذا الفولدر. 

في نفس الفولدر controllers أنشئ ملف بايثون فارغ `__init__.py` ، هذا الملف يلزمنا لكي نقوم بالإشارة لهذا الفولدر لاحقا من داخل الكود. 

## إضافة  views.py:
. أضف ملف views.py على مشروع ال django لكي نضع الدوال الخاصة بال views في هذا الملف.

. أضف الكود التالي لهذا الملف:

سنقوم بتعريف كافة ملفات ال classes  التي لدينا داخل الفولدر controllers، بفضل الملف `__init__.py` نستطيع أن نستخدم النقطة .  للوصول للملفات داخل الفولدر كما يلي: 
</div>


    from controllers.hotel import *
    from controllers.customer import *
    from controllers.reservation import *
    from controllers.notification import *
    from controllers.main import *
    from controllers.tester import *

    from django.http import HttpResponse


<div dir='rtl' align='right'>

الأن نريد أن ننفذ بعد الدوال التي تعيد قوائم، وهنا يجب أن أذكر نقطة مهمه أعطيتها كملاحظة لمعظم من قام بعمل الورش السابقة، يجب أن لا يكون هناك أمر طباعة print داخل هذه الدوال فقط يجب أن تعيد قوائم، والسبب أن الذي يستدعي الدالة هو مسؤول عن عرض المعلومات، في حالتنا هنا سيكون ال web مسؤول عن عرض المعلومات. 

حسنا ستقوم كل دالة بطلب ال  class الخاص بها لتحضر القائمة المطلوبة، داخل كل دالة يجب عليك أن تستدعي كافة الدوال التي كانت مسؤولة عن تعبئة البيانات المبدئية لفحص الكود سواء كنت وضعتها في main.py  أو في tester.py، يجب أن نفعل ذلك لكل دالة لأننا لم نتعرف على قواعد البيانات بعد :smile:

سأنفذ الدالة الأولى كمثال وأترك الباقي لكم: 

</div>

    def HotelList(request):
        # call the functions to fill all the data about hotels, customers, and reservations
    
        hotel_list_output = "<ul>"
        for h in Hotel.hotel_list:
            hotel_list_output += "<li>" + h.hotel_name + "</li>"
        hotel_list_output += "</ul>"
        return HttpResponse(hotel_list_output)
    
    def HotelInCity(request):
        # call the functions to fill all the data about hotels, customers, and reservations
        # select any city 
        # your code here

    def ReservationList(request):
        # call the functions to fill all the data about hotels, customers, and reservations
        # select any hotel 
        # your code here

 
<div dir='rtl' align='right'>

## إضافة  URL Mapping:
الأن بقي علينا أن نضيف ال url mapping لكي نوجه المتصفح ناحية ال  view الصحيح، في داخل ملف urls.py فلنكتب الكود التالي:
</div>

    from django.conf.urls import url
    from django.contrib import admin
    from .views import  *

    urlpatterns = [
        url(r'^admin/', admin.site.urls),
        url(r"", InitializeData),
        url(r"allhotels", HotelList,
        url(r"hotelincity", HotelInCity),
        url(r"reservationlist", ReservationList)
    ]

<div dir='rtl' align='right'>
الأن حان أن تجرب الكود وتختبر النتيجة :fireworks::sparkler:
نفذ البرنامج عن طريق الأمر التالي أو من خلال VSC:
</div>

    python manage.py runserver

<div dir='rtl' align='right'>
ثم من خلال المتصفح تنقل عن طريق طباعة العناوين التالية:
</div>

    http://127.0.0.1:800
    http://127.0.0.1:800/allhotels
    http://127.0.0.1:800/hotelincity
    http://127.0.0.1:800/reservationlist

