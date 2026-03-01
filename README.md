# About 

## العربية :

-  المشروع عبارة عن مجموعة من الأداوت التي تم استخدامها علي مدار سنوات حيث تعتمد الفكرة الأساسية علي عدم تكرار الأكواد التي عادة ما يتم إعادة إستخدامها مثل Request Headers التي يتم إستخدامها في التواصل مع السرفر.
-  مثال أخر خانة المحمول يتم إعدادها مرة واحدة في مكان واحد ويتم إستخدامها في أي input وان حدث اي تغيير لعدد الأرقام يتم ببساطة تعديلها في هذا المكان وتصبح جاهزة للأستعمال.
-  Function Splice From array التي يمكن من خلالها عمل تعديل إلي array 
-  Function Remove From array التي يمكن من خلالها حذف العنصر من array 
-  تحويل التاريخ إلي String بدون الوقت
-  إمكانية إلغاء فتح المستخدم Developer Tools 
-  يمكن عمل صلاحيات Routes فقط وفي هذه الحالة يمكن فتح Route وعمل search لكن بدون إجراء اي تعديل او إضافة
-  أمكانية عمل صلاحية لكل HTML Element 
-  عند فتح أي Route يتم التحقق من الصلاحيات الخاصة بالمستخدم الحالي ويتم عرض المسوح له فقط.
-  عند إرسال أي Request Server يتم التحقق من المستخدم وToken الخاص بيه والتأكد من أن له صلاحية الوصول للـRoute وأيضا قبل إجراء أي عملية يتم  التحقق   من صلاحية هذا المسنخدم من عمل هذا الإجراء.
-  تم إستخدام Lazy Loading.
-  يدعم Localization عربي وانجليزي مع إمكاينة إضافة لغات إخري.
-  الرسائل الواردة من السرفر يتم إهتمادها علي أساس Request Accepting Languages ويتم عرضها مباشرة للمستخدم
-  يتم عرض Spinner في حالة ارسال الطلب للسرفر وفي انتظار الرد
-  Pagination يتم عرضه تلقائيا عند الحالة عليه ويمكن إعداد الحد المطلوب مثل getAll ,Search ويمكن إضافة قيم اخري علي حسب الحاجة.
-  التصميم Responsive وويظهر علي المحمول والكمبيوتر بنفس الشكل.
- إممكانية تصدير البيانات للأكسل في جميع الشاشات.
- موديول material يتم فيه تعريف جميع الموديولات الخاصة ب Angular Material وتصديرها ليتم اسستخدامها في النظام بالكامل بدلا من استيراد الموديول المطلوب في كل شاشة.
- موديول nav ويتم فيه عمل القائمة ويمكن تعديله ليتناسب مع الاختياج الشاشات التي تحتاج لتسجيل دخول وأيضا الشاشات التي لاتحتاج لذلك.
- موديول Shared 
    - يحتوي علي مجلد Common ويحتوي علي الملفات التالية :
        - apps-names  حيتم استخدامها ديناميكيا بدلا من Hard code في service و الصلاحيات.
        - decode-token يتم فيه فك تشفير Token الوارد من السرفر ويتم استخدمه في كل App او Component لتحديد الصلاحيات الخاصة بالمستخدم.
        - export-to-excel Function يتم من خلالها عمل تصدير البيانات للأكسل.
        - hash-string طريقة مبسطة جدا كمثال علي تشفير Token والصلاحيات وال Routesالخاصة بالمستخدم .
        - inputs-length يتم فيه تحديد القيم المطلوبة والتي يمكن استخدامها في اكتر من مكان في النظام كالمحمول مثلا.
        - meta يمكن من خلالها عمل SEO البيانات الخاصة با بكل صفحة مع عرضها باللفة المطلوبة.
        - paginantion يتم فيها تعريف القيم الفاتراضية الخاصة بعدد البيانات المطلوبة من السرفر فيحالة البحث مثلا.
        - permissions-names - يتم فيها كتابة اسماء الصلاحيات الخاصة بالنظام ويتم استخدامها في عناصر HTML.
        - routes-names - يتم فيها تعريف Routes أو العناوين الخاصة بالنظام ويتم استخدامها أيضا في تحديد صلاحية المستخدم لعنوان معين.
        - set-meta-language - يتم فيها تعريف  البيانات المطلوبة لتاجات Meta الخاصة SEO.
        - site - يحتوي علي مجموعة من المهام والتعريفات مثل حذف عنصر من مصفوفة او تعديل عنصر في مصفوفة  أو انواع الاجراء المطلوب من إضافة وحذف وتعديل وبحث وحذف وايضايتم استخدامه في تعريف روابط api الخاصة بالسرفر.
        - validation-input-data -يتم استخدامه في حالة التأكد من بيانات المستخدم وإظهار رسائل قبل إرسال الRequest للسرفر .
        - validaton-response -يتم فيه التحقق من كل رد قادم من السرفر ويتم استخدامه في جميع Api's حيث يتم التحقق من الرد وعرض الرسائل للمستخدم علي حسب اللغه المستخدمة ويدعم اللغتين العربية والانجليزية.
    - Component يحتوي علي :
        - Paginator .
        - spinner
    - interfaces يحتوي علي : 
        - موديل البيانات الخاصة باللغة.
        - موديل البيانات الخاصة ب Meta Tag (قيد التطوير حاليا)
        - response-pagination-data -خاص ببيانات pagination الواردة من السرفر.
        - token-values -القيم الخاصة بالتوكين.
        - token البيانات الخاصة بالتوكن.
    - services ويحتوي علي :
        - auth-guard والذي يستخدم للتحقق من صلاحية المستخدم لفتح Route أو عنوان معين.
        - definitions-service تستخدم في service الخاصة من السرفر التي لاتحتاج إلي Component مثل اللغات.
        - dialog-service -يتم فيها تعريف الكيفية التي تعمل بها models الخاصة بالangular material model مع تحديد كيفية عملها CSS.
        - notification-service -تعتمد علي toaster والتي يتمكن من خلالها إظهار الرسائل للمستخدم.
        - set-app-name يتم تحديد component او app الحالي مع عرض إسمه في navbar بالاسم علي حسب اللغة الحالية للمستخدم.
        - set-title يتم فيها تعديل عنوان التاب الحالية.

- كل موديول يحتوي علي المجلدات التالية :
    - Compoents  والتي يتم فيها عمل الصفحة.
    - Configs  يتم تحديد Route الخاص بكل Component مع إمكانية تعديله في أي وقت.
    - InterFaces ويتم فيها تعريف Data Model للـ Component.
    - Service ويتم فيه تعريف Routes الخاصة Api's.
    - يتم تعريف ملف index.ts لجميع المجلدات السابفة علي أن يتم تصديرها لملف index.ts رئيسي للموديول.


## English :
- The project is a set of tools that have been used over the years, where the basic idea depends on not repeating codes that are usually reused, such as Request Headers, which are used to communicate with the server.
- Another example is the mobile field. It is set up once in one place and is used in any input. If there is any change in the number of numbers, it is simply modified in this place and becomes ready for use.
- Function Splice From array, through which you can make modifications to the array.
- Function Remove From array through which the item can be deleted from the array.
- Convert date to String without time.
- Possibility to unlock the Developer Tools user.
- Only Routes permissions can be created. In this case, a Route can be opened and a search can be performed, but without making any modifications or additions.
- The ability to create a validity for each HTML Element.
- When opening any Route, the permissions of the current user are verified and only those authorized are shown.
- When sending any Request Server, the user and his Token are verified and made sure that he has access to the Route. Also, before performing any operation, the user’s authority to perform this procedure is verified.
- Lazy Loading is used.
- Localization supports Arabic and English, with the ability to add other languages.
- Messages received from the server are processed based on Request Accepting Languages and displayed directly to the user.
- Spinner is displayed if the request is sent to the server and is waiting for a response.
- Pagination is automatically displayed when the status is on, and the required limit can be set, such as getAll, Search, and other values can be added as needed.
- Responsive design and it appears on mobile and computer in the same way.
- The possibility of exporting data to Excel in all screens.
- Material module in which all Angular Material modules are defined and exported to be used in the entire system instead of importing the required module in each screen.
- Nav module, in which the menu is created and can be modified to suit the needs of screens that need to log in, as well as screens that do not.
- Shared module
     It contains the Common folder and contains the following files:
         - apps-names will be used dynamically instead of the hard code in service and permissions.
         - decode-token In which the token received from the server is decrypted and used in each App or Component to determine the user's permissions.
         - export-to-excel Function through which data is exported to Excel.
         - hash-string A very simplified method as an example of a user's Token encryption, permissions, and Routes.
         - inputs-length In which the required values are specified, which can be used in more than one place in the system, such as the mobile.
         - Meta, through which SEO can generate data for each page and display it in the required format.
         - paginantion, in which the default values are defined for the number of data requested from the server in the case of a search, for example.
         - permissions-names - The system permission names are written and used in HTML elements.
         - routes-names - defines the routes or addresses of the system and is also used to determine the user's authority to a particular address.
         set-meta-language - Defines the data required for SEO Meta tags.
         - site - It contains a set of tasks and definitions, such as deleting an element from an array, modifying an element in an array, or the types of actions required, such as adding, deleting, modifying, searching, and deleting. It is also used in defining the server’s API links.
         - validation-input-data - It is used to verify user data and show messages before sending the request to the server.
         - validaton-response - in which each response coming from the server is verified and used in all API's where the response is verified and messages are displayed to the user according to the language used and it supports both Arabic and English.
     Component contains:
         -Paginator.
         -spinner
     - interfaces contains:
         Language data model.
         - Meta Tag data model (currently under development)
         - response-pagination-data - for pagination data received from the server.
         token-values - the values of the token.
         - token data for the token.
     - services and contains:
         - auth-guard which is used to verify that the user is authorized to open a particular route or address.
         - definitions-service is used in a special service of the server that does not need a component, such as languages.
         - dialog-service - It defines how the angular material model works, along with specifying how CSS works.
         - notification-service - It depends on the toaster, through which messages can be shown to the user.
         - set-app-name The current component or app is identified and its name is displayed in the navbar by name according to the user’s current language.
         - set-title in which the title of the current tab is modified.
- Each module contains the following folders:
    - Compoents in which the page is created.
     - Configs The Route for each Component is determined with the possibility of modifying it at any time.
     - InterFaces, in which the Data Model of the Component is defined.
     - Service, in which the API's Routes are defined.
     - An index.ts file is defined for all previous folders and is exported to a main index.ts file for the module.

# Dependencies
- Angular Ver 16.
- Angular Material 16.
- Bootstrap 5.3.
- Xlsx.
- toaster.
- prettier.
- eslint.

# Contact
    Email: BaherHamed@gmail.com;
    whatsapp: +2001001185518






