
 # :construction: ورشة عمل (1) القوائم والتكرار Lists and Loops 

# :computer_mouse: شرح برنامج الورشة: 

 <p dir='rtl' align='right'>
كما تعلم أن مطور الويب الشامل يكون مسؤول عن كافة أجزاء البرنامج، في هذه الورشة سنقوم بالعمل على الجزء الوسطي Backend Coding الذي يختص بقوانين البرنامج وكيف يعمل، لاحقاً في ورشات أخرى سنتطرق إلى آلية العرض Front-End Coding وآلية تخزين المعلومات .Database 
</p>

# :open_file_folder: تجهيز فولدر المشروع:
 <p dir='rtl' align='right'>
علينا بداية تخصيص فولدر معين لهذا المشروع، قم بتخصيص فولدر على جهازك لهذا المشروع
</p>

# :page_with_curl: تكوين ملف البرنامج:
 <p dir='rtl' align='right'>
في هذه المرحلة البرنامج سيكون في ملف واحد للحجوزات لنسميه reservation.py
</p>

# :wrench:البدء بالعمل على البرنامج:
 <p dir='rtl' align='right'>
في البداية ليس لدينا قاعدة بيانات وسنقوم بتخزين كل شيء داخل البرنامج كقيم مبدئية، من خلال القوائم List أو أي متغيرات أخرى تعلمناها لبناء قاعدة بيانات مصغرة داخل البرنامج
</p>

<p dir='rtl' align='right'>
سيطلب من البرنامج بتنفيذ الأوامر التالية بإمكاننا تسميتها
</p>

[User Stories قصة المستخدم](https://ar.wikipedia.org/wiki/%D9%82%D8%B5%D8%A9_%D8%A7%D9%84%D9%85%D8%B3%D8%AA%D8%AE%D8%AF%D9%85)

<p dir='rtl' align='right'>
من خلالها نتعرف على متطلبات المستخدم وكيف يريد أن يستفيد من البرنامج في هذه المرحلة (لن أذكر كل المطلوب الأن فقط خطوات صغيرة لنبدأ):
</p>

<p dir='rtl' align='right'>
<br> • إضافة فندق جديد
<br> • عرض كافة الفنادق المتاحة في مدينة معينة
<br> • طلب الغرف الشاغرة في فندق معين من القائمة
<br> • عرض الحجوزات لفندق معين
<br> • طلب الحجز في أحد الفنادق حسب الشواغر 
<br> • طباعة تأكيد الحجز إذا تم الحجز مع التوقيت
<br> • طباعة رفض الحجز إذا كان الفندق لا يملك شواغر
</p>

### يجب أن تتوافر المعلومات التالية عن كل فندق:

<p dir='rtl' align='right'>
<br> • اسمه hotel_name 
<br> • المدينة التابع لها city 
<br> • عدد الغرف ككل total_rooms 
<br> • عدد الغرف الشاغرة empty_rooms 
</p>

<p dir='rtl' align='right'>
في هذه المرحلة نريد أن نطبق ما تعلمناه في الجزء الثاني من المادة أي حتى درس ١٣ تقريبا لا يهم كثيرا تشكيل قاعدة البيانات داخل البرنامج وفاعليتها أو حتى طريقة الطباعة ما يهمنا هو أن يؤدي البرنامج المطلوب منه.
</p>

# تطبيق الورشة
<p dir='rtl' align='right'>
بما أنه ليس لدينا قاعدة بيانات فكل ما نستطيع فعله الأن هو استخدام القوائم لحفظ المعلومات
</p>

### قائمة الفنادق  hotels list:
<p dir='rtl' align='right'>
يلزمنا قائمة للفنادق تحفط المعلومات لكل فندق والتي سنجري عليها كل العمليات من كتابة وقراءة، قد تحتوي هذه القائمة الرئيسية على قوائم فرعية تمثل كل فندق على حدة، تحمل المعلومات عن الفندق المذكورة أعلاه.
</p>

### قائمة الزبائن customers list :
<p dir='rtl' align='right'>
يلزمنا قائمة للزبائن تحمل معلومات كل زبون، الأن نريد فقط اسم الزبون 
</p>

### قائمة الحجوزات  reservation list:
<p dir='rtl' align='right'>
وهنا نقوم بكتابة كل الحجوزات للفنادق في قائمة منفصلة، هنا نحتاج فقط لرقم الفندق ورقم الزبون وتفاصيل الحجز من تاريخ إلى تاريخ
</p>

## العمليات المطلوبة:

### إضافة فندق جديد:

    def add_hotel(number,hotel_name, city,total_rooms,empty_rooms):
        # add number,hotel_name, city,total_rooms,and empty_rooms to hotels list

### إضافة زبون جديد:

    def add_customer(customer_name):
        # add customer_name to customers list

### إضافة حجز جديد:


    def reserve_room (hotel_name, customer_name)
        # loop and check if there is empty_rooms in hotel_name 
        # if no rooms, 
        #     return False
        # else reserve a new room in hotel_name for customer_name
        #         add new reservation into the reservation list
        #          update the empty rooms in hotel_name
        #          return True

    def add_new_reservation(hotel_name, customer_name)
        # if reserve_room(hotel_name, customer_name) 
        #        add hotel_name, customer_name into the reservations list
        #       print “confirmation”
        # else
       #      print “sorry no rooms available”

### عرض الفنادق في مدينة معينة:

    def list_hotels_in_city(city_name):
        # search for city in hotels and print hotel name, total number of rooms if found

### عرض الحجوزات لفندق معين:

    def list_resevrations_for_hotel(hotel_name)
        # search for hotel_name in reservation list and print customer name
        
<p dir='rtl' align='right'>
### أتمنى التوفيق للجميع من كل :heart: :blush:
</p>

