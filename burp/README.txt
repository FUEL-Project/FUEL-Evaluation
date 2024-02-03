Burp UploadScanner
==================

# Setup

```
Start Burp
Install Jython
Install UploadScanner extension
```

- Capture a file upload request to the level.
- Right-click -> Send to Extension -> UploadScanner -> New
- Set the following options:

<See uploadscanner-options.png>

- Click "Send Redownloader Request"
- Then click "Scan with Redownloader"
- Wait for the scan to finish

# Scenario 1
FU: 1
CE: 1
XSS:1

See results/scenario1.png

# Scenario 2
FU: 1
CE: 1
XSS: 1

See results/scenario2.png

# Scenario 3
FU: 1 
CE: 1
XSS:0

See results/scenario3.png


# Scenario 4
FU: 1
CE: 1 
XSS:1

See results/scenario4.png


# Scenario 5
FU: 1
CE: 0
XSS:1

See results/scenario5.png


# Scenario 6
FU: 1
CE: 1
XSS:1

See results/scenario6.png


# Scenario 7
FU: 1
CE: 0
XSS:1

See results/scenario7.png


# Scenario 8
FU: 1
CE: 0
XSS:1

See results/scenario8.png

# Scenario 9
FU: 1
CE: 1
XSS:1

See results/scenario9.png


# Scenario 10
FU: 1
CE: 1
XSS:1

See results/scenario10.png


# Scenario 11
FU: 1
CE: 0
XSS:1

See results/scenario11.png


# Scenario 12
FU: 0
CE: 0
XSS:0

TIMEOUT

See results/scenario12.png


# Scenario 13
FU: 0
CE: 0
XSS:0

See results/scenario13.png


# Scenario 14
FU: 1
CE: 1
XSS:0

See results/scenario14.png


# Scenario 15
FU: 1
CE: 0
XSS: 1

See results/scenario15.png
