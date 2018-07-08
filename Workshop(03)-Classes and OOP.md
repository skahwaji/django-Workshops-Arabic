<h2>
<p dir='rtl' align='right'>
:construction: ورشة عمل (3) توزيع الكود على Classes وتطبيق OOP
</h2>
</p>

<h2>
<p dir='rtl' align='right'>
 :computer_mouse: شرح برنامج الورشة: 
</p>
</h2>

<p dir='rtl' align='right'>
كما تعلم أن مطور الويب الشامل يكون مسؤول عن كافة أجزاء البرنامج، في هذه الورشة سنقوم بالعمل على الجزء الوسطي Backend Coding الذي يختص بقوانين البرنامج وكيف يعمل، لاحقاً في ورشات أخرى سنتطرق إلى آلية العرض Front-End Coding وآلية تخزين المعلومات .Database 
</p>

<h2>
<p dir='rtl' align='right'>
 :page_with_curl: ملف البرنامج:
</p>
</h2>

 <p dir='rtl' align='right'>
إلى الأن لدينا ملف واحد للبرنامج ألا وهو reservation.py، وفي هذه الورشة سنقوم بتوزيع عملنا على أكثر من ملف
</p>

<h2>
<p dir='rtl' align='right'>
 :wrench:البدء بالعمل على البرنامج:
</p>
<h2>

 <p dir='rtl' align='right'>
في هذه الورشة سنقوم فقط بترتيب برنامجنا على شكل classes بحيث يصبح أسهل للمتابعة والتعديل في المستقبل.
</p>

<h3>
<p dir='rtl' align='right'>
 ما هي الوحدات Entities؟
</p>
</h3>

<p dir='rtl' align='right'>
 كيف يمكن توزيع الكود على ال classes؟ طبعا لا توجد طريقة واحدة وصحيحة إنما يمكننا أن نتبع أفضل الممارسات لفعل ذلك.
</p>
 <p dir='rtl' align='right'>
يجب أن نبحث عن الكيان **Entity**، وهو أي شيء مستقل بحد ذاته له صفات attributes وتجري عليه عمليات  operations. ومن خلال قراءتنا للورشات السابقة نجد أن التعابير التالية قد تشكل كيان مستقلا:
</p>

<p dir='rtl' align='right'>
<br> •	فندق
<br> •	عميل
<br> •	حجز
</p>

<p dir='rtl' align='right'>
ولكن ما رأيك بإرسال الرسائل النصية؟ حقيقة ذلك بحد ذاته قد لا يشكّل كيان منفصل ولكن لو فكرنا به على أنه تابع للتنبيهات notifications يمكننا أن نضمه لوحدة تدعى تنبيهات لأننا نعتقد أننا في المستقبل قد نضيف تنبه بالبريد الإلكتروني أو أي طريقة أخرى، فكلها تنضم في class واحد يدعى تنبهات.
</p>

<p dir='rtl' align='right'>
ولكن هناك شيء لا ينطبق عليه مبدأ الكيان ومع ذلك يمكننا أن نخصص له class لوحده وهو أيضا غير مذكور في جمل الورشات السابقة وهو دوال فحص الكود tester.
</p>

<h3>
<p dir='rtl' align='right'>
 توزع الكود على أكثر من ملف:
</p>
</h3>

<p dir='rtl' align='right'>
حسنا بعد أن عرفنا من يمكنه أن يتحول إلى class يمكننا الأن أن نستخدم أكثر من ملف لهذه ال classes بحيث يأخذ كل class ملف منفصل يحمل فقط كل ما يتعلق بذلك ال class.
</p>

<h3>
<p dir='rtl' align='right'>
 ملف hotel.py:
</p>
</h3>

<p dir='rtl' align='right'>
هنا سنبدأ بتعريف class Hotel وكافة المتغيرات والعمليات المتعلقة به من إضافة وحذف وبحث. 
</p>

<h3>
<p dir='rtl' align='right'>
 ملف customer.py:
</p>
</h3>

<p dir='rtl' align='right'>
هنا سنبدأ بتعريف class Customer وكافة المتغيرات والعمليات المتعلقة به من إضافة وحذف وبحث. 
</p>

<h3>
<p dir='rtl' align='right'>
 ملف reservation.py:
</p>
</h3>

<p dir='rtl' align='right'>
هنا سنبدأ بتعريف class Reservation وكافة المتغيرات والعمليات المتعلقة به من إضافة وحذف وبحث.
</p>

<h3>
<p dir='rtl' align='right'>
 ملف notification.py:
</p>
</h3>

<p dir='rtl' align='right'>
هنا سنبدأ بتعريف class Notification وكافة الدوال الخاصة بالتنبيهات. 
</p>

<h3>
<p dir='rtl' align='right'>
 ملف tester.py:
</p>
</h3>

<p dir='rtl' align='right'>
هنا سنبدأ بتعريف class Tester وكافة الدوال الخاصة بفحص الكود. 
</p>

<p dir='rtl' align='right'>
لاحظ أننا استعملنا الحرف الكبير في بداية ال class والاسم المفرد لتلك ال classes فلم نقل Hotels ولكن قلنا Hotel وذلك من ضمن أفضل الممارسات.
</p>

<h3>
<p dir='rtl' align='right'>
 ملف main.py:
</p>
</h3>

<p dir='rtl' align='right'>
ماذا عن ملف المشروع الرئيسي، يمكننا أن نسميه main.py أو أي اسم أخر، ومن خلاله يمكننا أن نشمل بقية الملفات عن طريق أمر import.
</p>

    “””
        main.py
        This is the main application file for the Hotel Reservation system 
    “””    
    import hotel # when you import you will use the file name not the class name
    import customer
    import reservation
    import tester
    import notification

كل الملفات يجب أن تكون موجودة على نفس الفولدر لتتعرف على بعضها البعض.

<h2>
<p dir='rtl' align='right'>
 تطبيق الورشة
</p>
</h2>

<p dir='rtl' align='right'>
حسنا تعرفنا الأن على ما يمكن أن يكون كيانات منفصلة entities قد تفيدنا في توزيع الكود على classes وتعرفنا على ماهية هذه ال classes والملفات التي تحتويها، علينا الأن فقط أن نقوم بتوزيع الكود الذي تمت كتابته في الورش السابقة على هذه الملفات وال classes بحيث لا يتأثر تنفيذ البرنامج.
</p>

<p dir='rtl' align='right'>
لنأخذ مثال الفندق وسأترك البقية لكم:
</p>

    “””
    hotel.py
    This is the Hotel class file 
    “””    

    class Hotel():
        hotels = []
        def __init__(self, number,hotel_name, city,total_rooms,empty_rooms):
            self.number = number
            self.hotel_name = hotel_name
            self.city = city
            self.total_rooms = total_rooms
            self.empty_rooms = empty_rooms

            Hotel.hotels.append([self.number , self.hotel_name, self.city, self.total_rooms 
            self.empty_rooms])

        def list_hotels_in_city(self, city):
            # search inside Hotel.hotels for hotels in a ‘city’

<p dir='rtl' align='right'>
ملف البرنامج الرئيسي:
</p>

    “””
        main.py
        This is the main application file for the Hotel Reservation system 
    “””    
    import hotel

    def start_app():
        rotana_hotel = Hotel(20,”Rotana”,”Abu Dhabi”,200,40)
        sheraton_hotel = Hotel(21,”Sheraton”,”Abu Dhabi”,300,100)

        print Hotel.hotels
        
    start_app()

<p dir='rtl' align='right'>
هناك ملاحظة أريدك أن تنتبه لها وهي الفرق بين class variable و instance variable:
</p>

<h2>
<p dir='rtl' align='right'>
ال class variable: 
</p>
</h2>

<p dir='rtl' align='right'>
هو متغيّر يتبع ال class على مستوى كافة ال objects التي ستنشأ من هذا ال class، لذلك قمت بتعريف القائمة hotels على مستوى ال class لكي أحتفظ بمعلومات كل الفنادق، هذا لا ينصح به ولكننا لم نتعرف على قواعد البيانات بعد لذلك سنقوم بهذه الحركة مؤقتا.
</p>

<h3>
<p dir='rtl' align='right'>
 ال instance or object variable: 
</p>
</h3>

<p dir='rtl' align='right'>
وهي المتغيرات التي تخص كل نسخة من هذا ال class أي تخص كل فندق لوحده وتم تعريفها داخل الدالة الإبتدائية `__init__`. 
</p>

<h3>
<p dir='rtl' align='right'>
 نصيحة: 
</p>
</h3>

<p dir='rtl' align='right'>
أعرف أنا الموضوع قد يبدو جديدا وبه بعض الإشكالات ولكنني هنا للمساعدة وإذا لم تطبق تلك المعرفة على أرض الواقع فلن تتعلم بالطريقة الصحيحة. إسأل كل الأسئلة التي تخطر ببالك وسأكون معك خطوة خطوة حتى تنفذ هذه الورشة والمشروع بأكمله إن شاء الله :smile: 
</p>

<h3>
<p dir='rtl' align='right'>
 أتمنى التوفيق للجميع من كل :heart: :blush:
</p>
</h3>
