Fuxploider Eval
==================

# Setup
First, bring up FUEL.

```
python3 -m venv venv
. venv/bin/activate
pip3 install -r requirements.txt
```

# Change PHP info regex
- `templates.json`
- Replace `"\\<title\\>phpinfo\\(\\)\\<\\/title\\>(.|\n)*\\<h2\\>PHP License\\<\\/h2\\>"` with `"\\<title\\>\\s*(PHP\\s*[0-9\\.]+)*\\s*-*\\s*phpinfo\\(\\)<\\/title\\>(.|\n)*\\<h2\\>PHP License\\<\\/h2\\>"`

# Execution with:

```
timeout 300s python3 fuxploider.py -u 'http://localhost:10001/' --true-regex 'See the' --uploads-path '/uploads/'
```

# Scenario 1

FU: 1
CE: 1
XSS: 0
```
2024-02-03 11:02:41 INFO - Code execution obtained ('.php','image/jpeg','phpinfo','http://localhost:10001//uploads//tmpr193crvg.php')
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 INFO - Upload of 'tmpfc7hgvh2.Php%00.jpe' with mime type image/jpeg successful
2024-02-03 11:02:41 INFO - Upload of 'tmpj48xjr6f.PhP%00.jpe' with mime type image/jpeg successful
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 INFO - Upload of 'tmpfy0m6_73.pHp1%00.jpe' with mime type image/jpeg successful
2024-02-03 11:02:41 INFO - Upload of 'tmpevbql1c_.pHp%00.jpe' with mime type image/jpeg successful
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:02:41 INFO - Upload of 'tmpz0h03g_a.pHP2%00.jpe' with mime type image/jpeg successful
2024-02-03 11:02:41 INFO - 1 entry point(s) found using 318 HTTP requests.

Found the following entry points: 
[{'suffix': '.php', 'mime': 'image/jpeg', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 2

FU: 1
CE: 1
XSS: 0
```
2024-02-03 11:11:54 INFO - Code execution obtained ('.php','image/jpeg','phpinfo','http://localhost:10002//uploads//tmpeqqa6pgz.php')
2024-02-03 11:11:54 INFO - Upload of 'tmpicjijw0k.pht%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:11:54 INFO - Upload of 'tmpui2ep_wy.PhP%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:11:54 INFO - Upload of 'tmps35iuxnh.Php%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:11:54 INFO - Upload of 'tmp3edpx5fm.phtml%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:11:55 INFO - 1 entry point(s) found using 306 HTTP requests.

Found the following entry points: 
[{'suffix': '.php', 'mime': 'image/jpeg', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 3

FU: 1
CE: 1
XSS: 0
```
Start uploading payloads? [Y/n]: 2024-02-03 11:12:20 INFO - ### Starting code execution detection (messing with file extensions and mime types...)
2024-02-03 11:12:21 INFO - Upload of 'tmpal1cuzbl.php' with mime type image/jpeg successful
2024-02-03 11:12:21 INFO - Upload of 'tmpp8b3z4ft.php1' with mime type image/jpeg successful
2024-02-03 11:12:21 INFO - Upload of 'tmp89yupvk2.php2' with mime type image/jpeg successful
2024-02-03 11:12:21 INFO - Upload of 'tmpr2ot4vv8.php3' with mime type image/jpeg successful
2024-02-03 11:12:21 INFO - Code execution obtained ('.php','image/jpeg','phpinfo','http://localhost:10003//uploads//tmpal1cuzbl.php')
2024-02-03 11:12:21 INFO - 1 entry point(s) found using 125 HTTP requests.

Found the following entry points: 
[{'suffix': '.php', 'mime': 'image/jpeg', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 4

FU: 1
CE: 1
XSS: 0
```
2024-02-03 11:39:56 INFO - Code execution obtained ('.php','image/jpeg','phpinfo','http://localhost:10004//uploads//tmpkorwdtk3.php')
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 INFO - Upload of 'tmpxgr4l_xm.PhP%00.jpe' with mime type image/jpeg successful
2024-02-03 11:39:56 INFO - Upload of 'tmpc38uewlv.Php%00.jpe' with mime type image/jpeg successful
2024-02-03 11:39:56 INFO - Upload of 'tmpocsm8qw6.phtml%00.jpe' with mime type image/jpeg successful
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 INFO - Upload of 'tmprwgsreod.pht%00.jpe' with mime type image/jpeg successful
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:56 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:39:57 INFO - 1 entry point(s) found using 307 HTTP requests.

Found the following entry points: 
[{'suffix': '.php', 'mime': 'image/jpeg', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 5

FU: 1
CE: 1
XSS: 0
```
2024-02-03 11:42:04 INFO - Code execution obtained ('.jpeg.PhP','image/jpeg','phpinfo','http://localhost:10005//uploads//tmp3z2ebs8s.jpeg.PhP')
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 INFO - Upload of 'tmp_5nd3g80.pht%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 INFO - Upload of 'tmpnfk4q3l1.phtml%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 INFO - Upload of 'tmpe756hv4p.Php%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 INFO - Upload of 'tmpyxdj8gj6.PhP%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 INFO - Upload of 'tmpw2aayp0z.pHp1%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:04 INFO - Upload of 'tmpd0f7yirx.pHp%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:04 INFO - 1 entry point(s) found using 308 HTTP requests.

Found the following entry points: 
[{'suffix': '.jpeg.PhP', 'mime': 'image/jpeg', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 6

FU: 1
CE: 1
XSS: 0
```
2024-02-03 11:42:25 INFO - Code execution obtained ('.pHp.jpeg','application/x-httpd-php','phpinfo','http://localhost:10006//uploads//tmpinuips5f.pHp.jpeg')
2024-02-03 11:42:25 INFO - Upload of 'tmpapcxr59_.php%00.jpeg' with mime type application/x-httpd-php successful
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 INFO - Upload of 'tmp5poe2rrc.pHP2%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:25 INFO - Upload of 'tmptpo4bf5k.PHp5%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:25 INFO - Upload of 'tmp_b7wgzmw.pHtMl%00.jpeg' with mime type image/jpeg successful
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 WARNING - Code exec detection returned an http code of 404.
2024-02-03 11:42:25 INFO - Upload of 'tmpee2gznqt.php1%00.jpeg' with mime type application/x-httpd-php successful
2024-02-03 11:42:25 INFO - Upload of 'tmpqlt4xhgj.php2%00.jpeg' with mime type application/x-httpd-php successful
2024-02-03 11:42:25 INFO - 1 entry point(s) found using 315 HTTP requests.

Found the following entry points: 
[{'suffix': '.pHp.jpeg', 'mime': 'application/x-httpd-php', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 7
FU: 1
CE: 1 (.htaccess)
XSS: 0

```
2024-02-03 11:46:31 INFO - Upload of '.htaccess' with mime type image/jpeg successful
2024-02-03 11:46:31 INFO - Upload of '.htaccess' with mime type image/x-ms-bmp successful
2024-02-03 11:46:31 INFO - Upload of '.htaccess' with mime type image/jpeg successful
2024-02-03 11:46:31 INFO - Upload of '.htaccess' with mime type image/jpeg successful
2024-02-03 11:46:31 INFO - Code execution obtained ('htaccess','image/jpeg','htaccess','http://localhost:10007//uploads//.htaccess')
2024-02-03 11:46:31 INFO - 1 entry point(s) found using 105906 HTTP requests.

Found the following entry points: 
[{'suffix': 'htaccess', 'mime': 'image/jpeg', 'templateName': 'htaccess', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': '.htaccess', 'staticFilename': 'True'}]
```

# Scenario 8
FU: 0
CE: 0
XSS: 0

```
2024-02-03 11:51:33 INFO - 0 entry point(s) found using 115601 HTTP requests.

Found the following entry points: 
[]
```

# Scenario 9
FU: 0
CE: 0
XSS: 0

```
[*] starting at 11:52:55
2024-02-03 11:52:55 INFO - ### Starting detection of valid extensions ...
2024-02-03 11:52:55 INFO - ### Tried 100 extensions,  0 are valid.
2024-02-03 11:52:55 ERROR - No valid extension found.
```

With `-s -l gif`:

```
Start uploading payloads? [Y/n]: 2024-02-03 11:53:28 INFO - ### Starting code execution detection (messing with file extensions and mime types...)
2024-02-03 11:53:29 INFO - Upload of 'tmpk56m4uwp.php' with mime type application/x-httpd-php successful
2024-02-03 11:53:29 INFO - Upload of 'tmp2u7fsos5.php1' with mime type application/x-httpd-php successful
2024-02-03 11:53:29 INFO - Upload of 'tmp490p0psx.php3' with mime type application/x-httpd-php successful
2024-02-03 11:53:29 INFO - Upload of 'tmpu5ldhzef.php2' with mime type application/x-httpd-php successful
2024-02-03 11:53:29 INFO - Code execution obtained ('.php','application/x-httpd-php','nastygif','http://localhost:10009//uploads//tmpk56m4uwp.php')
2024-02-03 11:53:29 INFO - 1 entry point(s) found using 157 HTTP requests.

Found the following entry points: 
[{'suffix': '.php', 'mime': 'application/x-httpd-php', 'templateName': 'nastygif', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.gif', 'staticFilename': None}]
```

# Scenario 10
FU: 0
CE: 0
XSS: 0


```
[*] starting at 11:54:43
2024-02-03 11:54:43 INFO - ### Starting detection of valid extensions ...
2024-02-03 11:54:43 INFO - ### Tried 100 extensions,  0 are valid.
2024-02-03 11:54:43 ERROR - No valid extension found.
```

With `-s -l png`

```
[*] starting at 11:55:16
2024-02-03 11:55:16 INFO - ### Skipping detection of valid extensions,  using provided extensions instead (['png']).
Extensions detection: 0:00:00.000241
Start uploading payloads? [Y/n]: 2024-02-03 11:55:16 INFO - ### Starting code execution detection (messing with file extensions and mime types...)
2024-02-03 11:55:17 INFO - 0 entry point(s) found using 483 HTTP requests.

Found the following entry points: 
[]
```

# Scenario 11
FU: 0
CE: 0
XSS: 0

```
2024-02-03 11:57:51 INFO - 0 entry point(s) found using 77201 HTTP requests.

Found the following entry points: 
[]
```

# Scenario 12
FU: FP
CE: 0
XSS: 0

```
2024-02-03 12:01:09 INFO - Code execution obtained ('.jsp%00.jpg','image/jpeg','basicjsp','http://localhost:10012//uploads//tmpmysdvb2a.jsp')
2024-02-03 12:01:09 INFO - 1 entry point(s) found using 1570 HTTP requests.

Found the following entry points: 
[{'suffix': '.jsp%00.jpg', 'mime': 'image/jpeg', 'templateName': 'basicjsp', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.jsp', 'staticFilename': None}]
```

# Scenario 13
FU: 0
CE: 0
XSS: 0

```
[*] starting at 12:04:41
2024-02-03 12:04:41 CRITICAL - No HTML forms found.
```

# Scenario 14
FU: 0
CE: 0
XSS: 0

```
2024-02-03 12:05:03 INFO - Code execution obtained ('.php%00.png','image/png','phpinfo','http://localhost:10014//uploads//tmp1bjguazx.php')
2024-02-03 12:05:03 INFO - 1 entry point(s) found using 231 HTTP requests.

Found the following entry points: 
[{'suffix': '.php%00.png', 'mime': 'image/png', 'templateName': 'phpinfo', 'codeExecURL': None, 'dynamicPayload': None, 'payloadFilename': 'template.php', 'staticFilename': None}]
```

# Scenario 15
FU: 0
CE: 0
XSS: 0

```
[*] starting at 12:05:36
2024-02-03 12:05:36 INFO - ### Starting detection of valid extensions ...
2024-02-03 12:05:36 INFO - ### Tried 100 extensions,  0 are valid.
2024-02-03 12:05:36 ERROR - No valid extension found.
```
