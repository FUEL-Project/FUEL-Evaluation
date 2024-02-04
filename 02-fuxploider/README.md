Fuxploider Eval
==================

# Setup
First, bring up FUEL.

```
sudo docker build --tag 'fuxploider' . 
sudo docker run -it --network=fuel_fuel_network --name fuxploider fuxploider bash
```

# Change PHP info regex
Since the PHPinfo page has changed in version 8, the regular expression in ` templates.json` needs to be adjusted.
This is done automatically if the Dockerfile is used, otherwise replace `"\\<title\\>phpinfo\\(\\)\\<\\/title\\>(.|\n)*\\<h2\\>PHP License\\<\\/h2\\>"` with `"\\<title\\>\\s*(PHP\\s*[0-9\\.]+)*\\s*-*\\s*phpinfo\\(\\)<\\/title\\>(.|\n)*\\<h2\\>PHP License\\<\\/h2\\>"`

# Execution with:

```
export SCENARIO=1 && timeout 300s echo 'Y' | python3 fuxploider.py -u "http://172.22.1.${SCENARIO}/" --true-regex 'See the' --uploads-path 'uploads' 2>&1 | tee results/172.22.1.${SCENARIO}.txt
```




# Scenario 1
iFUB:1
CE:  1
XSS: -

# Scenario 2
iFUB:1
CE:  1
XSS: -

# Scenario 3
iFUB:1
CE:  1
XSS: -

# Scenario 4
iFUB:1
CE:  1
XSS: -

# Scenario 5
iFUB:1
CE:  1
XSS: -

# Scenario 6
iFUB:1
CE:  1
XSS: -

# Scenario 7
iFUB:1
CE:  1
XSS: -

# Scenario 8
iFUB:0
CE:  0
XSS: -

# Scenario 9
iFUB:0
CE:  0
XSS: -

# Scenario 10
iFUB:0
CE:  0
XSS: -

# Scenario 11
iFUB:0
CE:  0
XSS: -

# Scenario 12
iFUB:1
CE:  1
XSS: -

# Scenario 13
iFUB:0
CE:  -
XSS: -

# Scenario 14
iFUB:T
CE:  T
XSS: T

# Scenario 15
iFUB:0
CE:  0
XSS: -
