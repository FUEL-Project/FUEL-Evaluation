FUSE Eval
====================

# Setup
First, bring up FUEL.

```
sudo docker build --tag 'fuse' . 
sudo docker run -it --network=fuel_fuel_network --name fuse fuse bash
```

Create configs for each scenario within the FUEL network, i.e. `scenario1.conf`:

```
[USER_CREDENTIAL]
WebRootPath = /var/www/html/
WebHost = http://172.22.1.1/
WebUploadURL = http://172.22.1.1/
WebUploadPageURL = http://172.22.1.1/
WebUploadSuccessStr = See the
WebUploadAdditionalValue =fileToUpload=%filebinary#
WebUploadedFileUrlPattern = http://172.22.1.1/uploads/%filename#
ID =
PW =
WebLoginIDName =
WebLoginPWName =
WebLoginURL =
WebLoginPageURL =
WebLoginCSRFName =
WebLoginAdditionalValue =
WebLoginSuccessStr =
WebUploadFormAttr =
WebUploadCustomHeader =
WebUploadCSRFName =
WebUploadFilesURL =
WebUploadFilesParameter =

[DETECTOR_CONF]
MutationChainLimit = 99
MonitorEnable = False
MonitorHost =
MonitorPort =
``` 

Adjust the internal IP address for each scenario.

# Execution with:

```
timeout 300s python2 framework.py scenario1.conf 
```

To copy the files from the container use:

```
sudo docker cp 'fuse:/fuse/scenario1.conf' ./configs/
sudo docker cp 'fuse:/fuse/172.22.1.1_report.txt' ./results/
```


# Scenario 1
FU: 1
CE: 1
XSS: 1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  69762b3eea7761ff460edfb85ab353d1_SEED.html
   -> http://172.22.1.1/uploads/69762b3eea7761ff460edfb85ab353d1_SEED.html

[+] Found Code Executable Uploaded Files( php ) - 1 files
  Seed(seed/seed.php)   :  6755c4e84291098173fecc75c0123ff1_SEED.php
   -> http://172.22.1.1/uploads/6755c4e84291098173fecc75c0123ff1_SEED.php

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 2
FU: 1
CE: 1
XSS: 1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  59c4a5a858001feff01d962bfd95cc31_SEED.html
   -> http://172.22.1.2/uploads/59c4a5a858001feff01d962bfd95cc31_SEED.html

[+] Found Code Executable Uploaded Files( php ) - 1 files
  Seed(seed/seed.php)   :  213c8adc02e1dd17a39036ef56556b50_SEED.php
   -> http://172.22.1.2/uploads/213c8adc02e1dd17a39036ef56556b50_SEED.php

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 3
FU: 1 
CE: 1 
XSS: 1 

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  M03_JPG:  e62d59f811082d70ce532b0962bcfdf7_M3JPG.html
   -> http://172.22.1.3/uploads/e62d59f811082d70ce532b0962bcfdf7_M3JPG.html

[+] Found Code Executable Uploaded Files( php ) - 1 files
  Seed(seed/seed.php)   M03_JPG:  cb237ce2aef845975b861d533c84bbc0_M3JPG.php
   -> http://172.22.1.3/uploads/cb237ce2aef845975b861d533c84bbc0_M3JPG.php
```

# Scenario 4
FU: 1 
CE: 1 
XSS:1 

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  4cfa2919b7c6ba74d8a83f90fb7e5f1e_SEED.html
   -> http://172.22.1.4/uploads/4cfa2919b7c6ba74d8a83f90fb7e5f1e_SEED.html

[+] Found Code Executable Uploaded Files( php ) - 1 files
  Seed(seed/seed.php)   :  f6ff364e84229b4023110be3334765b6_SEED.php
   -> http://172.22.1.4/uploads/f6ff364e84229b4023110be3334765b6_SEED.php

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 5
FU: 1
CE: 1
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  50e2a2918fd13f0f95bf5fbf02fe152b_SEED.html
   -> http://172.22.1.5/uploads/50e2a2918fd13f0f95bf5fbf02fe152b_SEED.html

[+] Found Code Executable Uploaded Files( php ) - 1 files
  Seed(seed/seed.php)   M11:  33225a12f8ee2456b45b4bcc32d4ee88_M11.PhP
   -> http://172.22.1.5/uploads/33225a12f8ee2456b45b4bcc32d4ee88_M11.PhP

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 6
FU: 1
CE: 0
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  7ac5971b6c790f8b70869e62b4cdc2d7_SEED.html
   -> http://172.22.1.6/uploads/7ac5971b6c790f8b70869e62b4cdc2d7_SEED.html

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 7
FU: 1
CE: 1 (.htaccess)
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  ebfd7204e2359cfa0b71f80b4e825720_SEED.html
   -> http://172.22.1.7/uploads/ebfd7204e2359cfa0b71f80b4e825720_SEED.html

[+] S1 - .htaccess upload success & It works. (Vulnerable!)
```

# Scenario 8
FU: 1
CE: 0
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  1462c6af623acd99125d8b0e67c7eda3_SEED.html
   -> http://172.22.1.8/uploads/1462c6af623acd99125d8b0e67c7eda3_SEED.html
```
# Scenario 9
FU: 1
CE: 1
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 2 files
  Seed(seed/seed.html)  M01_GIF:  de4b780820d98f216f8292abf581ea29_M1GIF.html
   -> http://172.22.1.9/uploads/de4b780820d98f216f8292abf581ea29_M1GIF.html
  Seed(seed/seed.html)  M02_GIF:  fe9c81eac5063a12de9d27c9d10ecae3_M2GIF.html
   -> http://172.22.1.9/uploads/fe9c81eac5063a12de9d27c9d10ecae3_M2GIF.html

[+] Found Code Executable Uploaded Files( php ) - 2 files
  Seed(seed/seed.php)   M01_GIF:  932b9224a2203d9ffaba1cd1c8180715_M1GIF.php
   -> http://172.22.1.9/uploads/932b9224a2203d9ffaba1cd1c8180715_M1GIF.php
  Seed(seed/seed.php)   M02_GIF:  7cc86d5a03229c3fc452d110e9e2c719_M2GIF.php
   -> http://172.22.1.9/uploads/7cc86d5a03229c3fc452d110e9e2c719_M2GIF.php
```

# Scenario 10
FU: 1
CE: 1
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 2 files
  Seed(seed/seed.html)  M02_PNG:  d95c4d4493811c697ddaa5209a6c5c9b_M2PNG.html
   -> http://172.22.1.10/uploads/d95c4d4493811c697ddaa5209a6c5c9b_M2PNG.html
  Seed(seed/seed.html)  M01_PNG:  925ed8e5096a49f7a49cd27f19b7778a_M1PNG.html
   -> http://172.22.1.10/uploads/925ed8e5096a49f7a49cd27f19b7778a_M1PNG.html

[+] Found Code Executable Uploaded Files( php ) - 2 files
  Seed(seed/seed.php)   M01_PNG:  4fc8bfe27293d3c38cf06173bc5b6c0a_M1PNG.php
   -> http://172.22.1.10/uploads/4fc8bfe27293d3c38cf06173bc5b6c0a_M1PNG.php
  Seed(seed/seed.php)   M02_PNG:  1b8fd6a0a619d7892288ae1422a6e3f9_M2PNG.php
   -> http://172.22.1.10/uploads/1b8fd6a0a619d7892288ae1422a6e3f9_M2PNG.php
```

# Scenario 11
FU: 1 
CE: 0
XSS:1

```
[+] Found Code Executable Uploaded Files( html ) - 1 files
  Seed(seed/seed.html)  :  c7ce06685b0e3d3575b1a6fdd1b26166_SEED.html
   -> http://172.22.1.11/uploads/c7ce06685b0e3d3575b1a6fdd1b26166_SEED.html
```

# Scenario 12
FU: Timeout
CE: Timeout
XSS: Timeout

```
Success = [php] - M04_JPG
Success = [php] - M04_PNG
```
# Scenario 13
FU: 0
CE: 0
XSS:0

```
[+] Tried to Upload File : 127160
[+] Uploaded Files having CE/PCE ability : 0


[-] S1 - .htaccess upload fail or It doesn't work (Secure!)

[-] S1+M3 - .htaccess upload fail or It doesn't work (Secure!)
```

# Scenario 14
FU: 0
CE: 0
XSS: 0

```
[+] Uploaded Files having CE/PCE ability : 0
```

# Scenario 15
FU: 0
CE: 0
XSS:0

```
[+] Uploaded Files having CE/PCE ability : 0
```