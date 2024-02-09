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
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 2
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 3
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 4
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 5
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 6
- iFUB:0
- CE:  0
- XSS: 1

# Scenario 7
- iFUB:1
- CE:  0
- XSS: 1

# Scenario 8
- iFUB:0
- CE:  0
- XSS: 1

# Scenario 9
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 10
- iFUB:1
- CE:  1
- XSS: 1

# Scenario 11
- iFUB:0
- CE:  0
- XSS: 1

# Scenario 12
- iFUB:0
- CE:  0
- XSS: 0

# Scenario 13
- iFUB:0
- CE:  -
- XSS: 0

# Scenario 14
- iFUB:Timeout
- CE:  Timeout
- XSS: Timeout

# Scenario 15
- iFUB:0
- CE:  0
- XSS: 0