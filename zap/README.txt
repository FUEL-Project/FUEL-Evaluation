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
- Switch all threshold off to deactivate all other scanning checks.
- Go to Miscellaneous and set FileUpload's Threshold and Strength to 'medium'.

# Scenario 1
FU: 1
CE: 1
XSS:1

# Scenario 2
FU: 1
CE: 1
XSS:1

# Scenario 3
FU: 0
CE: 0
XSS:0

# Scenario 4
FU: 1
CE: 1
XSS:1

# Scenario 5
FU: 1
CE: 1
XSS:1

# Scenario 6
FU: 1
CE: 1
XSS:1

# Scenario 7
FU: 1 
CE: 1 (.htaccess)
XSS:1

# Scenario 8
FU: 1
CE: 0
XSS:1

# Scenario 9
FU: 1
CE: 1
XSS:0

# Scenario 10
FU: 0
CE: 0
XSS:0

# Scenario 11
FU: 1
CE: 0
XSS:1

# Scenario 12
FU: 0
CE: 0
XSS:0

# Scenario 13
FU: 0
CE: 0
XSS:0

# Scenario 14
FU: 0
CE: 0
XSS:0

# Scenario 15
FU: 0
CE: 0
XSS:0