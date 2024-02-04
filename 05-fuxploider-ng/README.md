Fuxploider-NG Eval
==================

# Setup
First, bring up FUEL.

```
sudo docker build --tag 'fuxploider-ng' . 
sudo docker run -it --network=fuel_fuel_network --name fuxploider-ng fuxploider-ng bash
```

# Execution with:

```
export SCENARIO=1 && timeout 300s echo 'Y' | python3 fuxploider.py -u "http://172.22.1.${SCENARIO}/" --true-regex 'See the' --uploads-path 'uploads' -s -y -l png,gif 2>&1 | tee results/172.22.1.${SCENARIO}.txt
```


# Scenario 1
iFUB:1
CE:  1
XSS: 1

# Scenario 2
iFUB:1
CE:  1
XSS: 1

# Scenario 3
iFUB:1
CE:  1
XSS: 1

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
iFUB:1
CE:  1
XSS: 1

# Scenario 8
iFUB:1
CE:  1
XSS: 1

# Scenario 9
iFUB:1
CE:  1
XSS: 1

# Scenario 10
iFUB:1
CE:  1
XSS: 1

# Scenario 11
iFUB:1
CE:  1
XSS: 1

# Scenario 12
iFUB:1
CE:  1
XSS: 1

# Scenario 13
iFUB:1
CE:  -
XSS: 1

# Scenario 14
iFUB:1
CE:  1
XSS: 1

# Scenario 15
iFUB:0
CE:  0
XSS: 0
