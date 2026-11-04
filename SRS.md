# Software Requirements Specification (SRS)
## Personal Productivity & Knowledge Operating System

**الإصدار:** 1.0  
**الحالة:** Ready for Solution Design & Implementation  
**تاريخ الإصدار:** 27 سبتمبر 2026  
**المصدر:** BRD v1.0  
**نوع النظام:** Single-User Web/PWA Application  
**لغة الواجهة:** English  
**لغة المحتوى:** Arabic / English / Mixed  
**Timezone:** Egypt  
**الهدف:** تحويل الـBRD إلى مواصفات Software قابلة للتنفيذ والاختبار، مع تقسيم التنفيذ إلى MVPs متتابعة، وكل MVP يمثل Product Slice مكتمل وقابل للاستخدام.

---

# 1. Purpose

هذا المستند هو الـSRS التنفيذي للنظام، ويحوّل متطلبات الـBRD إلى:

- Functional Requirements
- System Behaviors
- Business Rules
- User Flows
- Data Model
- Validation Rules
- Acceptance Criteria
- Non-Functional Requirements
- Technical Assumptions
- Error Handling
- Security Requirements
- Testing Strategy
- MVP Delivery Plan
- Traceability Matrix
- Open Technical Decisions

الهدف ليس تحديد Technology Stack بشكل نهائي، وإنما تحديد **ما يجب أن يفعله النظام وكيف يجب أن يتصرف** بحيث يستطيع فريق الـProduct / UX / Frontend / Backend / QA البدء في التنفيذ.

---

# 2. Product Definition

النظام هو Personal Operating System لإدارة:

- Tasks
- Daily Execution
- Clients
- Learning
- Knowledge
- Files
- Notifications
- Activity History
- Recovery
- Backup / Restore

المبدأ الأساسي للتجربة:

> Open → Understand → Execute → Record → Learn → Organize → Recover

الـTasks هي مركز التنفيذ.

الـDashboard هي مركز القيادة.

الـClients تضيف سياق العمل.

Learning وKnowledge يدعمان التعلم المستمر.

Files تحفظ الأصول.

Search / Notifications / Activity / Trash / Backup / Restore هي طبقة الاعتمادية والاسترجاع.

---

# 3. Scope

## 3.1 In Scope

- Dashboard
- Tasks
- Task List
- Calendar
- Task Templates
- Recurring Tasks
- Subtasks
- Task Timer
- Task Updates
- Task Attachments
- Completed Tasks History
- Clients
- Client Profile
- Client Work History
- Client Agreement Notes
- Client General Notes
- Client Custom Fields
- Learning
- Courses
- Course Categories
- Course Progress
- Knowledge
- Knowledge Categories
- Knowledge Tags
- Files
- Folders
- File Relationships
- Global Search
- Notifications
- Activity History
- Trash
- Backup
- Export
- Restore
- Offline Mode
- Synchronization
- PWA
- Light / Dark Mode

## 3.2 Out of Scope

- Multi-user collaboration
- Email/Password Authentication in MVP
- Client Clone
- Task Dependencies
- Saved Searches
- Calendar Print/Export
- Keyboard Shortcuts
- Course Platform field
- Course Price field
- Formal Contract Management
- Ad Account / Pixel / Business Manager
- Products / Target Audience / Offers in Client Data
- Detailed Task Session History
- Time-efficiency percentage

---

# 4. Actors

## 4.1 Primary Actor

**User**

System is Single-User.

## 4.2 Future Actors

هذه ليست ضمن MVP:

- External Course Platform
- Cloud Storage Provider
- Push Notification Provider
- Backup Provider

---

# 5. Product Principles

1. كل MVP يجب أن يكون قابلًا للتشغيل independently.
2. لا يتم بناء UI بدون Behavior واضح.
3. كل Feature لها Acceptance Criteria.
4. أي Requirement غير محسوم تقنيًا يتم وضعه كـTBD.
5. البيانات لا تُفقد نتيجة Edit أو Delete عادي.
6. العمليات الخطرة تحتاج Confirmation.
7. الـMVP لا يعتمد على Features مستقبلية لكي يكون usable.
8. كل Phase يجب أن تضيف قيمة استخدام فعلية.
9. كل Phase يجب أن تحتوي على Regression Tests لما سبق.
10. الـData Model يجب أن يسمح بالتوسع بدون إعادة بناء النظام.

---

# 6. MVP Strategy

بدل تقسيم المشروع إلى Layers تقنية، يتم التنفيذ كـVertical Product Slices.

## MVP-1 — Task Execution

**القيمة:** المستخدم يستطيع إدارة وتنفيذ عمله اليومي بالكامل.

### Included

- Task CRUD
- Priority
- Status
- Due Date / Time
- Notes
- Tags
- Subtasks
- Attachments
- Task Updates
- Recurring Tasks
- Task Templates
- Timer
- Completed Tasks History

### User Outcome

المستخدم يستطيع فتح النظام، إنشاء مهامه، تنفيذها، تسجيل التحديثات، تشغيل الوقت، وإغلاق المهمة بدون الاعتماد على أي Module آخر.

---

## MVP-2 — Personal Command Center

**القيمة:** المستخدم يستطيع معرفة ماذا يجب أن يفعل الآن ومتى.

### Included

كل MVP-1 +

- Dashboard
- Quick Add
- Calendar
- Notifications Center
- Reminder Engine
- Dashboard Customization
- Global Search للـModules المتاحة

### User Outcome

المستخدم يحصل على Command Center حقيقي لإدارة يومه.

---

## MVP-3 — Learning & Knowledge

**القيمة:** المستخدم يستطيع تحويل التعلم إلى Knowledge قابلة لإعادة الاستخدام.

### Included

كل MVP-2 +

- Courses
- Course Categories
- Progress
- Course Notes
- Course Reminders
- Knowledge
- Knowledge Categories
- Knowledge Tags
- Knowledge Search / Filters
- Course → Knowledge relationship

### User Outcome

المستخدم يستطيع تسجيل ما يتعلمه وتحويله إلى Knowledge منظمة.

---

## MVP-4 — Client Workspace

**القيمة:** المستخدم يستطيع إدارة العمل مع العملاء داخل نفس النظام.

### Included

كل MVP-3 +

- Client List
- Client Profile
- Client Data
- Client Status
- Client Work History
- Client Agreement Notes
- Client General Notes
- Custom Fields
- Client Tasks
- Client Files relationships
- Client Export

### User Outcome

المستخدم يستطيع إدارة دورة العمل مع العميل من مكان واحد.

---

## MVP-5 — Files & Recovery

**القيمة:** النظام يصبح مساحة عمل موثوقة للبيانات والملفات.

### Included

كل MVP-4 +

- Files
- Folders
- File Preview
- File Relationships
- Trash
- Restore
- Activity History
- Backup
- Export
- Full Restore
- Storage Warnings

### User Outcome

المستخدم يستطيع حفظ واسترجاع بياناته وملفاته بدون خوف من فقدان البيانات.

---

## MVP-6 — Offline & Production Hardening

**القيمة:** النظام usable reliably على Mobile/Desktop حتى مع ضعف أو انقطاع الإنترنت.

### Included

كل MVP-5 +

- PWA
- Offline Data Layer
- Offline CRUD
- Sync Queue
- Conflict Resolution
- Desktop/Mobile Synchronization
- Push Notifications
- Performance Hardening
- Reliability / Recovery Testing
- Security Hardening

### User Outcome

النظام يصبح Production-Ready كـPersonal Operating System.

---

# 7. Release Gates

كل MVP لا يعتبر مكتملًا إلا إذا حقق:

### Product Gate

- كل Features المدرجة تعمل.
- الـCore User Journey مكتمل.
- لا يوجد Blocker.
- البيانات تحفظ وتسترجع بشكل صحيح.

### UX Gate

- Responsive.
- Mobile usable.
- Empty states.
- Loading states.
- Error states.
- Confirmation للعمليات الخطرة.

### QA Gate

- Unit Tests.
- Integration Tests.
- Critical E2E tests.
- Regression tests للمراحل السابقة.

### Data Gate

- Create / Read / Update / Delete يعمل.
- Relationships سليمة.
- لا توجد بيانات orphaned بسبب العمليات الأساسية.
- Backup/Recovery requirements الخاصة بالمرحلة تعمل إذا كانت ضمن المرحلة.

### Performance Gate

الأرقام النهائية يتم اعتمادها أثناء Solution Design، لكن النظام يجب أن يظل responsive مع زيادة البيانات.

---

# 8. Global UX Requirements

## 8.1 Layout

Desktop:

- Sidebar
- Main Content
- Optional contextual panels

Mobile:

- Responsive navigation
- Touch-friendly controls
- No horizontal overflow
- Bottom navigation أو mobile sidebar حسب UX Design

## 8.2 Theme

يدعم:

- Light
- Dark
- Manual Theme Selection

## 8.3 Language

UI:

- English only

User-generated content:

- Arabic
- English
- Mixed
- Unicode

## 8.4 Timezone

جميع التواريخ والأوقات يتم التعامل معها وفق:

`Africa/Cairo`

يجب حفظ timestamps بطريقة تسمح بالتعامل الآمن مع timezone في طبقة البيانات.

## 8.5 Global UI States

كل Screen يجب أن تدعم:

- Loading
- Empty
- Success
- Error
- Offline
- Permission / Security error عند الحاجة
- Confirmation
- Destructive action warning

---

# 9. Global Data Rules

1. كل Entity لها unique internal ID.
2. لا يعتمد النظام على اسم العنصر كـUnique Identifier.
3. كل Record يحتوي على createdAt.
4. كل Record قابل للتعديل يحتوي على updatedAt.
5. التاريخ الافتراضي للعمليات الزمنية هو current date في Egypt timezone.
6. User content يدعم Unicode.
7. حذف البيانات العادي Soft Delete حيثما ينطبق.
8. العناصر القابلة للاسترجاع تنتقل إلى Trash.
9. Permanent Delete غير قابل للاسترجاع.
10. أي علاقة بين Records يجب أن تحافظ على Referential Integrity.
11. حذف Parent يجب أن يحدد behavior واضح للـChildren.
12. لا يتم حذف البيانات التاريخية تلقائيًا إلا وفق retention rules.

---

# 10. Core Entity Model

## 10.1 Task

```text
Task
- id
- title
- clientId?
- priority
- status
- dueDate?
- dueTime?
- notes?
- estimatedTime?
- actualTime
- sortOrder
- recurrenceId?
- parentTaskId?
- createdAt
- updatedAt
- completedAt?
- deletedAt?
```

### Priority

- Urgent
- High
- Medium
- Low

Priority is required.

### Status

- To Do
- In Progress
- Done

---

# 11. Task Requirements

## FR-TASK-001 Create Task

The system SHALL allow the user to create a Task.

### Required

- Task Name
- Priority

### Optional

- Client
- Due Date
- Due Time
- Notes
- Tags
- Subtasks
- Attachments
- Estimated Time
- Recurrence

### Acceptance Criteria

- Save without Client.
- Save without Due Date.
- Reject save without Priority.
- New task appears in Active Tasks.
- New task appears in relevant Dashboard/Calendar views.

---

## FR-TASK-002 Edit Task

User SHALL be able to edit all editable Task fields.

Changes SHALL be persisted.

---

## FR-TASK-003 Delete Task

System SHALL require confirmation.

After confirmation:

1. Task is soft-deleted.
2. Task appears in Trash.
3. Undo is available for 4 seconds.
4. Related historical records behavior follows Task deletion policy.

---

## FR-TASK-004 Task Status

User SHALL change status from:

- To Do
- In Progress
- Done

Status change is possible from List and Calendar.

---

## FR-TASK-005 Complete Task

A Task SHALL NOT become Done if required Subtasks are incomplete.

When Done:

- Active Task list no longer shows it.
- Completed History contains it.
- Timer stops automatically.
- Actual Time is saved.
- completedAt is populated.

---

## FR-TASK-006 Reopen Task

Completed Task SHALL be reopenable as:

- To Do
- In Progress

Original Task details remain intact.

---

# 12. Subtasks

## FR-SUB-001

Task SHALL support nested Subtasks.

## FR-SUB-002

System SHALL support more than one nesting level where technically supported.

## FR-SUB-003

Parent Task cannot be marked Done while required Subtasks are incomplete.

## FR-SUB-004

Completing all required Subtasks does not automatically mark parent Done unless explicitly designed in UX.

---

# 13. Task Ordering

User SHALL be able to Drag & Drop Tasks.

The system SHALL persist sort order.

Order should remain stable after refresh.

---

# 14. Task Tags

Tags:

- Are reusable.
- Have customizable colors.
- Can be renamed.
- Can be deleted.
- Can be assigned to multiple Tasks.

Deleting a Tag MUST NOT delete Tasks.

---

# 15. Task Notes

Task Notes SHALL support:

- Rich text
- Bullets
- Checklists
- Links
- Images
- Files

Auto-save is required.

System SHALL reduce risk of losing unsaved content.

---

# 16. Task Updates

Task Updates are separate from Notes.

Each Update supports:

- Text
- Images
- Files
- Links
- Edit
- Delete
- Timestamp

Example:

```text
10:30 — Client requested a new Creative.
13:00 — Creative sent.
16:00 — Client approved.
```

### Client Rule

If Task has Client:

Task Updates are copied as historical entries into Client Work History.

Later edit/delete of the Task Update SHALL NOT modify the historical Work History entry.

### No Client Rule

If Task has no Client:

Task Update is recorded in General Activity History.

---

# 17. Task Timer

Each Task supports:

- Start
- Pause
- Stop

Only one active Timer may exist system-wide.

Starting a Timer for another Task:

1. Stops current Timer.
2. Saves current elapsed time.
3. Starts new Timer.

Timer survives navigation between Sections.

Active Timer is globally visible.

Completing Task stops Timer.

System stores:

- estimatedTime
- actualTime

Detailed session history is out of scope.

Actual Time can be manually edited.

---

# 18. Recurring Tasks

Supported frequencies:

- Daily
- Weekly
- Monthly

Supported configuration:

- Start Date
- End Date
- Stop Recurrence

If no End Date exists, recurrence continues until stopped.

## Daily

- Every day
- Selected days

## Weekly

- One or more weekdays

## Monthly

- Selected day of month

If selected day does not exist:

- execute on last day of that month.

## Occurrence

Completing current occurrence generates next occurrence.

New occurrence inherits Client relationship.

## Editing

Editing recurring task SHALL define whether change applies to:

- Current occurrence
- Future occurrences

The BRD requires current + future behavior; exact data model remains a technical design decision.

## Delete

Stopping/deleting recurrence affects future occurrences.

Completed historical occurrences remain.

---

# 19. Task Templates

Template stores:

- Priority
- Notes
- Tags
- Subtasks
- Attachments
- Recurrence
- Other supported Task properties

Templates are generic and not permanently tied to a Client.

Operations:

- Create
- Edit
- Duplicate
- Delete
- Search
- Filter
- Category

Creating a Task from Template SHALL allow editing before Save.

---

# 20. Calendar

Views:

- Day
- Week
- Month

## Create From Calendar

Clicking empty time slot opens Create Task with:

- Due Date
- Due Time

pre-populated.

## Drag & Drop

Dragging Task changes:

- Due Date
- Due Time

## Filters

- Client
- Priority
- Status
- Tags

Calendar print/export is not required.

Task Dependencies are not required.

---

# 21. Completed Tasks History

Completed Tasks History is separate from Global Search.

Search:

- Task Name

Filters:

- Client
- Priority
- Completion Date

Stored content:

- Notes
- Subtasks
- Updates
- Attachments
- Tags
- Due Date
- Other Task details

Completed Tasks can be reopened.

---

# 22. Dashboard

Dashboard is the primary entry point.

Primary question:

> What do I need to do now?

Widgets:

- Task Summary
- Full Active Task List
- Urgent
- Today
- Overdue
- Upcoming
- Learning
- Client
- Client Recent Activity
- Quick Add
- Active Timer

## Dashboard Task Summary

Must show:

- Today
- Overdue
- Urgent
- Upcoming

## Full Task List

All active tasks are accessible.

Scrolling is acceptable.

## Urgent

Urgent tasks remain visually prominent regardless of Due Date.

## Customization

User can:

- Show/hide widgets.
- Drag/reorder widgets.
- Auto-save layout.
- Reset dashboard.

## Learning Widget

User can choose supported displayed data, such as:

- Courses To Learn
- Completed Courses
- Other relevant Learning metrics

## Client Widget

Client Widget is fixed.

## Recent Activity

Dashboard Recent Activity means Client Recent Activity only.

General Activity History does not appear there.

---

# 23. Quick Add

Dashboard SHALL provide:

- + Task
- + Client
- + Course
- + Knowledge
- + Activity

Keyboard shortcuts are not required.

---

# 24. Learning

Learning is a tracker, not a full LMS.

## Course Entity

```text
Course
- id
- name
- url?
- startDate?
- completionDate?
- notes?
- categoryId
- status
- instructor?
- progressPercent
- createdAt
- updatedAt
```

No:

- Platform
- Price

unless added in a future requirement.

## Course Status

- To Learn
- Done

## Categories

Operations:

- Add
- Rename
- Delete
- Move Courses

Deleting a Course Category requires Confirmation.

Current BRD behavior says Courses inside deleted category are deleted. This is a destructive rule and must show an explicit warning.

## Course Notes

Support:

- Text
- Images
- Files
- Links

## Search / Filters

Courses support search and filters.

## Duplicate

Course duplication is supported.

## Bulk Actions

Supported.

## Progress

Manual Progress %.

External integration MAY provide:

- Progress %
- Current/Last Lesson
- Course Structure
- Completed Lessons

Only if API is available and integration is explicitly supported.

---

# 25. Knowledge

Knowledge is independent from Courses.

Knowledge sources:

- Courses
- Work
- Research
- General Experience

## Knowledge Entity

```text
KnowledgeNote
- id
- title
- whatILearned
- date
- courseId?
- categoryId
- status
- richContent
- tags[]
- pinned
- createdAt
- updatedAt
```

## Status

- Draft
- Published

## Categories

- Add
- Rename
- Delete
- Move Notes

Deleting category:

- Confirmation
- Category removed
- Notes moved to Uncategorized

## Tags

- Optional
- Reusable
- Colored
- Searchable
- Filterable
- Multiple tags per filter

## Features

- Search
- Filters
- Pin
- Duplicate
- Bulk Actions
- Edit
- Delete

Pinned notes appear first.

---

# 26. Clients

## Client Entity

```text
Client
- id
- photo?
- name
- startDate
- typeOfWork
- briefAboutClient?
- briefAboutBusiness?
- contactData?
- socialMedia?
- website?
- status
- customFields
- generalNotes
- createdAt
- updatedAt
- deletedAt?
```

Client names do not need to be unique.

## Status

- Upcoming
- Active
- Paused
- Inactive

Status is manually changed.

Inactive Client can return to Active.

## Client List

Display:

- Photo
- Name
- Start Date
- Last Activity
- Status

Features:

- Search by name
- Status filters
- Bulk actions
- Scroll

Photo is optional.

Without photo:

- Person placeholder

---

# 27. Client Profile

Recommended order:

1. Tasks
2. Work History
3. Agreement
4. Client Data
5. General Client Notes

## Client Data

Optional fields:

- Photo
- Name
- Type of Work
- Brief About Client
- Brief About Business
- Contact Data
- Social Media
- Website
- Other Additional Data

Explicitly excluded:

- Ad Account
- Pixel
- Business Manager
- Products
- Target Audience
- Offers

---

# 28. Client Custom Fields

Two scopes:

## Global

Field appears for all Clients.

## Client-Specific

Field appears for one Client.

Types:

- Text
- Number
- Date
- Link
- Yes/No

Custom Field values participate in Global Search.

Deleting a field requires choice:

1. Delete field + stored values.
2. Delete field definition while retaining historical values where technically supported.

---

# 29. Client Work History

Each entry:

- Date
- Activity
- Rich Content

Default date is today.

Supports:

- Text
- Images
- Files
- Links
- Edit
- Delete
- Search
- Date filters
- Custom date range

Task Updates related to Client appear automatically.

Manual Activities can also be added.

---

# 30. Client Agreement

Agreement is NOT Contract Management.

It is a collection of free-form Agreement Notes.

Each note:

- Content
- Date

Supports:

- Text
- Images
- Files
- Links
- Edit
- Delete

No formal:

- Start Date
- End Date
- Agreement category

---

# 31. Client General Notes

Separate from:

- Agreement
- Work History

Supports:

- One large note OR multiple notes
- Rich Content
- Images
- Files
- Links
- Edit
- Delete

Included in Global Search.

---

# 32. Client Operations

Supported:

- Bulk Status Change
- Bulk Delete
- Client Export

Client Clone is NOT supported.

## Client Export

Single Client export must include:

- Client Data
- Tasks
- Work History
- Agreement Notes
- Related Files
- Other related records

---

# 33. Client Delete / Restore

Deleting Client:

1. Confirmation
2. Client moves to Trash
3. Related Tasks move according to relationship policy
4. Work History moves according to relationship policy
5. Agreement moves according to relationship policy
6. Related files move according to relationship policy
7. Restore attempts to recover related records

Exact restore behavior for partially missing dependencies is a technical decision.

---

# 34. Files

Supported:

- Images
- PDFs
- Word
- Excel
- Other technically supported formats

File relationships:

- One/multiple Clients
- One/multiple Tasks
- Client + Task
- General File

## File Entity

```text
File
- id
- originalFilename
- displayName
- mimeType
- size
- storageKey
- folderId?
- tags[]
- createdAt
- updatedAt
- deletedAt?
```

## Operations

- Upload
- Rename
- Move
- Duplicate
- Delete
- Download
- Preview

Drag & Drop Upload required.

Original filename retained.

User may rename.

---

# 35. Folders

Folders are optional.

Nested folders supported.

Operations:

- Create
- Rename
- Delete
- Move
- Move into another folder

Deleting non-empty Folder requires Confirmation.

BRD states contents are deleted after confirmation; UX must clearly communicate this destructive behavior.

---

# 36. File Preview

Supported files should preview in-system when technically possible.

Unsupported / very large files may require Download.

No fixed product-level file size limit.

Actual limit depends on infrastructure.

---

# 37. Global Search

Global Search covers:

- Tasks
- Clients
- Client Data
- Custom Fields
- Work History
- Agreement Notes
- General Client Notes
- Courses
- Knowledge
- Files
- Activities
- Other searchable records

Excluded:

- Completed Tasks History

Completed Tasks History has its own Task Name search.

## Search Content

- Titles
- Names
- Metadata
- Rich Text
- Custom Field values

## Languages

- Arabic
- English
- Mixed

## Fuzzy Search

Search should support close matches.

Example:

Query:

`Facebook Ads`

may return:

`Create Facebook Ad`

when relevance is appropriate.

Exact fuzzy algorithm is TBD.

## Filters

- Module
- Tasks
- Clients
- Files
- Knowledge
- Courses
- Other supported sources

Saved Searches are not required.

---

# 38. Notifications

Notifications Center supports:

- Read
- Unread
- Mark All as Read
- Historical Notifications

Retention:

30 days.

Sources:

- Tasks
- Recurring Tasks
- Courses
- Clients
- Files
- Backup
- Storage
- Other important system events

Delivery:

- In-System
- Mobile Push

Course reminders are in-system.

Notifications can be disabled from Settings.

---

# 39. Reminder Engine

Task reminders:

- Default reminder
- Custom task reminder
- One day before
- Due date
- Overdue behavior
- Stronger Urgent notification

Tasks without Due Date do not receive due-date reminders.

Default Reminder Time is TBD.

Exact overdue notification behavior is TBD.

---

# 40. Trash

Central Trash contains:

- Tasks
- Clients
- Files
- Courses
- Knowledge
- Folders
- Other deletable records

Each item displays type.

Retention:

30 days.

After retention:

- Permanent deletion

Restore supported.

Permanent Delete:

- Manual
- Confirmation required
- Irreversible

Undo after normal deletion:

4 seconds.

---

# 41. Activity History

Activity History records important system operations.

Examples:

- Create
- Edit
- Delete
- Restore
- Important system operations

Retention:

90 days.

Features:

- Search
- Filters
- Clear History

General Activity History is NOT the same as Dashboard Client Recent Activity.

---

# 42. Settings

Settings include:

- Theme
- Default Reminder Time
- Notifications On/Off
- Backup
- Export
- Restore
- Trash settings where needed
- Categories
- Tags
- Custom Fields
- Dashboard Reset
- Reset All Settings

Reset All Settings:

- Restores defaults.
- Does NOT delete user data.

---

# 43. Backup

Automatic Backup:

- Daily
- Full system
- Cloud if technically possible

Retention:

30 days / latest backup policy as technically implemented.

Manual Backup/export:

- Selected Modules
- Data
- Files
- Combined Export
- ZIP for combined export

Backup implementation is dependent on storage architecture.

---

# 44. Restore

Restore is Full System Restore.

Behavior:

1. User selects backup.
2. System warns that current data will be replaced.
3. System creates automatic backup of current data.
4. Restore starts.
5. System validates restored data.
6. System reports success/failure.

Restore is destructive to current state and requires explicit confirmation.

---

# 45. Offline Mode

System SHALL support:

- Offline read
- Offline create
- Offline edit
- Offline delete
- Local persistence
- Sync after connection returns

The system must clearly show offline state.

Changes made offline are queued for synchronization.

---

# 46. Synchronization

Sync must support:

- Desktop
- Mobile
- Automatic synchronization
- Offline queue
- Server/local reconciliation

## Conflict Resolution

Required technical policy is TBD.

Recommended Solution Design must explicitly define:

- Conflict detection
- Conflict identity
- Last-write behavior or alternative
- Delete/update conflicts
- Relationship conflicts
- User-visible conflict handling if required

No silent destructive conflict resolution should be implemented without explicit design approval.

---

# 47. PWA

PWA must provide:

- Installability
- Responsive UI
- Offline capability
- App-like mobile experience
- Reconnection handling

PWA support is part of final production MVP.

---

# 48. Data Relationships

Core relationships:

```text
Client 1 ---- N Tasks
Client 1 ---- N WorkHistory
Client 1 ---- N AgreementNotes
Client 1 ---- N GeneralNotes

Task 1 ---- N Subtasks
Task 1 ---- N Updates
Task N ---- N Tags
Task N ---- N Files
Task N ---- 1 Client

Course N ---- 1 Category
Course 1 ---- N KnowledgeNotes

Knowledge N ---- 1 Category
Knowledge N ---- N Tags

File N ---- N Clients
File N ---- N Tasks
File N ---- 1 Folder
```

The exact relational/document database mapping is a Solution Design decision.

---

# 49. State Machines

## Task

```text
To Do
  ↓
In Progress
  ↓
Done

Done → To Do
Done → In Progress
```

Validation:

- Done blocked by incomplete required Subtasks.

## Client

```text
Upcoming
Active
Paused
Inactive
```

Transitions are manually controlled.

## Course

```text
To Learn → Done
```

## Knowledge

```text
Draft → Published
Published → Draft
```

---

# 50. Validation Rules

## Task

- title required
- priority required
- priority must be supported value
- status must be supported value
- due time requires due date
- no reminder based on due date when due date absent

## Course

- name required
- category required based on category design
- progress range 0–100
- status supported value

## Client

- name required
- start date defaulted automatically
- status supported value

## Knowledge

- title required
- category behavior defined
- status supported value

## File

- filename required
- mime type captured
- size captured
- storage reference required after successful upload

---

# 51. Error Handling

Every critical action must provide user-readable feedback.

Examples:

### Network Error

`Unable to connect. Your changes are saved locally and will sync when connection returns.`

### Save Error

`We couldn't save this change. Please try again.`

### Upload Error

`The file could not be uploaded.`

### Restore Error

`Restore failed. Your current data was not replaced.`

### Sync Conflict

`This item was changed on another device. Review the latest version before continuing.`

Exact copy may be refined during UX implementation.

---

# 52. Empty States

Every module must have an intentional Empty State.

Examples:

## Tasks

`No active tasks yet.`

CTA:

`+ Add Task`

## Clients

`No clients yet.`

CTA:

`+ Add Client`

## Learning

`No courses added yet.`

CTA:

`+ Add Course`

## Knowledge

`No knowledge notes yet.`

CTA:

`+ Add Knowledge`

## Files

`No files yet.`

CTA:

`Upload File`

Empty states must not look like system errors.

---

# 53. Loading States

All data-heavy screens require loading states.

For lists:

- Skeleton loading preferred.

For actions:

- Button loading state.
- Prevent duplicate submissions.

For uploads:

- Progress indicator when technically available.

---

# 54. Security Requirements

Because the system is Single-User but may use Cloud Sync:

1. Data must be transmitted securely.
2. Cloud credentials/secrets must never be exposed to frontend code.
3. File access must be authorized.
4. Backup access must be protected.
5. Restore must require explicit confirmation.
6. Destructive actions require confirmation.
7. Authentication strategy is TBD based on deployment model.
8. Local storage must not expose sensitive data unnecessarily.
9. If cloud authentication is introduced, sessions must be securely managed.

---

# 55. Performance Requirements

Exact numeric SLAs are TBD during Solution Design.

Minimum expected behavior:

- UI remains responsive with large task/client/course datasets.
- Search should not freeze the UI.
- Large file uploads should provide progress.
- Long lists should use appropriate rendering strategy.
- Dashboard should avoid loading every historical record unnecessarily.
- Search should use indexing appropriate to expected dataset size.

Recommended implementation:

- Pagination / virtualization where necessary.
- Lazy loading.
- Indexed local storage.
- Server-side search if cloud dataset requires it.

---

# 56. Accessibility

System SHALL provide:

- Readable typography
- Clear status indicators
- Adequate contrast
- Keyboard accessibility where practical
- Touch-friendly mobile controls
- Visible focus states
- Form validation messages
- Accessible labels for icon-only actions

---

# 57. Audit / Activity Requirements

Activity records should contain at minimum:

```text
Activity
- id
- type
- entityType
- entityId
- timestamp
- metadata
```

Examples:

```text
TASK_CREATED
TASK_UPDATED
TASK_COMPLETED
TASK_DELETED
TASK_RESTORED
CLIENT_CREATED
CLIENT_UPDATED
CLIENT_DELETED
COURSE_COMPLETED
KNOWLEDGE_CREATED
FILE_UPLOADED
FILE_DELETED
BACKUP_CREATED
RESTORE_STARTED
RESTORE_COMPLETED
```

Final event catalog is TBD.

---

# 58. API / Service Boundary

Even if the first version is implemented as a single application, the logical architecture should separate:

## Domain Services

- TaskService
- ClientService
- LearningService
- KnowledgeService
- FileService
- SearchService
- NotificationService
- BackupService
- SyncService
- ActivityService
- TrashService

## Cross-Cutting Services

- Validation
- Date/Timezone
- Error Handling
- Logging
- Storage
- Authentication/Security

This allows later architecture changes without changing business behavior.

---

# 59. Suggested API Operations

Exact API style is TBD.

Typical operations:

```text
Tasks
GET    /tasks
POST   /tasks
GET    /tasks/:id
PATCH  /tasks/:id
DELETE /tasks/:id

POST   /tasks/:id/complete
POST   /tasks/:id/reopen
POST   /tasks/:id/timer/start
POST   /tasks/:id/timer/pause
POST   /tasks/:id/timer/stop

Clients
GET    /clients
POST   /clients
GET    /clients/:id
PATCH  /clients/:id
DELETE /clients/:id

Courses
GET    /courses
POST   /courses
PATCH  /courses/:id
DELETE /courses/:id

Knowledge
GET    /knowledge
POST   /knowledge
PATCH  /knowledge/:id
DELETE /knowledge/:id

Files
POST   /files
GET    /files/:id
PATCH  /files/:id
DELETE /files/:id

Search
GET    /search?q=

Notifications
GET    /notifications
PATCH  /notifications/:id/read

Trash
GET    /trash
POST   /trash/:id/restore
DELETE /trash/:id/permanent

Backup
POST   /backup
GET    /backups

Restore
POST   /restore

Sync
POST   /sync/push
GET    /sync/pull
```

These are logical examples, not mandatory REST paths.

---

# 60. MVP-1 Detailed Scope — Task Execution

## Goal

Build a fully usable task management product.

## Screens

1. Tasks List
2. Task Details
3. Create/Edit Task
4. Calendar
5. Completed History
6. Task Templates
7. Tags Management

## MVP-1 Core Journey

```text
Open
→ View Tasks
→ Create Task
→ Add Priority
→ Add optional details
→ Save
→ Start Timer
→ Add Update
→ Complete Subtasks
→ Complete Task
→ Timer stops
→ Task moves to History
→ Reopen if needed
```

## MVP-1 Acceptance

A real user can manage a full working day without needing Dashboard, Clients, Learning, Files, or Cloud Sync.

## MVP-1 Exit Criteria

- Task CRUD works.
- Status works.
- Priority works.
- Subtasks work.
- Tags work.
- Notes work.
- Updates work.
- Recurrence works.
- Templates work.
- Timer works.
- History works.
- Responsive UI works.
- Critical E2E tests pass.

---

# 61. MVP-2 Detailed Scope — Command Center

## Goal

Turn MVP-1 into a daily operating system.

## Added

- Dashboard
- Quick Add
- Calendar
- Notifications
- Reminders
- Search
- Dashboard Customization

## Core Journey

```text
Open Dashboard
→ Understand Today
→ See Urgent / Overdue
→ Quick Add
→ Open Task
→ Work
→ Timer
→ Receive Reminder
→ Search old active information
→ Continue execution
```

## MVP-2 Exit Criteria

- Dashboard answers "What do I need to do now?"
- Quick Add works.
- Calendar works.
- Reminder engine works.
- Notifications work.
- Search works for included entities.
- Dashboard customization persists.

---

# 62. MVP-3 Detailed Scope — Learning & Knowledge

## Goal

Create a closed learning loop.

```text
Course
→ Learn
→ Track Progress
→ Take Notes
→ Extract Knowledge
→ Publish Knowledge
→ Search / Reuse
```

## Exit Criteria

- Course CRUD
- Category management
- Progress
- Course notes
- Course reminders
- Knowledge CRUD
- Knowledge categories
- Tags
- Pin
- Search
- Course relationship

All work without external LMS integration.

External course integrations remain optional.

---

# 63. MVP-4 Detailed Scope — Client Workspace

## Goal

Manage client context without leaving the system.

## Core Journey

```text
Create Client
→ Add Client Data
→ Create Client Task
→ Work
→ Add Task Updates
→ Work History updated
→ Add Agreement Note
→ Add General Note
→ Attach Files
→ Search Client
→ Export Client
```

## Exit Criteria

- Client CRUD
- Status
- Search
- Work History
- Agreement
- Notes
- Custom Fields
- Client Tasks
- Client Files relationships
- Export
- Delete/Restore behavior tested

---

# 64. MVP-5 Detailed Scope — Files & Recovery

## Goal

Make the system a reliable source of truth.

## Core Journey

```text
Upload
→ Organize
→ Link to Client/Task
→ Preview
→ Download
→ Delete
→ Trash
→ Restore
```

Backup Journey:

```text
Automatic Backup
→ Backup Retained
→ User Export
→ Restore Request
→ Safety Backup
→ Restore
→ Validation
```

## Exit Criteria

- File upload
- File relations
- Folders
- Preview
- Trash
- Restore
- Activity History
- Backup
- Export
- Restore
- Storage warning

---

# 65. MVP-6 Detailed Scope — Offline & Production

## Goal

Production reliability across devices.

## Core Journey

```text
Open App
→ Offline
→ Create/Edit
→ Local Save
→ Connection Returns
→ Sync
→ Resolve Conflicts
→ Data Consistent
```

## Exit Criteria

- PWA install
- Offline read/write
- Sync queue
- Reconnection
- Conflict resolution
- Push notifications
- Production performance
- Security review
- Recovery tests
- Cross-device testing

---

# 66. Development Workflow Per MVP

كل MVP يجب أن ينفذ بهذا الترتيب:

## Step 1 — Requirement Freeze

- Confirm scope.
- Confirm acceptance criteria.
- Record TBDs.

## Step 2 — UX Flow

- Screen map.
- User journey.
- Empty/loading/error states.
- Mobile behavior.

## Step 3 — Data Design

- Entities.
- Relationships.
- Constraints.
- Indexes.
- Migration plan.

## Step 4 — Backend / Domain

- Services.
- Validation.
- Business rules.
- Persistence.

## Step 5 — Frontend

- Screens.
- Forms.
- Lists.
- States.
- Responsive behavior.

## Step 6 — Integration

- Connect UI to domain/data.
- Handle errors.
- Handle loading.

## Step 7 — Testing

- Unit.
- Integration.
- E2E.
- Regression.

## Step 8 — User Acceptance

Run the MVP core journey with real scenarios.

## Step 9 — Release

Tag/version the MVP.

## Step 10 — Freeze

Do not add next-phase scope until MVP is accepted.

---

# 67. Definition of Done

A Feature is Done when:

- Requirement implemented.
- Validation implemented.
- Error state implemented.
- Loading state implemented.
- Empty state implemented where applicable.
- Mobile responsive.
- Data persisted.
- Existing functionality not broken.
- Tests pass.
- Acceptance criteria pass.
- No known blocker.
- User journey tested.

An MVP is Done only when all its Features satisfy Definition of Done.

---

# 68. Testing Strategy

## Unit Tests

Test:

- Task status transitions
- Priority validation
- Recurrence calculations
- Monthly last-day rule
- Timer calculations
- Reminder calculation
- Trash retention
- Activity retention
- Search normalization
- Progress validation

## Integration Tests

Test:

- Task + Client
- Task + Tags
- Task + Files
- Course + Knowledge
- Client + Work History
- Client + Tasks
- Delete + Trash
- Restore + Relationships

## E2E

Critical scenarios:

1. Create and complete Task.
2. Create recurring Task.
3. Start/stop Timer.
4. Create Client and Task.
5. Create Course and Knowledge.
6. Upload File.
7. Delete and Restore.
8. Search across modules.
9. Backup and Restore.
10. Offline create → Online sync.

---

# 69. Critical Acceptance Scenarios

## Scenario 1 — Task Completion

Given:

- Task exists.
- Required Subtasks complete.

When:

- User marks Task Done.

Then:

- Task status = Done.
- completedAt set.
- Timer stopped.
- Task removed from active list.
- Task appears in Completed History.

## Scenario 2 — Blocked Completion

Given:

- Required Subtask incomplete.

When:

- User tries to mark parent Done.

Then:

- System blocks completion.
- User sees clear reason.

## Scenario 3 — Urgent Task

Given:

- Task priority = Urgent.
- No Due Date.

Then:

- Task appears in Urgent section.
- Task has no due-date reminder.
- Task remains Urgent.

## Scenario 4 — Recurrence

Given:

- Monthly task on day 31.

When:

- Month has 30 days.

Then:

- Occurrence runs on last day.

## Scenario 5 — Timer

Given:

- Task A timer active.

When:

- User starts Task B timer.

Then:

- Task A timer stops.
- Task A actual time updated.
- Task B timer becomes active.

## Scenario 6 — Client Update

Given:

- Task linked to Client.

When:

- User adds Task Update.

Then:

- Update appears in Task.
- Historical copy appears in Client Work History.

Editing original Update does not alter historical copy.

## Scenario 7 — Delete

Given:

- User deletes a Task.

Then:

- Confirmation shown.
- Undo available for 4 seconds.
- Task enters Trash.

## Scenario 8 — Restore

Given:

- Task exists in Trash.

When:

- User restores.

Then:

- Task returns to previous usable state where possible.

---

# 70. Retention Policies

| Data | Retention |
|---|---:|
| Notifications | 30 days |
| Trash | 30 days |
| Activity History | 90 days |
| Backups | 30 days / final policy TBD |
| Completed Tasks | No automatic retention specified |
| Client History | No automatic retention specified |
| Knowledge | No automatic retention specified |
| Files | No automatic retention specified |

---

# 71. Technical Decisions Required Before Production

These must be explicitly decided during Solution Design:

1. Frontend framework.
2. Backend architecture.
3. Database.
4. Local offline database.
5. Cloud hosting.
6. Cloud file storage.
7. Authentication/security model.
8. Sync protocol.
9. Conflict resolution.
10. Search engine.
11. Fuzzy Arabic search strategy.
12. Rich Text Editor.
13. File preview libraries.
14. Push notification provider.
15. Backup storage.
16. Backup versioning.
17. Export schema.
18. Course integrations.
19. Maximum practical file size.
20. Storage warning threshold.
21. Default reminder time.
22. Exact overdue notification behavior.
23. Activity event catalog.
24. Recurring task update model.
25. Restore partial dependency behavior.

---

# 72. Recommended Technical Defaults

These are recommendations, NOT fixed requirements.

The implementation team should evaluate:

## Frontend

A modern TypeScript-based responsive web framework.

## PWA

Service Worker + installable manifest.

## Local Data

Indexed local database suitable for offline-first operation.

## Search

Indexed full-text search locally for offline data, with server-side indexing if cloud scale requires it.

## Files

Object storage rather than storing large binary files directly in the primary database.

## Rich Content

Structured rich-text JSON rather than raw unsafe HTML.

## Sync

Change queue with record versioning.

## IDs

UUID/ULID-style identifiers.

## Timestamps

UTC persistence + Egypt timezone presentation, unless architecture requires another explicit strategy.

These recommendations require technical validation before implementation.

---

# 73. Data Migration

Every MVP must provide a migration strategy.

Database schema changes must be versioned.

Example:

```text
Migration 001 — Core Tasks
Migration 002 — Dashboard
Migration 003 — Learning
Migration 004 — Clients
Migration 005 — Files/Recovery
Migration 006 — Offline/Sync
```

Migrations must be:

- Repeatable where possible.
- Tested.
- Backward-aware where required.
- Included in release notes.

---

# 74. Observability

Production version should capture:

- Application errors
- Sync failures
- Backup failures
- Restore failures
- Upload failures
- Notification failures
- Performance issues

Logs must not expose sensitive user content unnecessarily.

---

# 75. Analytics

Product analytics are optional because this is Single-User.

If enabled, analytics should focus on technical/product health:

- Feature usage
- Errors
- Sync status
- Backup success
- Performance

Do not make analytics a dependency for core functionality.

---

# 76. Traceability Matrix

| BRD Area | SRS |
|---|---|
| Tasks | FR-TASK + Task sections |
| Dashboard | Dashboard |
| Learning | Learning |
| Knowledge | Knowledge |
| Clients | Clients |
| Files | Files |
| Search | Global Search |
| Notifications | Notifications |
| Trash | Trash |
| Activity | Activity History |
| Backup | Backup |
| Restore | Restore |
| Offline | Offline Mode |
| Sync | Synchronization |
| PWA | PWA |
| Settings | Settings |
| Security | Security Requirements |
| Performance | Performance Requirements |

---

# 77. BRD Requirement Coverage

## Core Priority

BRD priority:

1. Tasks
2. Dashboard
3. Learning
4. Clients
5. Files

SRS MVP order:

1. Task Execution
2. Command Center
3. Learning & Knowledge
4. Client Workspace
5. Files & Recovery
6. Offline & Production

The SRS preserves the BRD priority while grouping supporting features into usable product slices.

---

# 78. Important Requirement Interpretation

The BRD explicitly defines the product as a Single-User system and says Email/Password authentication is not required in MVP.

Therefore:

- Authentication is not a prerequisite for MVP-1.
- Security architecture still must be defined before cloud production.
- If cloud sync is introduced, identity and authorization cannot remain undefined.

The BRD also identifies Offline Sync, Backup, Push Notifications, Search, File Storage, and Course Integrations as technical dependencies. These are therefore treated as Solution Design decisions rather than invented product requirements.

---

# 79. Ambiguities / Clarifications To Resolve

These do not block MVP-1.

## A. Recurring Task Editing

Need exact UX:

- Edit this occurrence only?
- Edit this and future?
- Edit entire series?

BRD currently states current + future behavior, but implementation needs explicit data semantics.

## B. Course Category Deletion

BRD says deleting a Category deletes its Courses.

This is destructive and unusual compared with Knowledge Category behavior.

Need confirmation before production.

## C. Folder Deletion

BRD says deleting non-empty Folder deletes contents.

Need explicit confirmation wording and recovery behavior.

## D. Client Restore

Need policy when:

- Client restored
- Related file permanently deleted
- Related task was independently deleted

## E. Offline Conflict

Need exact conflict algorithm.

## F. Backup Retention

Need exact meaning of:

- Latest Backup
- 30-day retention
- Number of versions

## G. Push Notifications

Need provider and platform support.

## H. External Course Integrations

Need supported platforms, if any.

---

# 80. Recommended First Implementation Sequence

## Sprint / Build 1

Foundation:

- Project setup
- Routing
- Design system
- Database
- Task entity
- Task CRUD
- Status
- Priority

**Output:** Basic working Task App.

## Sprint / Build 2

- Subtasks
- Tags
- Notes
- Attachments
- Task Updates

**Output:** Complete Task workspace.

## Sprint / Build 3

- Recurrence
- Templates
- Timer
- Completed History

**Output:** MVP-1.

## Sprint / Build 4

- Dashboard
- Quick Add
- Calendar

**Output:** Daily Command Center.

## Sprint / Build 5

- Notifications
- Reminders
- Search
- Dashboard customization

**Output:** MVP-2.

## Sprint / Build 6

- Courses
- Categories
- Progress
- Notes

## Sprint / Build 7

- Knowledge
- Categories
- Tags
- Search
- Course relationship

**Output:** MVP-3.

## Sprint / Build 8

- Clients
- Profile
- Status
- Tasks

## Sprint / Build 9

- Work History
- Agreement
- Notes
- Custom Fields
- Export

**Output:** MVP-4.

## Sprint / Build 10

- Files
- Folders
- Preview
- Relationships

## Sprint / Build 11

- Trash
- Activity
- Backup
- Restore
- Storage warnings

**Output:** MVP-5.

## Sprint / Build 12

- PWA
- Offline
- Sync
- Conflict resolution
- Push
- Production hardening

**Output:** MVP-6 / Production Release.

---

# 81. Definition of MVP

في هذا المشروع:

> MVP لا يعني "نسخة ناقصة".

الـMVP يعني:

> Smallest complete product slice that provides a real user outcome end-to-end.

لذلك:

### MVP-1

ليس مجرد CRUD للـTasks.

بل:

Create → Plan → Execute → Track Time → Update → Complete → Reopen

### MVP-2

ليس مجرد Dashboard.

بل:

Open → Understand → Plan → Execute → Receive Reminder → Search → Continue

### MVP-3

ليس مجرد Course CRUD.

بل:

Learn → Track → Note → Extract Knowledge → Organize → Search

### MVP-4

ليس مجرد Client CRUD.

بل:

Client → Work → Task → Update → History → Agreement → Notes → Export

### MVP-5

ليس مجرد File Upload.

بل:

Store → Organize → Relate → Preview → Delete → Restore → Backup

### MVP-6

ليس مجرد Offline checkbox.

بل:

Work Offline → Save Locally → Reconnect → Sync → Resolve → Consistent State

---

# 82. Final Product Architecture Concept

```text
                    ┌─────────────────────┐
                    │      Dashboard      │
                    │   Command Center    │
                    └──────────┬──────────┘
                               │
       ┌───────────────┬───────┼────────┬───────────────┐
       │               │       │        │               │
    Tasks           Clients  Learning Knowledge       Files
       │               │       │        │               │
       └───────────────┴───────┴────────┴───────────────┘
                               │
                  ┌────────────┴────────────┐
                  │      Core Services      │
                  │ Search / Notifications  │
                  │ Activity / Trash        │
                  │ Backup / Restore        │
                  └────────────┬────────────┘
                               │
                  ┌────────────┴────────────┐
                  │ Infrastructure Layer   │
                  │ Database / Storage      │
                  │ Offline / Sync          │
                  │ PWA / Push              │
                  └─────────────────────────┘
```

---

# 83. Implementation Handoff Checklist

قبل أن يبدأ المطور:

- [ ] SRS approved
- [ ] MVP-1 scope frozen
- [ ] UX wireframes for MVP-1
- [ ] Database schema MVP-1
- [ ] API/domain contracts
- [ ] Validation rules
- [ ] Error states
- [ ] Empty states
- [ ] Acceptance criteria
- [ ] Test cases
- [ ] Definition of Done
- [ ] Git/repository setup
- [ ] Environment setup
- [ ] Migration strategy
- [ ] Deployment strategy

قبل الانتقال إلى MVP-2:

- [ ] MVP-1 accepted
- [ ] Critical bugs = 0
- [ ] Data integrity verified
- [ ] Regression tests pass
- [ ] User journey validated
- [ ] Release tagged

---

# 84. Final Recommendation

الـBRD الحالي قوي جدًا من ناحية Business Discovery، لكنه كان يضع Features كثيرة في نفس المستوى.

الـSRS يعالج هذا عن طريق:

1. تحويل المتطلبات إلى Functional Requirements.
2. تعريف System Behavior.
3. تعريف Data Model.
4. تعريف Validation.
5. تعريف Acceptance Criteria.
6. تعريف حالات الـLoading/Error/Empty.
7. فصل Business Rules عن Technical Decisions.
8. تحويل المشروع إلى 6 MVPs.
9. جعل كل MVP قابلًا للاستخدام End-to-End.
10. وضع Gate واضح يمنع الانتقال للمرحلة التالية قبل قبول المرحلة الحالية.

الترتيب النهائي:

```text
MVP-1
Task Execution
        ↓
MVP-2
Personal Command Center
        ↓
MVP-3
Learning & Knowledge
        ↓
MVP-4
Client Workspace
        ↓
MVP-5
Files & Recovery
        ↓
MVP-6
Offline & Production
```

والقاعدة الأساسية:

> لا نبدأ Phase جديدة لمجرد أن Features الـPhase الحالية اتكتبت؛ نبدأها فقط بعد أن يكون الـMVP السابق قابلًا للتشغيل، الاختبار، والاستخدام الحقيقي.
