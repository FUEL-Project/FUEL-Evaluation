ZAP FileUpload
==============

# Setup

- Install ZAProxy
- Click the "Manage Addons" Icon
- Switch to Tab "Marketplace" and search for  "FileUpload"
- Install the FileUpload plugin and activate it

To configure the FileUpload addon, go to Settings -> File Upload and enter the following:

- Start Identifier: <a href='
- End Identifier: '>See the
- Check: Keep exploiting after discovery

See `zap-config.png`

# Execution

- Click the `Manual Explore` button and enter the URL of the first scenario `http://localhost:10001/` and click `Launch browser`. (See zap-explore.png)
- Upload a sample file to scenario 1. 
- Right-click on the POST request in the navigation and choose -> Attack -> Active Scan (See zap-select-request.png)

- Click 'Show advanced options'
- Go to Miscellaneous and set FileUpload's Threshold and Strength to 'insane'. (see zap-fileupload-insane.png)

To reuse the session state, first run `gunzip fuel-eval.session.data.gz`.

# Scenario 1
iFUB:1
CE:  1
XSS: 1

# Scenario 2
iFUB:1
CE:  1
XSS: 1

# Scenario 3
iFUB:0
CE:  0
XSS: 0

# Scenario 4
iFUB:1
CE:  1
XSS: 1

# Scenario 5
iFUB:1
CE:  1
XSS: 1

# Scenario 6
iFUB:1
CE:  1
XSS: 1

# Scenario 7
iFUB:0
CE:  0
XSS: 1

# Scenario 8
iFUB:0
CE:  0
XSS: 1

# Scenario 9
iFUB:1
CE:  1
XSS: 0

# Scenario 10
iFUB:0
CE:  0
XSS: 0

# Scenario 11
iFUB:0
CE:  0
XSS: 1

# Scenario 12
iFUB:0
CE:  0
XSS: 0

# Scenario 13
iFUB:1
CE:  -
XSS: 1

# Scenario 14
iFUB:T
CE:  T
XSS: T

# Scenario 15
iFUB:0
CE:  0
XSS: 0
