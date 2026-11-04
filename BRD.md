# وثيقة متطلبات الأعمال (BRD)

## نظام إدارة الإنتاجية الشخصية والمعرفة

**نوع الوثيقة:** وثيقة متطلبات الأعمال (Business Requirements Document)  
**الإصدار:** 1.0  
**الحالة:** اكتمل جمع المتطلبات / جاهز للمراجعة  
**إعداد:** Business Analyst  
**التاريخ:** 27 سبتمبر 2026

---

# 1. الملخص التنفيذي

هذا المشروع عبارة عن نظام شخصي لإدارة الإنتاجية والمعرفة، مصمم لتجميع وإدارة أعمال المستخدم اليومية، والعملاء، والمهام، والتعلم، والمعرفة، والملفات، وسجل الأنشطة، والإشعارات، والسجلات المرتبطة بها في مكان واحد.

القيمة الأساسية للنظام هي:

> عندما يفتح المستخدم النظام، يعرف فورًا ما الذي يحتاج إلى تنفيذه، وما الذي يحتاج إلى متابعة، وما الذي يحدث مع العملاء، وما الذي يتعلمه حاليًا.

النظام يهدف إلى تقليل التشتت الناتج عن استخدام أدوات منفصلة لإدارة المهام، والملاحظات، والملفات، والكورسات، وسجلات العملاء، وسجل الأنشطة.

يجب أن يكون النظام متجاوبًا على الكمبيوتر والموبايل، وأن تكون لغة الواجهة الإنجليزية مع دعم كتابة المحتوى بالعربية والإنجليزية، مع توفير الوضع الفاتح والداكن، والعمل بدون إنترنت، والمزامنة، والنسخ الاحتياطي، والتصدير، والاستعادة، والبحث، والإشعارات، وسلة محذوفات موحدة.

---

# 2. المشكلة التجارية

يحتاج المستخدم إلى إدارة عدة أنواع من المعلومات والعمل، منها:

- المهام اليومية والمتكررة.
- العمل والمتابعة مع العملاء.
- التعلم والكورسات.
- المعرفة المكتسبة من التعلم والعمل.
- الملفات المهمة.
- اتفاقات العملاء وسجل العمل معهم.
- سجل الأنشطة الشخصية.
- الإشعارات والتذكيرات.

بدون نظام مركزي، يمكن أن تصبح هذه المعلومات مشتتة وصعبة المتابعة.

لذلك يجب أن يوفر النظام مساحة عمل موحدة يستطيع المستخدم من خلالها:

1. معرفة ما يجب تنفيذه.
2. إدارة المهام بالتفصيل.
3. إدارة علاقات العملاء وسجل العمل معهم.
4. متابعة الكورسات والتعلم.
5. تحويل ما يتعلمه إلى Knowledge قابلة للبحث.
6. تخزين وتنظيم الملفات المهمة.
7. البحث في النظام بالكامل.
8. الاحتفاظ بالسجل التاريخي للأنشطة.
9. استعادة المعلومات المحذوفة.
10. عمل Backup وRestore للنظام بالكامل.

---

# 3. أهداف العمل

## 3.1 الأهداف الأساسية

- تجميع معلومات العمل والإنتاجية الشخصية في نظام واحد.
- جعل Tasks هي مركز التنفيذ الأساسي.
- توفير Dashboard توضح الأولويات فور فتح النظام.
- الاحتفاظ بسجلات منظمة للعملاء وتاريخ التعامل معهم.
- توفير Learning Tracker بسيط وفعال.
- تحويل التعلم إلى Knowledge قابلة لإعادة الاستخدام والبحث.
- تجميع الملفات المهمة.
- تقليل إدخال البيانات المتكرر من خلال Quick Add وTemplates وRecurring Tasks والأتمتة.
- تسهيل الوصول للمعلومات التاريخية واستعادتها.
- حماية البيانات من خلال Backup وRestore وTrash وRecovery.

## 3.2 أهداف إضافية

- دعم استخدام الكمبيوتر والموبايل.
- دعم العمل بدون إنترنت والمزامنة بعد عودة الاتصال.
- توفير بحث شامل وسريع داخل المحتوى.
- السماح بتكاملات مستقبلية عند إمكانية تنفيذها تقنيًا.
- الحفاظ على واجهة بسيطة وقابلة للتخصيص بدون تعقيد غير ضروري.

---

# 4. المستخدم / الجهات المتفاعلة

## 4.1 المستخدم الأساسي

يوجد مستخدم أساسي واحد فقط.

النظام مصمم كتطبيق **Single-User**.

## 4.2 تسجيل الدخول

تسجيل الدخول باستخدام Email/Password غير مطلوب في الـMVP.

لكن قد تكون هناك حاجة إلى طبقة أمان حسب طريقة نشر النظام واستخدام التخزين السحابي.

---

# 5. اللغة والتوطين

## 5.1 لغة الواجهة

لغة واجهة النظام ستكون **English فقط**.

لا يوجد Language Switcher في الـMVP.

## 5.2 محتوى المستخدم

يجب أن يدعم النظام:

- العربية.
- الإنجليزية.
- المحتوى المختلط عربي/إنجليزي.
- Unicode.

ويشمل ذلك Tasks وNotes وClients وKnowledge وAgreements وActivities وبيانات الملفات وغيرها.

## 5.3 المنطقة الزمنية

النظام يستخدم **توقيت مصر** كمنطقة زمنية ثابتة.

---

# 6. المنصات وتجربة الاستخدام

يجب أن يدعم النظام:

- Desktop.
- Mobile.
- Responsive UI.
- Light Mode.
- Dark Mode.
- اختيار الثيم يدويًا.
- PWA.
- العمل بدون إنترنت.
- المزامنة تلقائيًا بعد عودة الاتصال.

يمكن للمستخدم عمل Reset يدوي لـ:

- ترتيب الـDashboard.
- إعدادات النظام.

إعادة ضبط الإعدادات لا تحذف بيانات المستخدم.

---

# 7. أولوية الـMVP

ترتيب الأولويات الذي حدده المستخدم:

1. **Tasks**
2. **Dashboard**
3. **Learning**
4. **Clients**
5. **Files**

وتوجد Modules داعمة:

- Knowledge
- Activity History
- Notifications
- Trash
- Settings
- Backup / Export / Restore
- Global Search

---

# 8. التنقل الرئيسي

القائمة الجانبية (Sidebar) تحتوي على:

1. Dashboard
2. Tasks
3. Clients
4. Learning
5. Knowledge
6. Files
7. Activity History
8. Trash
9. Settings
10. Notifications Center

---

# 9. متطلبات الـDashboard

## 9.1 الهدف

الـDashboard هي نقطة الدخول الأساسية للنظام، ويجب أن تجيب على سؤال:

> ماذا أحتاج أن أفعل الآن؟

## 9.2 مكونات الـDashboard

تحتوي على:

- ملخص المهام.
- قائمة المهام كاملة.
- Urgent Tasks.
- Today.
- Overdue.
- Upcoming.
- Learning Widget.
- Client Widget.
- Client Recent Activity.
- Quick Add.
- Active Timer.

## 9.3 ملخص المهام

يظهر ملخص مختصر مثل:

- Today.
- Overdue.
- Urgent.
- Upcoming.

ثم تظهر قائمة المهام الفعلية.

## 9.4 قائمة المهام الكاملة

يجب أن تكون جميع المهام النشطة متاحة من الـDashboard.

المستخدم يريد ظهور القائمة كاملة حتى لو كان عدد المهام كبيرًا.

استخدام Scroll مقبول.

## 9.5 المهام العاجلة

يجب أن تكون Urgent Tasks واضحة جدًا في الـDashboard بغض النظر عن تاريخ استحقاقها.

## 9.6 تخصيص الـDashboard

يمكن للمستخدم:

- إظهار أو إخفاء Widgets.
- إعادة ترتيب الـWidgets باستخدام Drag & Drop.
- حفظ الترتيب تلقائيًا.
- إعادة الـDashboard للوضع الافتراضي.

## 9.7 Learning Widget

الـLearning Widget قابل للتخصيص.

يمكن للمستخدم اختيار المعلومات التي تظهر، مثل:

- Courses to Learn.
- Completed Courses.
- معلومات تعلم أخرى مناسبة.

لا يوجد Recent Knowledge كـWidget في الـDashboard.

## 9.8 Client Widget

الـClient Widget ثابت وليس قابلًا للتخصيص.

## 9.9 Recent Activity

الـRecent Activity الموجودة في الـDashboard مخصصة لأنشطة العملاء فقط.

أما General Activity History فلا تظهر في هذا الـWidget.

## 9.10 Quick Add

يوجد Quick Add مباشرة من الـDashboard:

- + Task
- + Client
- + Course
- + Knowledge
- + Activity

Keyboard Shortcuts غير مطلوبة.

---

# 10. وحدة Tasks

الـTasks هي الوحدة الأساسية في النظام.

## 10.1 طرق عرض المهام

تدعم:

- Sheet/List View.
- Calendar View.
- Completed Tasks History.
- Task Templates.

## 10.2 نموذج قائمة المهام

جميع المهام تظهر في قائمة موحدة.

لا توجد قوائم منفصلة لـ:

- Client Tasks.
- Personal Tasks.
- Learning Tasks.

حقل Client اختياري.

## 10.3 بيانات المهمة

يمكن أن تحتوي المهمة على:

- Task Name.
- Client اختياري.
- Priority.
- Due Date اختياري.
- Due Time اختياري.
- Notes / Rich Content.
- Status.
- Tags.
- Comments / Updates.
- Subtasks.
- Estimated Time.
- Actual Time.
- Recurrence.
- Attachments.

## 10.4 الأولوية

Priority إجباري عند إنشاء Task.

القيم:

- Urgent
- High
- Medium
- Low

لا توجد قيمة افتراضية.

## 10.5 الحالة

قيم Status:

- To Do
- In Progress
- Done

يمكن تغيير Status مباشرة من:

- Task List.
- Calendar.

## 10.6 المهام المكتملة

عند تحويل Task إلى Done:

- تختفي من قائمة المهام النشطة.
- تنتقل إلى Completed Tasks History.
- تحتفظ بكل تفاصيلها الأصلية.

يمكن إعادة Task مكتملة إلى:

- To Do.
- In Progress.

## 10.7 تاريخ الاستحقاق

Due Date اختياري.

Task بدون Due Date لا تحصل على تذكيرات مرتبطة بتاريخ الاستحقاق.

## 10.8 تذكيرات المهام

تدعم:

- Default Reminder Time من Settings.
- Custom Reminder لكل Task.
- تذكير قبل يوم.
- تذكير في يوم الاستحقاق.
- إشعارات للمهام المتأخرة وفق سلوك النظام المتفق عليه.
- إشعار أقوى للـUrgent Tasks.

الإشعارات تصل عبر:

- Notifications Center.
- Mobile Push Notifications.

## 10.9 Urgent Tasks

المهام العاجلة:

- تحصل على إشعارات أقوى وأكثر وضوحًا.
- تظهر بشكل بارز في Dashboard.
- تظل ظاهرة كـUrgent بغض النظر عن Due Date.

## 10.10 المهام المتكررة

تدعم:

- Daily.
- Weekly.
- Monthly.

وتدعم:

- Start Date.
- End Date.
- Stop Recurrence.
- علامة مرئية توضح أنها Recurring.

إذا لم يوجد End Date، تستمر المهمة حتى يتم إيقاف التكرار.

### Daily

يمكن للمستخدم:

- اختيار أيام محددة.
- أو عدم اختيار أي أيام، وفي هذه الحالة تتكرر يوميًا.

### Weekly

يمكن اختيار يوم واحد أو أكثر من أيام الأسبوع.

### Monthly

يتم اختيار يوم من الشهر.

إذا لم يكن اليوم موجودًا في شهر معين، يتم تنفيذ المهمة في **آخر يوم من الشهر**.

### إنشاء الـOccurrences

عند إكمال الـOccurrence الحالية، ينشئ النظام الـOccurrence التالية تلقائيًا.

إذا كانت المهمة مرتبطة بعميل، تظل كل Occurrence جديدة مرتبطة بنفس العميل.

### تعديل Recurring Task

التعديل يؤثر على:

- الـOccurrence الحالية.
- الـOccurrences القادمة.

### حذف Recurring Task

الحذف/الإيقاف يؤثر على الـOccurrences القادمة ولا يحذف الـOccurrences التاريخية المكتملة.

## 10.11 Subtasks

المهام تدعم Subtasks.

يمكن أن تدعم Subtasks متداخلة لأكثر من مستوى عند الحاجة.

لا يمكن جعل المهمة الرئيسية Done قبل إكمال الـSubtasks المطلوبة.

## 10.12 ترتيب المهام

يمكن إعادة ترتيب Tasks باستخدام Drag & Drop.

يتم حفظ الترتيب.

## 10.13 نسخ المهام

يمكن عمل Duplicate/Clone للـTask.

## 10.14 الإجراءات الجماعية

Bulk Actions مدعومة.

مثل:

- Delete.
- تغيير Priority.
- تغيير Status.
- تغيير Due Date.
- أي عمليات جماعية منطقية أخرى.

## 10.15 Rich Notes

تدعم:

- تنسيق النص.
- Bullets.
- Checklists.
- Links.
- Images.
- Files.
- Rich Content آخر مدعوم.

يجب استخدام Auto-Save لمنع فقدان المحتوى.

يمكن إضافة الملفات والصور من خلال Attachments وكذلك Drag & Drop.

## 10.16 Task Updates

Task Updates منفصلة عن Notes.

هي سجلات زمنية مثل:

- بدأ العمل.
- العميل طلب تعديل.
- تم إرسال Creative.
- تم الانتهاء من التعديل.

تدعم:

- Text.
- Images.
- Files.
- Links.

ويمكن:

- تعديلها.
- حذفها.

لا يحتاج النظام لتسجيل اسم من قام بالتعديل لأن المستخدم واحد.

### Task مرتبطة بعميل

عندما تكون Task مرتبطة بClient، يتم إضافة Task Updates تلقائيًا إلى Client Work History.

قاعدة مهمة:

تعديل أو حذف Task Update الأصلية **لا يعدل السجل التاريخي** الذي تم إنشاؤه داخل Work History.

### Task بدون Client

Updates الخاصة بالـTasks غير المرتبطة بعميل تذهب إلى General Activity History.

## 10.17 Task Timer

كل Task تدعم:

- Start.
- Pause.
- Stop.

يمكن تشغيل Timer لمهمة واحدة فقط في نفس الوقت.

عند تشغيل Timer لمهمة جديدة:

- يتوقف الـTimer السابق تلقائيًا.
- يبدأ الـTimer الجديد.

الـTimer يستمر أثناء الانتقال بين الـSections.

يظل الـActive Timer ظاهرًا في الواجهة ويمكن إيقافه من أي Section.

عند تحويل Task إلى Done:

- يتوقف Timer تلقائيًا.
- يتم حفظ Actual Time.

النظام يحتفظ بـ:

- Estimated Time.
- إجمالي Actual Time.

ولا يحتفظ بسجل تفصيلي لكل Session.

يمكن تعديل Actual Time يدويًا.

يظهر Estimated Time وActual Time معًا للمقارنة.

لا يوجد حساب لنسبة الوقت المستهلك من الوقت المتوقع.

لا تظهر بيانات Timer داخل Completed Tasks History.

## 10.18 Task Tags

Task Tags:

- يديرها المستخدم.
- يمكن إعادة استخدامها في أكثر من Task.
- يمكن تغيير اسمها.
- يمكن حذفها.
- لها ألوان قابلة للتخصيص.

حذف Tag لا يحذف الـTasks.

## 10.19 Task Templates

يوجد قسم مستقل لـTask Templates داخل Tasks.

الـTemplate يحفظ كل تفاصيل الـTask.

الـTemplates:

- عامة.
- غير مرتبطة بشكل دائم بعميل معين.

وتدعم:

- Subtasks.
- Tags.
- Recurrence.
- Attachments.
- Priority.
- Notes.
- باقي تفاصيل Task.

العمليات:

- Create.
- Edit.
- Duplicate.
- Delete.

وتدعم:

- Search.
- Filters.
- Categories.

عند إنشاء Task من Template يمكن تعديل البيانات قبل الحفظ.

---

# 11. Task Calendar

يدعم:

- Day View.
- Week View.
- Month View.

## 11.1 إنشاء Task من Calendar

عند الضغط على مساحة فارغة في يوم/وقت:

يفتح Create Task مع تعبئة:

- Due Date.
- Due Time.

تلقائيًا حسب المكان الذي تم الضغط عليه.

## 11.2 Drag & Drop

يمكن سحب Task داخل Calendar لتغيير:

- Due Date.
- Due Time.

## 11.3 Status

يمكن تغيير Status مباشرة من Calendar.

## 11.4 Filters

يدعم:

- Client.
- Priority.
- Status.
- Tags.

Calendar Print/Export غير مطلوب.

## 11.5 Task Dependencies

Task Dependencies غير مطلوبة.

---

# 12. Completed Tasks History

Completed Tasks History منفصلة عن Global Search.

## 12.1 البحث

البحث يكون بواسطة:

- Task Name فقط.

## 12.2 Filters

تشمل:

- Client.
- Priority.
- Completion Date.

## 12.3 البيانات التاريخية

تحتفظ المهمة المكتملة بـ:

- Notes.
- Subtasks.
- Comments/Updates.
- Attachments.
- Tags.
- Due Date.
- باقي تفاصيل المهمة.

## 12.4 إعادة فتح المهمة

يمكن إعادة المهمة إلى:

- To Do.
- In Progress.

---

# 13. وحدة Clients

## 13.1 نموذج العميل

لكل Client نوع عمل أساسي واحد.

Type of Work عبارة عن Free Text.

## 13.2 حالة العميل

الحالات النهائية:

- Upcoming.
- Active.
- Paused.
- Inactive.

الحالة يتم تغييرها يدويًا.

يمكن إعادة Client من Inactive إلى Active بدون فقدان الـHistory.

## 13.3 قائمة العملاء

تعرض:

- Photo.
- Name.
- Start Date.
- Last Activity.
- Status.

وتدعم:

- Search بالاسم.
- Status Filters.
- Bulk Actions.
- Scroll بدل Pagination.

أسماء العملاء ليست بالضرورة Unique.

## 13.4 صورة العميل

الصورة اختيارية.

إذا لم توجد صورة يظهر Placeholder لشخص.

الضغط على الصورة يفتح Client Data/Profile.

## 13.5 Start Date

يتم تعبئته تلقائيًا عند إضافة العميل.

يمكن للمستخدم تعديله.

## 13.6 ترتيب Client Profile

الترتيب المقترح:

1. Tasks
2. Work History
3. Agreement
4. Client Data
5. General Client Notes

## 13.7 Client Data

الحقول الاختيارية:

- Client Photo.
- Client Name.
- Type of Work.
- Brief About Client.
- Brief About Business.
- Contact Data.
- Social Media.
- Website.
- Other Additional Data.

الحقول المستبعدة نهائيًا:

- Ad Account.
- Pixel.
- Business Manager.
- Products.
- Target Audience.
- Offers.

## 13.8 Custom Fields

يدعم النظام:

### Global Custom Fields

حقول تظهر لكل Clients.

### Client-specific Custom Fields

حقول مخصصة لعميل معين.

الأنواع تشمل:

- Text.
- Number.
- Date.
- Link.
- Yes/No.
- أنواع إضافية مستقبلًا حسب الحاجة.

Custom Fields تدخل في Global Search.

عند حذف Custom Field يظهر للمستخدم اختيار بين:

- حذف الـField والقيم المخزنة.
- حذف تعريف الـField مع الاحتفاظ بالقيم التاريخية حيث يسمح التصميم التقني بذلك.

## 13.9 Client Work History

هو سجل أنشطة يحتوي على:

- Date.
- Activity.
- Rich Content.

التاريخ الافتراضي هو اليوم ويمكن تعديله.

يدعم:

- Text.
- Images.
- Files.
- Links.
- Edit.
- Delete.
- Search.
- Date Filters.
- Custom Date Range.

Task Updates المرتبطة بالعميل تظهر تلقائيًا.

كما يمكن إضافة Activities يدويًا.

## 13.10 Client Agreement

Agreement ليس Contract Management Module.

هو مجموعة من Agreement Notes الحرة.

كل Note تحتوي على:

- Content.
- Date.

التاريخ يملأ تلقائيًا ويمكن تعديله.

وتدعم:

- Text.
- Images.
- Files.
- Links.
- Edit.
- Delete.

لا توجد تصنيفات للـAgreement Notes.

ولا توجد Start/End Date رسمية للاتفاق.

## 13.11 General Client Notes

يوجد قسم منفصل عن:

- Agreement.
- Work History.

ويدعم:

- Note واحدة كبيرة.
- أو Notes متعددة.
- Rich Content.
- Images.
- Files.
- Links.
- Edit.
- Delete.

وتدخل ضمن Global Search.

## 13.12 Client Bulk Actions

تدعم:

- Change Status.
- حذف عدة Clients.
- عمليات Bulk منطقية أخرى.

## 13.13 Client Duplicate

Client Clone غير مدعوم.

## 13.14 Client Export

يمكن تصدير Client واحدة بكل:

- Client Data.
- Tasks.
- Work History.
- Agreement Notes.
- Related Files.
- باقي السجلات المرتبطة.

## 13.15 حذف Client

حذف Client ينقل العميل وكل الـrecords المرتبطة به إلى Trash.

ومنها:

- Tasks.
- Work History.
- Agreement.
- Related Files.
- السجلات التابعة الأخرى.

استعادة Client تعيد السجلات المرتبطة بها حيثما كانت متاحة.

---

# 14. وحدة Learning

Learning هي Learning Tracker بسيطة وليست LMS كاملة.

## 14.1 بيانات Course

يدعم:

- Course Name.
- Course URL.
- Start Date.
- Completion Date.
- Notes.
- Category.
- Status.
- Instructor/Creator اختياري.
- Progress %.

لا توجد حقول Platform أو Price.

## 14.2 Course Status

القيم:

- To Learn.
- Done.

عند اختيار Done تنتقل Course من To Learn إلى Done.

## 14.3 Categories

لكل Course Category واحدة.

إدارة Categories:

- Add.
- Rename.
- Delete.
- Move Courses.

حذف Category يتطلب Confirmation ويؤدي إلى حذف Courses الموجودة داخلها.

## 14.4 Course Notes

تدعم:

- Text.
- Images.
- Files.
- Links.

## 14.5 Search & Filters

Courses تدعم Search وFilters.

## 14.6 Duplicate

Course Duplicate/Clone مدعوم.

## 14.7 Bulk Actions

Course Bulk Actions مدعومة.

## 14.8 Course Progress

يوجد Manual Progress %.

إذا كانت المنصة الخارجية توفر API/Integration مسموحًا وعمليًا، يمكن للنظام جلب:

- Progress %.
- Current/Last Lesson.
- Course Structure.
- Completed Lessons.

ولا يجب افتراض إمكانية التكامل مع أي منصة خارجية.

## 14.9 Course Reminders

Course Reminders تعتمد على إعداد عام/افتراضي.

وتظهر داخل النظام.

---

# 15. وحدة Knowledge

Knowledge منفصلة عن Courses.

هدفها تخزين المعرفة الفعلية الناتجة عن:

- Courses.
- Work.
- Research.
- General Experience.

## 15.1 أنواع Knowledge

يمكن أن تكون:

- مرتبطة بـCourse واحدة.
- General Knowledge غير مرتبطة بكورس.

## 15.2 بيانات Knowledge Note

تشمل:

- Title.
- What I Learned.
- Date.
- Course اختياري.
- Category.
- Tags.
- Status.
- Rich Content.

## 15.3 Status

القيم:

- Draft.
- Published.

## 15.4 Categories

المستخدم يدير Categories:

- Add.
- Rename.
- Delete.
- Move Notes.

عند حذف Category:

- Confirmation.
- حذف Category.
- نقل Notes إلى Uncategorized.

## 15.5 Tags

Knowledge Tags:

- اختيارية.
- يديرها المستخدم.
- قابلة لإعادة الاستخدام.
- لها ألوان.
- قابلة للبحث والفلترة.

يمكن استخدام أكثر من Tag في نفس Filter.

## 15.6 خصائص Knowledge

تدعم:

- Search.
- Filters.
- Pin.
- Duplicate/Clone.
- Bulk Actions.
- Edit.
- Delete.

Pinned Notes تظهر أعلى صفحة Knowledge.

لا تظهر Knowledge كـRecent Knowledge Widget في Dashboard.

---

# 16. وحدة Files

Files لها Section مستقلة.

## 16.1 أنواع الملفات

يجب دعم الملفات الشائعة مثل:

- Images.
- PDFs.
- Word.
- Excel.
- أنواع أخرى عند دعمها تقنيًا.

## 16.2 روابط الملفات

يمكن ربط File بـ:

- Client واحد أو أكثر.
- Task واحدة أو أكثر.
- Client + Task معًا.
- أو بدون ارتباط كـGeneral File.

## 16.3 File Tags

تدعم:

- Tags.
- إدارة المستخدم.
- ألوان Tags.

## 16.4 Search & Filters

تشمل:

- File Name.
- File Type.
- Folder.
- Client.
- Task.
- Tags.

## 16.5 عمليات الملفات

تدعم:

- Upload.
- Rename.
- Move.
- Duplicate.
- Delete.
- Download.
- Preview.

لا توجد حاجة إلى Sort مخصص.

ولا توجد حاجة إلى Advanced File Details.

## 16.6 Upload

يدعم Drag & Drop Upload.

يتم الاحتفاظ بالـOriginal Filename تلقائيًا.

يمكن للمستخدم إعادة تسمية الملف اختياريًا.

## 16.7 Folders

Folders اختيارية.

يمكن وضع File بدون Folder.

تدعم Nested Folders.

العمليات:

- Create.
- Rename.
- Delete.
- Move.
- Move into another folder.

حذف Folder غير فارغة يحتاج Confirmation ويحذف محتوياتها.

## 16.8 Preview

الملفات المدعومة يتم Preview لها داخل النظام قدر الإمكان.

يظهر الـPreview في صفحة الملف الأولى/التفاصيل.

الملفات الكبيرة أو غير المدعومة قد تحتاج Download.

## 16.9 حجم الملفات

لا يوجد حد ثابت من ناحية المنتج.

الحد العملي يعتمد على التخزين والبنية التقنية.

---

# 17. Global Search

Global Search من الوظائف الأساسية.

## 17.1 نطاق البحث

يشمل:

- Tasks.
- Clients.
- Client Data.
- Custom Fields.
- Work History.
- Agreement Notes.
- General Client Notes.
- Courses.
- Knowledge.
- Files.
- Activities.
- باقي السجلات القابلة للبحث.

استثناء مهم:

Completed Tasks History لا تدخل في Global Search، ولها Search خاص باسم Task.

## 17.2 لغة البحث

يدعم:

- Arabic.
- English.
- Mixed Content.

## 17.3 محتوى البحث

يبحث في:

- Titles.
- Names.
- Metadata المناسبة.
- Rich Text Content.
- Custom Field Values.

## 17.4 Smart/Fuzzy Search

يجب أن يدعم البحث الصياغات القريبة.

مثال:

البحث عن:

`Facebook Ads`

يمكن أن يعرض نتيجة تحتوي:

`Create Facebook Ad`

عند ملاءمة النتائج.

## 17.5 Filters

يمكن فلترة النتائج حسب الـModule/Source.

مثل:

- Tasks.
- Clients.
- Files.
- Knowledge.
- Courses.

## 17.6 Saved Searches

غير مطلوبة.

---

# 18. Notifications Center

Notifications Center قسم مستقل.

## 18.1 الخصائص

يدعم:

- Read.
- Unread.
- Mark All as Read.
- Historical Notifications.

## 18.2 الاحتفاظ

يتم حذف الإشعارات تلقائيًا بعد:

**30 يومًا**

## 18.3 مصادر الإشعارات

يمكن أن تأتي من:

- Tasks.
- Recurring Tasks.
- Courses.
- Clients.
- Files.
- Backup Events.
- Storage Warnings.
- أنشطة النظام المهمة الأخرى.

## 18.4 طريقة التوصيل

الإشعارات العامة تدعم:

- In-System Notifications.
- Mobile Push Notifications.

Course Reminders مطلوبة داخل النظام.

## 18.5 إعدادات الإشعارات

يمكن إيقاف Notifications بالكامل من Settings.

---

# 19. Trash / Recycle Bin

Trash منطقة موحدة على مستوى النظام.

## 19.1 العناصر

يمكن أن تحتوي على:

- Tasks.
- Clients.
- Files.
- Courses.
- Knowledge.
- Folders.
- باقي العناصر القابلة للحذف.

يظهر نوع العنصر مع كل عنصر.

## 19.2 مدة الاحتفاظ

العناصر تبقى في Trash لمدة:

**30 يومًا**

ثم تحذف نهائيًا تلقائيًا.

## 19.3 Restore

يمكن استعادة العناصر قبل الحذف النهائي.

استعادة Client تعيد السجلات المرتبطة بها حيثما أمكن.

## 19.4 Permanent Delete

يمكن الحذف النهائي يدويًا قبل مرور 30 يومًا.

ويتطلب Confirmation إضافي.

## 19.5 Undo

بعد الحذف يظهر Undo لمدة:

**4 ثوانٍ**

---

# 20. Activity History

Activity History يسجل العمليات المهمة في النظام.

## 20.1 أمثلة

مثل:

- Create.
- Edit.
- Delete.
- Restore.
- عمليات النظام المهمة الأخرى.

## 20.2 مدة الاحتفاظ

تحذف تلقائيًا بعد:

**90 يومًا**

## 20.3 الإدارة

يمكن للمستخدم:

- Search.
- Filters.
- Clear Activity History يدويًا.

## 20.4 علاقتها بالـDashboard

General Activity History لا تظهر في Dashboard Recent Activity.

الـRecent Activity في Dashboard مخصصة للعملاء.

---

# 21. Settings

تشمل:

- Theme.
- Default Reminder Time.
- Notifications On/Off.
- Backup.
- Export.
- Restore.
- إعدادات Trash عند الحاجة.
- Categories Management.
- Tags Management.
- Custom Fields.
- Dashboard Reset.
- Reset All Settings.

## 21.1 Reset All Settings

يعيد الإعدادات للوضع الافتراضي.

ولا يحذف بيانات المستخدم.

---

# 22. Backup / Export / Restore

## 22.1 Automatic Backup

- يومي.
- يشمل النظام بالكامل.
- Cloud Backup إذا كان ممكنًا تقنيًا.

## 22.2 Backup Retention

المستخدم اختار الاحتفاظ بآخر Backup مع سياسة احتفاظ 30 يومًا.

يجب مواءمة ذلك مع نظام Versioning/Storage المستخدم.

## 22.3 Manual Export

يدعم:

- Selected Modules.
- Data.
- Files.
- Combined Export.

يدعم ZIP للـCombined Export.

## 22.4 Restore

Restore هو:

- Full System Restore.
- يستبدل البيانات الحالية بالكامل.

قبل Restore:

- يعمل النظام Backup تلقائي للبيانات الحالية.

---

# 23. حماية البيانات واسترجاعها

يجب توفير:

- Auto-Save.
- Confirmation قبل الحذف.
- Confirmation إضافي للحذف النهائي.
- Undo.
- Trash.
- Restore.
- Backup قبل Restore.
- Automatic Backup.
- Storage Warning.

إذا فشل Automatic Backup:

- يظهر Notification.

إذا اقترب التخزين من الامتلاء:

- يظهر Warning داخل النظام.

---

# 24. Offline & Synchronization

يجب أن يدعم:

- العمل بدون إنترنت.
- حفظ التغييرات أثناء Offline.
- المزامنة تلقائيًا عند عودة الإنترنت.
- المزامنة بين Mobile وDesktop.

يجب تحديد آلية Conflict Resolution أثناء التصميم التقني إذا حدث تعديل لنفس البيانات من أكثر من جهاز أثناء Offline.

---

# 25. المتطلبات غير الوظيفية

## 25.1 Responsiveness

يجب أن يكون النظام مناسبًا لـ:

- Mobile.
- Desktop.

## 25.2 Usability

يجب أن:

- يقلل التنقل غير الضروري.
- يجعل الإجراءات الأساسية واضحة.
- يوفر Quick Add.
- يجعل المهام الأساسية واضحة.
- يحافظ على سياق المستخدم.
- يوفر Confirmation للعمليات الخطيرة.

## 25.3 Performance

يجب أن يظل النظام Responsive مع زيادة:

- Tasks.
- Clients.
- Courses.
- Knowledge Notes.
- Files.
- Activities.

يتم تحديد أرقام الأداء الدقيقة أثناء التصميم التقني.

## 25.4 Reliability

تقليل فقدان البيانات من خلال:

- Auto-Save.
- Automatic Backup.
- Restore.
- Trash.
- Undo.

## 25.5 Accessibility

يجب توفير:

- Typography واضحة.
- Status Indicators واضحة.
- Contrast مناسب.
- Keyboard Accessibility حيثما كان عمليًا.
- Mobile-friendly controls.

---

# 26. Business Rules

1. النظام Single-User.
2. Priority إجباري لكل Task.
3. Client اختياري في Task.
4. Task بدون Due Date لا تحصل على Reminder مرتبط بالموعد.
5. لا يمكن جعل Task Done قبل إكمال Subtasks المطلوبة.
6. Task المكتملة تخرج من Active Tasks وتبقى في History.
7. يمكن إعادة فتح Task مكتملة.
8. Recurring Tasks تنشئ Occurrences مستقبلية تلقائيًا.
9. تاريخ الـRecurring Tasks محفوظ.
10. Weekly Recurrence تدعم أكثر من يوم.
11. Monthly Recurrence تستخدم آخر يوم في الشهر إذا لم يوجد اليوم المختار.
12. Daily Recurrence يمكن أن تكون كل يوم أو أيام محددة.
13. Occurrence الجديدة ترث Client المرتبط.
14. Timer واحد فقط يمكن تشغيله في نفس الوقت.
15. تشغيل Timer جديد يوقف السابق.
16. Timer يستمر أثناء التنقل بين الصفحات.
17. إكمال Task يوقف Timer.
18. Actual Time قابل للتعديل.
19. Client Status يدوي.
20. Inactive Client يمكن إعادته إلى Active.
21. Client Names ليست Unique بالضرورة.
22. حذف Client ينقل السجلات التابعة إلى Trash.
23. Restore للـClient يعيد السجلات التابعة حيثما أمكن.
24. Client Clone غير مدعوم.
25. حذف Course Category يحذف Courses الموجودة داخلها بعد Confirmation.
26. حذف Knowledge Category ينقل Notes إلى Uncategorized.
27. Tags قابلة لإعادة الاستخدام.
28. حذف Tag لا يحذف السجلات المرتبطة.
29. Completed Tasks History خارج Global Search.
30. Notifications تحتفظ بالبيانات 30 يومًا.
31. Trash تحتفظ بالعناصر 30 يومًا.
32. Activity History تحتفظ بالسجلات 90 يومًا.
33. Undo للحذف متاح 4 ثوانٍ.
34. Permanent Delete يحتاج Confirmation.
35. Restore عملية Full System.
36. يتم Backup للبيانات الحالية قبل Restore.
37. لغة الواجهة English.
38. المحتوى يدعم العربية والإنجليزية.
39. توقيت مصر ثابت.
40. Dashboard قابلة للتخصيص والحفظ.
41. Quick Add متاحة.
42. Keyboard Shortcuts غير مطلوبة.
43. Saved Searches غير مطلوبة.
44. Task Dependencies غير مطلوبة.
45. Calendar Print/Export غير مطلوب.
46. Client Clone غير مدعوم.

---

# 27. نطاق المشروع

## 27.1 داخل النطاق

- Dashboard.
- Tasks.
- Task Calendar.
- Task Templates.
- Recurring Tasks.
- Task Timer.
- Clients.
- Client Work History.
- Client Agreements.
- Client Notes.
- Custom Fields.
- Learning.
- Knowledge.
- Files.
- Global Search.
- Notifications.
- Activity History.
- Trash.
- Settings.
- Backup.
- Export.
- Restore.
- Offline Mode.
- Synchronization.
- PWA.
- Light/Dark Mode.

## 27.2 خارج النطاق أو غير مطلوب

- Multi-user Collaboration.
- Email/Password Authentication في MVP.
- Client Clone.
- Task Dependencies.
- Saved Searches.
- Calendar Print/Export.
- Keyboard Shortcuts.
- Course Platform Field.
- Course Price Field.
- Formal Contract Management.
- Ad Account / Pixel / Business Manager.
- Products / Target Audience / Offers في Client Data.
- Detailed Task Session History.
- Time-efficiency Percentage.

---

# 28. أهم User Journeys

## 28.1 الاستخدام اليومي

1. المستخدم يفتح Dashboard.
2. يراجع الملخص.
3. يراجع Urgent / Today / Overdue Tasks.
4. ينشئ أو يفتح Tasks.
5. ينفذ المهام.
6. يتابع العملاء.
7. يحدث Client Work History.
8. يدرس Courses.
9. يسجل Knowledge.
10. يخزن أو يصل إلى Files.
11. يراجع Notifications.

## 28.2 إنشاء Task

1. الضغط على Quick Add → Task.
2. إدخال Task Name.
3. اختيار Priority إجباري.
4. اختيار Client اختياري.
5. إضافة Due Date/Time اختياريًا.
6. إضافة Notes/Tags/Subtasks/Attachments/Estimated Time/Recurrence عند الحاجة.
7. Save.
8. تظهر Task في Active Tasks وDashboard وCalendar حسب البيانات.

## 28.3 إكمال Task

1. إكمال كل Subtasks المطلوبة.
2. تغيير Status إلى Done.
3. إيقاف Timer تلقائيًا إذا كان يعمل.
4. نقل Task من Active Tasks.
5. حفظها في Completed Tasks History.

## 28.4 Client Workflow

1. إنشاء Client.
2. Start Date يملأ تلقائيًا.
3. إضافة Client Data اختياريًا.
4. إضافة Tasks.
5. تسجيل Work History.
6. تسجيل Agreement Notes.
7. تسجيل General Client Notes.
8. ربط Files.
9. تغيير Status يدويًا عند الحاجة.

## 28.5 Learning Workflow

1. إنشاء Course.
2. اختيار Category.
3. تحديد To Learn.
4. متابعة Progress % يدويًا.
5. إضافة Course Notes.
6. إكمال Course.
7. تحويل Status إلى Done.
8. إنشاء Knowledge Notes مرتبطة بالكورس.

---

# 29. توصية تنفيذ الـMVP

يجب أن يتبع التنفيذ ترتيب الأولويات الذي حدده المستخدم.

## المرحلة الأولى — Core Execution

- Tasks.
- Task List.
- Task Status.
- Priority.
- Due Dates.
- Subtasks.
- Tags.
- Notes.
- Attachments.
- Task Updates.
- Recurring Tasks.
- Task Templates.
- Task Timer.
- Completed Tasks History.

## المرحلة الثانية — Command Center

- Dashboard.
- Quick Add.
- Dashboard Customization.
- Calendar.
- Notifications.
- Global Search.

## المرحلة الثالثة — Learning & Knowledge

- Courses.
- Categories.
- Progress.
- Knowledge.
- Knowledge Categories.
- Tags.
- Search.

## المرحلة الرابعة — Clients

- Client List.
- Client Profile.
- Work History.
- Agreement.
- General Notes.
- Custom Fields.
- Client Tasks.
- Client Files.
- Client Export.

## المرحلة الخامسة — Files & Infrastructure

- Files.
- Folders.
- File Relationships.
- Preview.
- Trash.
- Activity History.
- Backup.
- Export.
- Restore.
- Offline Sync.
- PWA.

هذا ترتيب تنفيذ مقترح، وليس تغييرًا لأولويات المستخدم الأصلية.

---

# 30. Dependencies

تحتاج هذه الأجزاء إلى قرارات تقنية أثناء Solution Design:

1. Cloud Storage Provider.
2. Offline Database Technology.
3. Synchronization Architecture.
4. Conflict Resolution.
5. Push Notification Infrastructure.
6. PWA Support.
7. File Preview Libraries/Services.
8. External Course Integrations.
9. Backup Storage/Versioning.
10. Search Engine / Fuzzy Search.
11. Rich Text Editor.
12. File Storage Architecture.
13. Authentication/Security Architecture في حالة Cloud Sync.

---

# 31. المخاطر

## 31.1 Offline Sync Conflicts

قد يعدل أكثر من جهاز نفس السجل أثناء Offline.

يجب تحديد Conflict Resolution Policy.

## 31.2 تكلفة تخزين الملفات

الصور والملفات الكبيرة يمكن أن ترفع تكلفة التخزين.

## 31.3 التكامل مع منصات الكورسات

يعتمد جلب Progress على API والصلاحيات ودعم المنصة.

## 31.4 Cloud Backup

يتطلب Cloud Backup بنية موثوقة وآمنة.

## 31.5 تعقيد البحث

البحث التقريبي بالعربية والإنجليزية داخل Rich Content وCustom Fields وMetadata قد يحتاج Search Strategy متخصصة.

## 31.6 Rich Content

دعم الصور والملفات داخل Notes وUpdates يزيد من تعقيد التنفيذ والتخزين.

---

# 32. نقاط تحتاج حسم تقني في الـSRS

رغم اكتمال Business Discovery، هناك نقاط يجب حسمها أثناء Solution Design:

1. Cloud Backup Provider.
2. Cloud File Storage Provider.
3. Security/Auth Model.
4. Offline Sync Conflict Resolution.
5. Backup Versioning.
6. Notification Scheduling Architecture.
7. أنواع الملفات المدعومة للـPreview.
8. الحد العملي للتخزين.
9. طريقة Mobile Push.
10. صيغة Export للبيانات المنظمة.
11. خوارزمية Fuzzy Search.
12. Course Integrations التي ستدعم في البداية.
13. هل External Integrations جزء من MVP أم Post-MVP.
14. الأحداث التي يسجلها Activity History بالتحديد.
15. سلوك Restore عندما يكون Record تابع غير قابل للاستعادة.
16. سلوك تعديل Recurring Tasks بعد إنشاء Occurrences سابقة وحالية وقادمة.
17. Default Reminder Time.
18. Storage Warning Threshold.
19. سلوك Sync عند تعديل نفس Record من أكثر من جهاز Offline.

---

# 33. النتائج التجارية المطلوبة

يُعتبر النظام ناجحًا من ناحية Business عندما يستطيع المستخدم:

- فتح Dashboard وفهم شغله اليومي فورًا.
- إنشاء وإدارة Tasks بسرعة.
- معرفة Urgent وOverdue Tasks.
- إدارة المهام المتكررة بدون إعادة إنشائها يدويًا.
- استخدام Templates للمهام المتكررة.
- معرفة الوقت الفعلي الذي قضاه على Tasks.
- إدارة العملاء ورؤية تاريخ التعامل معهم.
- متابعة Courses وProgress.
- تسجيل Knowledge قابلة لإعادة الاستخدام.
- العثور على المعلومات بسرعة من Global Search.
- تخزين واسترجاع الملفات المهمة.
- استعادة البيانات المحذوفة.
- استقبال التذكيرات المهمة.
- استخدام النظام من Mobile وDesktop.
- العمل Offline والمزامنة بعد عودة الإنترنت.
- عمل Backup وRestore للنظام بالكامل.

---

# 34. ملخص التتبع (Traceability)

| احتياج العمل | الوحدة الأساسية |
|---|---|
| معرفة ما يجب عمله | Dashboard + Tasks |
| إدارة العمل اليومي | Tasks |
| إدارة الأعمال المتكررة | Recurring Tasks + Templates |
| معرفة الوقت المستغرق | Task Timer |
| إدارة العملاء | Clients |
| متابعة التعلم | Learning |
| تسجيل المعرفة | Knowledge |
| تخزين الملفات | Files |
| العثور على المعلومات | Global Search |
| عدم تفويت التذكيرات | Notifications |
| استعادة المحذوفات | Trash |
| معرفة تاريخ العمليات | Activity History |
| حماية البيانات | Backup / Restore |
| العمل من أي مكان | Responsive UI + PWA + Offline Sync |

---

# 35. الخلاصة النهائية للـBA

أوضحت جلسة Discovery أن المنتج المقترح ليس مجرد Task Manager، ولكنه أقرب إلى:

> **نظام تشغيل شخصي للعمل والعملاء والمهام والتعلم والمعرفة والملفات.**

لذلك يجب أن تظل التجربة الأساسية:

> **Open → Understand → Execute → Record → Learn → Organize → Recover**

الـTasks هي قلب النظام التشغيلي.

الـDashboard هي مركز القيادة.

الـClients تضيف سياق العمل التجاري.

Learning وKnowledge يدعمان التطور المستمر.

Files توفر مكانًا مركزيًا للأصول المهمة.

Search وNotifications وActivity History وTrash وBackup وRestore هي البنية الداعمة التي تجعل النظام عمليًا وموثوقًا للاستخدام اليومي.

هذه الوثيقة تمثل الأساس للمرحلة التالية:

**Software Requirements Specification (SRS)**

يجب أن يحول الـSRS هذه المتطلبات إلى Functional Requirements تفصيلية، System Behavior، Data Model، Use Cases، Acceptance Criteria، Validation Rules، Technical Assumptions، ومواصفات جاهزة للتنفيذ.
