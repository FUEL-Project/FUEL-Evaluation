FUEL Evaluation
===============

We evaluated 4 different unrestricted file upload (UFU) vulnerability scanners against the 15 file upload scenarios implemented in FUEL.

# Scanners:

- FUSE
- Fuxploider
- BurpSuite Pro + UploadScanner plugin
- ZAP + FileUpload plugin

# Evaluations

Each of the following directories contains a separate README with additional information about the scanner's evaluation.

- `01-fuse`: FUSE
- `02-fuxploider`: Fuxploider 
- `03-zap-img`: ZAP initialized with `fuel.png`
- `04-burp-img`: BurpSuite initialized with `fuel.png`
- `05-fuxploider-ng`: Fuxploider-NG (our improved version)
- `06-zap-txt`: ZAP initialized with `fuel.txt`
- `07-burp-txt`: BurpSuite initialized with `fuel.txt`

# Software:

- Docker: 24.0.7
- Docker-compose: 2.24.4
- FUSE: Commit 7dd3a8e
- Fuxploider: Commit ec8742b
- ZAP: 2.14.0
- FileUpload plugin: 1.2.1
- BurpSuite Professional: 2024.1.1
- UploadScanner plugin: 1.0.8a

# Notice for reviewers

This README and parts of the repository will be extended with more documentation upon the acceptance of the paper. The brevity is for anonymity reasons.