# orm-more-queries


    raise FieldError(
django.core.exceptions.FieldError: Cannot resolve keyword 'receipe_view_count' into field. Choices are: id, receipe_description, receipe_image, receipe_name, reciepe_view_count, user, user_id
>>> Receipe.objects.filter(reciepe_view_count=55)
<QuerySet [<Receipe: Receipe object (9)>]>
>>> Receipe.objects.filter(reciepe_view_count __lte=55)
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 63, in runsource
    code = self.compile(source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 178, in __call__
    return _maybe_compile(self.compiler, source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 106, in _maybe_compile
    raise err1
  File "/usr/lib/python3.8/codeop.py", line 93, in _maybe_compile
    code1 = compiler(source + "\n", filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 143, in __call__
    codeob = compile(source, filename, symbol, self.flags, 1)
  File "<console>", line 1
    Receipe.objects.filter(reciepe_view_count __lte=55)
                                              ^
SyntaxError: invalid syntax
>>> Receipe.objects.filter(reciepe_view_count__lte=55)
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>]>
>>> Receipe.objects.filter(reciepe_view_count__lte=55)
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>]>
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py makemigrations
Migrations for 'vege':
  vege/migrations/0004_department_studentid_student.py
    - Create model Department
    - Create model StudentID
    - Create model Student
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions, vege
Running migrations:
  Applying vege.0004_department_studentid_student... OK
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py runserver
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
February 14, 2024 - 11:21:43
Django version 4.2.10, using settings 'recepe_project.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

Not Found: /
[14/Feb/2024 11:21:46] "GET / HTTP/1.1" 404 3122
Not Found: /favicon.ico
[14/Feb/2024 11:21:51] "GET /admin/ HTTP/1.1" 302 0
[14/Feb/2024 11:21:51] "GET /admin/login/?next=/admin/ HTTP/1.1" 200 4181
[14/Feb/2024 11:22:01] "POST /admin/login/?next=/admin/ HTTP/1.1" 302 0
[14/Feb/2024 11:22:02] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:02] "GET /static/admin/img/icon-changelink.svg HTTP/1.1" 200 380
[14/Feb/2024 11:22:02] "GET /static/admin/img/icon-addlink.svg HTTP/1.1" 200 331
[14/Feb/2024 11:22:06] "GET /admin/vege/studentid/ HTTP/1.1" 200 8349
[14/Feb/2024 11:22:06] "GET /static/admin/css/changelists.css HTTP/1.1" 200 6566
[14/Feb/2024 11:22:06] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:22:07] "GET /static/admin/js/filters.js HTTP/1.1" 200 978
[14/Feb/2024 11:22:07] "GET /static/admin/img/tooltag-add.svg HTTP/1.1" 200 331
[14/Feb/2024 11:22:08] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:09] "GET /admin/vege/receipe/ HTTP/1.1" 200 11018
[14/Feb/2024 11:22:09] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:22:10] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:11] "GET /admin/vege/department/ HTTP/1.1" 200 8351
[14/Feb/2024 11:22:11] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:22:12] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:13] "GET /admin/vege/student/ HTTP/1.1" 200 8330
[14/Feb/2024 11:22:13] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:22:14] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:16] "GET /admin/vege/receipe/2/change/ HTTP/1.1" 302 0
[14/Feb/2024 11:22:16] "GET /admin/ HTTP/1.1" 200 8282
[14/Feb/2024 11:22:16] "GET /static/admin/img/icon-alert.svg HTTP/1.1" 200 504
[14/Feb/2024 11:22:17] "GET /admin/login/?next=/admin/ HTTP/1.1" 302 0
[14/Feb/2024 11:22:17] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:19] "GET /admin/ HTTP/1.1" 200 8112
[14/Feb/2024 11:22:59] "GET /admin/vege/department/ HTTP/1.1" 200 8351
[14/Feb/2024 11:22:59] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:00] "GET /admin/vege/department/add/ HTTP/1.1" 200 9147
[14/Feb/2024 11:23:01] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:01] "GET /static/admin/js/prepopulate_init.js HTTP/1.1" 200 586
[14/Feb/2024 11:23:11] "POST /admin/vege/department/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:23:11] "GET /admin/vege/department/add/ HTTP/1.1" 200 9388
[14/Feb/2024 11:23:11] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:11] "GET /static/admin/img/icon-yes.svg HTTP/1.1" 200 436
[14/Feb/2024 11:23:21] "POST /admin/vege/department/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:23:21] "GET /admin/vege/department/add/ HTTP/1.1" 200 9399
[14/Feb/2024 11:23:21] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:27] "POST /admin/vege/department/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:23:27] "GET /admin/vege/department/add/ HTTP/1.1" 200 9393
[14/Feb/2024 11:23:28] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:33] "POST /admin/vege/department/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:23:33] "GET /admin/vege/department/add/ HTTP/1.1" 200 9393
[14/Feb/2024 11:23:33] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:37] "POST /admin/vege/department/add/ HTTP/1.1" 200 9290
[14/Feb/2024 11:23:37] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:23:39] "GET /admin/vege/department/ HTTP/1.1" 200 10149
[14/Feb/2024 11:23:39] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:03] "GET /admin/vege/department/add/ HTTP/1.1" 200 9147
[14/Feb/2024 11:24:04] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:15] "POST /admin/vege/department/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:24:15] "GET /admin/vege/department/add/ HTTP/1.1" 200 9395
[14/Feb/2024 11:24:15] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:16] "GET /admin/vege/department/ HTTP/1.1" 200 10363
[14/Feb/2024 11:24:17] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:25] "GET /admin/vege/studentid/ HTTP/1.1" 200 8349
[14/Feb/2024 11:24:25] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:39] "GET /admin/vege/studentid/add/ HTTP/1.1" 200 9143
[14/Feb/2024 11:24:40] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:51] "POST /admin/vege/studentid/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:24:51] "GET /admin/vege/studentid/ HTTP/1.1" 200 9711
[14/Feb/2024 11:24:51] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:24:56] "GET /admin/vege/studentid/1/change/ HTTP/1.1" 200 9366
[14/Feb/2024 11:24:56] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:02] "GET /admin/vege/ HTTP/1.1" 200 6328
[14/Feb/2024 11:25:06] "GET /admin/vege/student/ HTTP/1.1" 200 8330
[14/Feb/2024 11:25:06] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:18] "GET /admin/vege/student/ HTTP/1.1" 200 8330
[14/Feb/2024 11:25:18] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:23] "GET /admin/vege/student/add/ HTTP/1.1" 200 14623
[14/Feb/2024 11:25:23] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:23] "GET /static/admin/img/icon-viewlink.svg HTTP/1.1" 200 581
[14/Feb/2024 11:25:47] "POST /admin/vege/student/add/ HTTP/1.1" 302 0
[14/Feb/2024 11:25:47] "GET /admin/vege/student/add/ HTTP/1.1" 200 14865
[14/Feb/2024 11:25:47] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:48] "GET /admin/vege/student/ HTTP/1.1" 200 9486
[14/Feb/2024 11:25:49] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:50] "GET /admin/vege/student/1/change/ HTTP/1.1" 200 14901
[14/Feb/2024 11:25:50] "GET /admin/jsi18n/ HTTP/1.1" 200 3343
[14/Feb/2024 11:25:51] "GET /admin/vege/student/ HTTP/1.1" 200 9486
^Cjayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ pytohn3 manage.py shell

Command 'pytohn3' not found, did you mean:

  command 'python3' from deb python3 (3.8.2-0ubuntu2)

Try: sudo apt install <deb name>

jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/django_project1/recepe_project/vege/seed.py", line 1, in <module>
    from faker import Faker
ModuleNotFoundError: No module named 'faker'
>>> 
KeyboardInterrupt
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ pip3 install faker
Collecting faker
  Downloading Faker-23.1.0-py3-none-any.whl (1.7 MB)
     |████████████████████████████████| 1.7 MB 1.7 MB/s 
Requirement already satisfied: typing-extensions>=3.10.0.1; python_version <= "3.8" in /home/jayendra/.local/lib/python3.8/site-packages (from faker) (4.9.0)
Requirement already satisfied: python-dateutil>=2.4 in /usr/lib/python3/dist-packages (from faker) (2.7.3)
Installing collected packages: faker
Successfully installed faker-23.1.0
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
local variable 'student_id_obj' referenced before assignment
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
unsupported operand type(s) for -: 'str' and 'str'
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
unsupported operand type(s) for -: 'str' and 'str'
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
Student() got unexpected keyword arguments: 'Student_id', 'Student_name', 'Student_email', 'Student_age'
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
name 'student_id' is not defined
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
StudentID() got unexpected keyword arguments: 'student_id'
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
StudentID() got unexpected keyword arguments: 'student_id'
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py makemigrations
Was studentid.Student_id renamed to studentid.student_id (a CharField)? [y/N] y
Migrations for 'vege':
  vege/migrations/0005_rename_student_id_studentid_student_id.py
    - Rename field Student_id on studentid to student_id
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions, vege
Running migrations:
  Applying vege.0005_rename_student_id_studentid_student_id... OK
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.seed import *
>>> seed_db()
>>> seed_db()
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.models import *
>>> queryset=Student.objects.filter(student_name__startwith="jay")
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/manager.py", line 87, in manager_method
    return getattr(self.get_queryset(), name)(*args, **kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1436, in filter
    return self._filter_or_exclude(False, args, kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1454, in _filter_or_exclude
    clone._filter_or_exclude_inplace(negate, args, kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1461, in _filter_or_exclude_inplace
    self._query.add_q(Q(*args, **kwargs))
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1546, in add_q
    clause, _ = self._add_q(q_object, self.used_aliases)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1577, in _add_q
    child_clause, needed_inner = self.build_filter(
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1492, in build_filter
    condition = self.build_lookup(lookups, col, value)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1313, in build_lookup
    lhs = self.try_transform(lhs, lookup_name)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1357, in try_transform
    raise FieldError(
django.core.exceptions.FieldError: Unsupported lookup 'startwith' for CharField or join on the field not permitted, perhaps you meant startswith or istartswith?
>>> queryset=Student.objects.filter(student_name__startswith="jay")
>>> queryset
<QuerySet [<Student: Jayendra sharma>]>
>>> queryset=Student.objects.filter(student_name__startswith="j")
>>> queryset
<QuerySet [<Student: Jacqueline Olson>, <Student: James Brown>, <Student: James Jones>, <Student: James Lambert>, <Student: James Terry>, <Student: Jamie Boyd>, <Student: Jane Taylor>, <Student: Jason Clark>, <Student: Jason Gentry>, <Student: Jayendra sharma>, <Student: Jeffrey Herring>, <Student: Jennifer Fitzpatrick>, <Student: Jennifer Lopez>, <Student: Jennifer Miller>, <Student: Jennifer Nichols>, <Student: Jennifer Perkins>, <Student: Jennifer Wong>, <Student: Jessica Davidson>, <Student: Jim Herrera>, <Student: Joan Cooper>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.filter(student_name__endswith="j")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_name__endswith="a")
>>> queryset
<QuerySet [<Student: Jayendra sharma>, <Student: Jim Herrera>, <Student: John Estrada>, <Student: Lindsey Ochoa>, <Student: Luis Mendoza>, <Student: Thomas Garza>, <Student: Timothy Herrera>]>
>>> queryset=Student.objects.filter(student_email__endswith="a")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_email__startswith="a")
>>> queryset
<QuerySet [<Student: Anne Mitchell>, <Student: Benjamin Gonzalez>, <Student: Christopher Hood>, <Student: Cody Johnston>, <Student: Corey Hawkins>, <Student: Hailey Dickerson>, <Student: Jayendra sharma>, <Student: Jennifer Lopez>, <Student: Jennifer Wong>, <Student: Kelly Austin>, <Student: Mark Fields>, <Student: Samuel Alexander>, <Student: Thomas Garza>]>
>>> queryset=Student.objects.filter(student_email__startswith=".com")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_email__endswith=".com")
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anne Mitchell>, <Student: Antonio Guzman>, <Student: Benjamin Mckinney>, <Student: Charles Case>, <Student: Christina Lopez>, <Student: Cory Garrett>, <Student: David Johnson>, <Student: David Scott>, <Student: David Spencer>, <Student: Denise Osborn>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, '...(remaining elements truncated)...']>
>>> for q in queryset:
...     print(q.student_email)
... 
stevenbeard@example.com
thomas36@example.com
sarahperez@example.com
rodriguezjohn@example.com
michaelwilson@example.com
kristipatel@example.com
jennifer38@example.com
adam34@example.com
desireechandler@example.com
leslierichardson@example.com
knichols@example.com
hicksnathan@example.com
xandrews@example.com
markreyes@example.com
xcowan@example.com
tlopez@example.com
jonathanromero@example.com
nicoleevans@example.com
brendapham@example.com
cynthia75@example.com
loribaker@example.com
jbeck@example.com
nbarnett@example.com
davidnguyen@example.com
larryjones@example.com
jenniferharris@example.com
erinsavage@example.com
loganchristian@example.com
jfox@example.com
jenniferlee@example.com
katelyn05@example.com
abc@gmail.com
jaimelewis@example.com
john91@example.com
summeroliver@example.com
zanderson@example.com
clarencemoore@example.com
collinsdiana@example.com
johnmiller@example.com
lisalee@example.com
dfox@example.com
chavezerica@example.com
deckerrodney@example.com
william09@example.com
sylviamurray@example.com
weaverstefanie@example.com
frosales@example.com
jason11@example.com
ryannancy@example.com
eorozco@example.com
ryanthompson@example.com
holmeschris@example.com
oreyes@example.com
angeladavidson@example.com
courtney40@example.com
rebeccaflores@example.com
colemankenneth@example.com
lijeffery@example.com
danielfry@example.com
pwhite@example.com
>>> queryset=Student.objects.filter(student_email__endswith=".gmail")
>>>     print(q.student_email)
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 63, in runsource
    code = self.compile(source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 178, in __call__
    return _maybe_compile(self.compiler, source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 106, in _maybe_compile
    raise err1
  File "/usr/lib/python3.8/codeop.py", line 93, in _maybe_compile
    code1 = compiler(source + "\n", filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 143, in __call__
    codeob = compile(source, filename, symbol, self.flags, 1)
  File "<console>", line 1
    print(q.student_email)
    ^
IndentationError: unexpected indent
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_email__endswith=".gmail")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_email__endswith=".yahoo")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_email__endswith=".com")
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anne Mitchell>, <Student: Antonio Guzman>, <Student: Benjamin Mckinney>, <Student: Charles Case>, <Student: Christina Lopez>, <Student: Cory Garrett>, <Student: David Johnson>, <Student: David Scott>, <Student: David Spencer>, <Student: Denise Osborn>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.filter(student_email__startswith=".hotmail")
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(student_name__endswith="l")
>>> queryset
<QuerySet [<Student: Adrian Wall>, <Student: Alicia Campbell>, <Student: Ann Campbell>, <Student: Anne Mitchell>, <Student: Ashley Randall>, <Student: Doris Powell>, <Student: Kristen Hall>, <Student: Mary Campbell>, <Student: Shane Carroll>, <Student: Timothy Campbell>, <Student: William Mcdaniel>]>
>>> queryset=Student.objects.filter(student_name__startswith("a"))
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'student_name__startswith' is not defined
>>> queryset=Student.objects.filter(student_name__startswith="a")
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>]>
>>> queryset=Student.objects.filter(student_name__icontains="a")
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>, <Student: Benjamin Gonzalez>, <Student: Benjamin Mckinney>, '...(remaining elements truncated)...']>
>>> queryset[0].student_id
<StudentID: STU-0397>
>>> queryset[1].student_id
<StudentID: STU-0146>
>>> queryset[1].id
11
>>> queryset[0].id
63
>>> queryset[0].pk
63
>>> queryset[1].pk
11
>>> queryset[0].department
<Department: Electrical>
>>> queryset[2].department
<Department: Biotechnical>
>>> queryset[67].department
<Department: Biotechnical>
>>> queryset[100].department
<Department: Civil>
>>> queryset[100].department.department
'Civil'
>>> queryset[100].department
<Department: Civil>
>>> queryset=Student.objects.filter(department__deparment="Civil")
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/manager.py", line 87, in manager_method
    return getattr(self.get_queryset(), name)(*args, **kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1436, in filter
    return self._filter_or_exclude(False, args, kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1454, in _filter_or_exclude
    clone._filter_or_exclude_inplace(negate, args, kwargs)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1461, in _filter_or_exclude_inplace
    self._query.add_q(Q(*args, **kwargs))
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1546, in add_q
    clause, _ = self._add_q(q_object, self.used_aliases)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1577, in _add_q
    child_clause, needed_inner = self.build_filter(
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1492, in build_filter
    condition = self.build_lookup(lookups, col, value)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1313, in build_lookup
    lhs = self.try_transform(lhs, lookup_name)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1357, in try_transform
    raise FieldError(
django.core.exceptions.FieldError: Unsupported lookup 'deparment' for ForeignKey or join on the field not permitted.
>>> queryset=Student.objects.filter(department__department="Civil")
>>> queryset
<QuerySet [<Student: Andre Beck>, <Student: Andrew Simon>, <Student: Anthony Smith>, <Student: Christina Wells>, <Student: Cory Garrett>, <Student: Dawn Cole>, <Student: Debra Davis>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, <Student: Donald Pitts>, <Student: Heather Petty>, <Student: Jamie Boyd>, <Student: Jeffrey Herring>, <Student: Jennifer Lopez>, <Student: Jennifer Nichols>, <Student: John Estrada>, <Student: John Gibbs>, <Student: Johnny Fisher>, <Student: Kyle Wilcox>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.filter(department__department__icontains="Civ")
>>> queryset
<QuerySet [<Student: Andre Beck>, <Student: Andrew Simon>, <Student: Anthony Smith>, <Student: Christina Wells>, <Student: Cory Garrett>, <Student: Dawn Cole>, <Student: Debra Davis>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, <Student: Donald Pitts>, <Student: Heather Petty>, <Student: Jamie Boyd>, <Student: Jeffrey Herring>, <Student: Jennifer Lopez>, <Student: Jennifer Nichols>, <Student: John Estrada>, <Student: John Gibbs>, <Student: Johnny Fisher>, <Student: Kyle Wilcox>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.filter(department__department__startswith="Civ")
>>> queryset
<QuerySet [<Student: Andre Beck>, <Student: Andrew Simon>, <Student: Anthony Smith>, <Student: Christina Wells>, <Student: Cory Garrett>, <Student: Dawn Cole>, <Student: Debra Davis>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, <Student: Donald Pitts>, <Student: Heather Petty>, <Student: Jamie Boyd>, <Student: Jeffrey Herring>, <Student: Jennifer Lopez>, <Student: Jennifer Nichols>, <Student: John Estrada>, <Student: John Gibbs>, <Student: Johnny Fisher>, <Student: Kyle Wilcox>, '...(remaining elements truncated)...']>
>>>  queryset.count()
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 63, in runsource
    code = self.compile(source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 178, in __call__
    return _maybe_compile(self.compiler, source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 106, in _maybe_compile
    raise err1
  File "/usr/lib/python3.8/codeop.py", line 93, in _maybe_compile
    code1 = compiler(source + "\n", filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 143, in __call__
    codeob = compile(source, filename, symbol, self.flags, 1)
  File "<console>", line 1
    queryset.count()
    ^
IndentationError: unexpected indent
>>> queryset.count()
35
>>> queryset=Student.objects.filter(department__department__startswith="Computer science")
>>> queryset
<QuerySet [<Student: Amy Strong>, <Student: Anna Andrews>, <Student: Ashley Moreno>, <Student: Benjamin Mckinney>, <Student: Carly Brown>, <Student: Casey Hale>, <Student: Crystal Watkins>, <Student: David Spencer>, <Student: Debbie Watson>, <Student: Diana Weaver>, <Student: Dustin Wilson>, <Student: Gabriela Young>, <Student: George Palmer>, <Student: James Lambert>, <Student: Jayendra sharma>, <Student: Joan Cooper>, <Student: Jose Underwood>, <Student: Kathryn Kerr>, <Student: Kristy Hoffman>, <Student: Lauren May>, '...(remaining elements truncated)...']>
>>> queryset.count()
42
>>> queryset=Student.objects.filter(department__department__in=d)
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'd' is not defined
>>> d=['Civil','Electrical']
>>> queryset=Student.objects.filter(department__department__in=d)
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Andre Beck>, <Student: Andrew Good>, <Student: Andrew Simon>, <Student: Anthony Smith>, <Student: Bruce Rodriguez>, <Student: Carol Watkins>, <Student: Christina Wells>, <Student: Christina Williams>, <Student: Christopher James>, <Student: Connie Banks>, <Student: Cory Garrett>, <Student: Dawn Cole>, <Student: Debra Davis>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, <Student: Donald Pitts>, <Student: Gregory Wood>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.filter(department__department__icontains=d)
>>> queryset
<QuerySet []>
>>> d=['Civil','Electrical','Computer science']
>>> d
['Civil', 'Electrical', 'Computer science']
>>> queryset=Student.objects.filter(department__department__icontains=d)
>>> queryset
<QuerySet []>
>>> queryset=Student.objects.filter(department__department__in=d)
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Andre Beck>, <Student: Andrew Good>, <Student: Andrew Simon>, <Student: Anthony Smith>, <Student: Bruce Rodriguez>, <Student: Carol Watkins>, <Student: Christina Wells>, <Student: Christina Williams>, <Student: Christopher James>, <Student: Connie Banks>, <Student: Cory Garrett>, <Student: Dawn Cole>, <Student: Debra Davis>, <Student: Dennis Herring>, <Student: Dennis Perry>, <Student: Diane Carpenter>, <Student: Donald Pitts>, <Student: Gregory Wood>, '...(remaining elements truncated)...']>
>>> queryset.count()
69
>>> queryset=Student.objects.exclude(department__department__in="Civil")
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>, <Student: Benjamin Gonzalez>, <Student: Benjamin Mckinney>, '...(remaining elements truncated)...']>
>>> queryset.count()
191
>>> queryset=Student.objects.filter(student_name="jayendra")
>>> queryset
<QuerySet []>
>>> len(queryset)
0
>>> queryset.exists()
False
>>> queryset=Student.objects.filter(student_name__icontains="jayendra")
>>> queryset
<QuerySet [<Student: Jayendra sharma>]>
>>> queryset.exists()
True
>>> queryset[0:100]
<QuerySet [<Student: Jayendra sharma>]>
>>> queryset=Students.objects.all()
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'Students' is not defined
>>> queryset=students.objects.all()
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'students' is not defined
>>> queryset=Student.objects.all()
>>> queryset[0:100]
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>, <Student: Benjamin Gonzalez>, <Student: Benjamin Mckinney>, '...(remaining elements truncated)...']>
>>> queryset[0:100].student_name
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'QuerySet' object has no attribute 'student_name'
>>> queryset.values()
<QuerySet [{'id': 63, 'department_id': 3, 'student_id_id': 64, 'student_name': 'Aaron Haynes', 'student_email': 'stevenbeard@example.com', 'student_age': 100, 'student_address': '928 Ruiz Mountain\nLake Julietown, LA 54113'}, {'id': 11, 'department_id': 3, 'student_id_id': 12, 'student_name': 'Adrian Wall', 'student_email': 'kristinbrown@example.net', 'student_age': 66, 'student_address': '443 Bautista Ridges\nBrianport, NV 22765'}, {'id': 170, 'department_id': 5, 'student_id_id': 171, 'student_name': 'Albert Lee', 'student_email': 'mbaker@example.org', 'student_age': 80, 'student_address': '872 Johnson Streets Apt. 555\nSouth Angela, DC 52833'}, {'id': 181, 'department_id': 5, 'student_id_id': 182, 'student_name': 'Alicia Campbell', 'student_email': 'fschmidt@example.org', 'student_age': 98, 'student_address': '22307 Watson Crescent Suite 773\nSmithberg, VA 66242'}, {'id': 34, 'department_id': 2, 'student_id_id': 35, 'student_name': 'Amy Strong', 'student_email': 'lmoore@example.net', 'student_age': 55, 'student_address': 'USNV Simmons\nFPO AP 20251'}, {'id': 23, 'department_id': 1, 'student_id_id': 24, 'student_name': 'Andre Beck', 'student_email': 'thomas36@example.com', 'student_age': 63, 'student_address': '80990 Sara Center\nMelissaview, MO 24208'}, {'id': 87, 'department_id': 5, 'student_id_id': 88, 'student_name': 'Andre Mann', 'student_email': 'sarahperez@example.com', 'student_age': 44, 'student_address': '690 Tanya Creek\nMatthewsburgh, NH 80605'}, {'id': 152, 'department_id': 3, 'student_id_id': 153, 'student_name': 'Andrew Good', 'student_email': 'rodriguezjohn@example.com', 'student_age': 93, 'student_address': '6900 Marvin Drive\nGilbertfort, SD 83541'}, {'id': 36, 'department_id': 5, 'student_id_id': 37, 'student_name': 'Andrew Rodriguez', 'student_email': 'michaelwilson@example.com', 'student_age': 80, 'student_address': '63810 Valdez Islands Suite 014\nSouth Andrew, NC 60087'}, {'id': 109, 'department_id': 1, 'student_id_id': 110, 'student_name': 'Andrew Simon', 'student_email': 'kristipatel@example.com', 'student_age': 54, 'student_address': 'Unit 8139 Box 9909\nDPO AP 18511'}, {'id': 31, 'department_id': 4, 'student_id_id': 32, 'student_name': 'Ann Campbell', 'student_email': 'jennifer38@example.com', 'student_age': 92, 'student_address': 'PSC 0163, Box 4182\nAPO AE 75509'}, {'id': 122, 'department_id': 2, 'student_id_id': 123, 'student_name': 'Anna Andrews', 'student_email': 'vharris@example.org', 'student_age': 31, 'student_address': '0904 Amber Plains Apt. 386\nNew Daniellemouth, KS 15559'}, {'id': 178, 'department_id': 5, 'student_id_id': 179, 'student_name': 'Anne Mitchell', 'student_email': 'adam34@example.com', 'student_age': 51, 'student_address': '9694 James Village Suite 171\nSouth Brooke, OR 59785'}, {'id': 98, 'department_id': 1, 'student_id_id': 99, 'student_name': 'Anthony Smith', 'student_email': 'smithtroy@example.net', 'student_age': 28, 'student_address': 'Unit 7933 Box 0994\nDPO AE 08313'}, {'id': 5, 'department_id': 4, 'student_id_id': 6, 'student_name': 'Antonio Guzman', 'student_email': 'desireechandler@example.com', 'student_age': 79, 'student_address': '8311 Cody Trace Apt. 443\nWest Whitneybury, WA 29422'}, {'id': 45, 'department_id': 2, 'student_id_id': 46, 'student_name': 'Ashley Moreno', 'student_email': 'vgarrison@example.org', 'student_age': 88, 'student_address': '620 Mccall Isle\nWest Daniel, ID 44425'}, {'id': 22, 'department_id': 5, 'student_id_id': 23, 'student_name': 'Ashley Randall', 'student_email': 'rbaker@example.net', 'student_age': 94, 'student_address': '62822 Robert Tunnel Suite 187\nWesleyton, AK 86725'}, {'id': 148, 'department_id': 4, 'student_id_id': 149, 'student_name': 'Autumn Burns', 'student_email': 'ithompson@example.net', 'student_age': 100, 'student_address': '9860 Gross Field\nNorth Christopher, IN 72509'}, {'id': 43, 'department_id': 5, 'student_id_id': 44, 'student_name': 'Benjamin Gonzalez', 'student_email': 'amyle@example.org', 'student_age': 95, 'student_address': '0384 Tamara Inlet Suite 452\nLisamouth, NE 86086'}, {'id': 51, 'department_id': 2, 'student_id_id': 52, 'student_name': 'Benjamin Mckinney', 'student_email': 'leslierichardson@example.com', 'student_age': 53, 'student_address': '68355 Anita Bridge\nWest Carmenbury, NV 84213'}, '...(remaining elements truncated)...']>
>>> queryset.values()[0]
{'id': 63, 'department_id': 3, 'student_id_id': 64, 'student_name': 'Aaron Haynes', 'student_email': 'stevenbeard@example.com', 'student_age': 100, 'student_address': '928 Ruiz Mountain\nLake Julietown, LA 54113'}
>>> queryset.values()[0]['student_age']
100
>>> queryset.values()[0]['student_name']
'Aaron Haynes'
>>> queryset.values()[0]['student_email']
'stevenbeard@example.com'
>>> queryset.values()[0]['department']
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
KeyError: 'department'
>>> queryset.values()[0]['department__department']
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
KeyError: 'department__department'
>>> queryset.values()[0]['student_email']
'stevenbeard@example.com'
>>> queryset=student.objects.all().order_by('student_name')
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'student' is not defined
>>> queryset=Student.objects.all().order_by('student_name')
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>, <Student: Benjamin Gonzalez>, <Student: Benjamin Mckinney>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.all().order_by('student_age')
>>> queryset
<QuerySet [<Student: Jayendra sharma>, <Student: Michael Hoffman>, <Student: Jennifer Perkins>, <Student: Robert Melton>, <Student: Stephen Norris>, <Student: Jim Herrera>, <Student: Jennifer Miller>, <Student: David Scott>, <Student: Samuel Alexander>, <Student: Cody Johnston>, <Student: Doris Powell>, <Student: Monica Gonzalez>, <Student: Jessica Davidson>, <Student: Anthony Smith>, <Student: William Young>, <Student: Joshua Wolfe>, <Student: Kathy Peterson>, <Student: Jeffrey Herring>, <Student: Sherry Randolph>, <Student: Susan Gonzalez>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.all().order_by('-student_age')
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Autumn Burns>, <Student: Lori Roberts>, <Student: Robert Chang>, <Student: Lauren May>, <Student: Alicia Campbell>, <Student: Kenneth Cortez>, <Student: Lisa Hopkins>, <Student: Trevor Houston>, <Student: Christina Wells>, <Student: Tina Baird>, <Student: Benjamin Gonzalez>, <Student: Thomas Dixon>, <Student: Jacqueline Olson>, <Student: Ashley Randall>, <Student: Patrick Welch>, <Student: Zachary Fuller>, <Student: Andrew Good>, <Student: Ann Campbell>, <Student: Brenda Reynolds>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.all().distinct('student_name')
>>> queryset
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 374, in __repr__
    data = list(self[: REPR_OUTPUT_SIZE + 1])
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 380, in __len__
    self._fetch_all()
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1881, in _fetch_all
    self._result_cache = list(self._iterable_class(self))
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 91, in __iter__
    results = compiler.execute_sql(
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/compiler.py", line 1549, in execute_sql
    sql, params = self.as_sql()
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/compiler.py", line 785, in as_sql
    distinct_result, distinct_params = self.connection.ops.distinct_sql(
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/backends/base/operations.py", line 202, in distinct_sql
    raise NotSupportedError(
django.db.utils.NotSupportedError: DISTINCT ON fields is not supported by this database backend
>>> queryset=Student.objects.all()
>>> queryset.reverse()
<QuerySet [<Student: Zachary Fuller>, <Student: William Young>, <Student: William Walker>, <Student: William Mcdaniel>, <Student: William Jackson>, <Student: William Hudson>, <Student: William Erickson>, <Student: Wesley Keith>, <Student: Veronica Nelson>, <Student: Trevor Houston>, <Student: Trevor Dunn>, <Student: Todd Lowery>, <Student: Tina Baird>, <Student: Timothy Herrera>, <Student: Timothy Campbell>, <Student: Timothy Barry>, <Student: Thomas Miller>, <Student: Thomas Garza>, <Student: Thomas Dixon>, <Student: Tamara Collins>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.all()
>>> queryset
<QuerySet [<Student: Aaron Haynes>, <Student: Adrian Wall>, <Student: Albert Lee>, <Student: Alicia Campbell>, <Student: Amy Strong>, <Student: Andre Beck>, <Student: Andre Mann>, <Student: Andrew Good>, <Student: Andrew Rodriguez>, <Student: Andrew Simon>, <Student: Ann Campbell>, <Student: Anna Andrews>, <Student: Anne Mitchell>, <Student: Anthony Smith>, <Student: Antonio Guzman>, <Student: Ashley Moreno>, <Student: Ashley Randall>, <Student: Autumn Burns>, <Student: Benjamin Gonzalez>, <Student: Benjamin Mckinney>, '...(remaining elements truncated)...']>
>>> queryset=Student.objects.values_list('id','student_name')
>>> queryset
<QuerySet [(63, 'Aaron Haynes'), (11, 'Adrian Wall'), (170, 'Albert Lee'), (181, 'Alicia Campbell'), (34, 'Amy Strong'), (23, 'Andre Beck'), (87, 'Andre Mann'), (152, 'Andrew Good'), (36, 'Andrew Rodriguez'), (109, 'Andrew Simon'), (31, 'Ann Campbell'), (122, 'Anna Andrews'), (178, 'Anne Mitchell'), (98, 'Anthony Smith'), (5, 'Antonio Guzman'), (45, 'Ashley Moreno'), (22, 'Ashley Randall'), (148, 'Autumn Burns'), (43, 'Benjamin Gonzalez'), (51, 'Benjamin Mckinney'), '...(remaining elements truncated)...']>
>>> queryset=Student.objects.get(id=140)
>>> queryset
<Student: Erica Mcclure>
>>> 
