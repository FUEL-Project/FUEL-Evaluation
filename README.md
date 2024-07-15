FUEL Evaluation
===============

This repository contains the documentation and results of the evaluation conducted for the paper `Bringing UFUs Back into the Air With FUEL: A Framework for Evaluating the Effectiveness of Unrestricted File Upload Vulnerability Scanners` to be published at [DIMVA 2024](https://www.dimva.org/dimva2024/). 

FUEL is an abbreviation for File-Upload Exploitation Lab, which aims to model different file upload scenarios that can occur in web applications. FUEL can be found in [this repository](https://github.com/FUEL-Project/FUEL-FileUploadExploitationLab).

We evaluated four different state-of-the-art unrestricted file upload (UFU) vulnerability scanners against the 15 file upload scenarios implemented in FUEL.

# UFU Scanners:

- [FUSE](https://github.com/WSP-LAB/FUSE)
- [Fuxploider](https://github.com/almandin/fuxploider)
- [BurpSuite Pro + UploadScanner plugin](https://github.com/PortSwigger/upload-scanner)
- [ZAP + FileUpload plugin](https://github.com/SasanLabs/owasp-zap-fileupload-addon)

# Evaluations

Each of the following directories contains a separate README with additional information about the scanner's evaluation.

- `01-fuse`: FUSE
- `02-fuxploider`: Fuxploider 
- `03-zap-img`: ZAP initialized with `fuel.png`
- `04-burp-img`: BurpSuite initialized with `fuel.png`
- `05-fuxploider-ng`: Fuxploider-NG (our improved version)
- `06-zap-txt`: ZAP initialized with `fuel.txt`
- `07-burp-txt`: BurpSuite initialized with `fuel.txt`

Each folder contains a `README.md` with the exact command used to run the tool against FUEL. Further, the subfolder `results/` contains the tool's output for each scenario.

# Software:

- Docker: 24.0.7
- Docker-compose: 2.24.4
- FUSE: Commit 7dd3a8e
- Fuxploider: Commit ec8742b
- ZAP: 2.14.0
- FileUpload plugin: 1.2.1
- BurpSuite Professional: 2024.1.1
- UploadScanner plugin: 1.0.8a

# Paper & Authors

This file upload exploitation lab was developed for the academic publication by Sebastian Neef and Maath Oudeh.

If you use the the lab, please cite it as follows:

```
@InProceedings{10.1007/978-3-031-64171-8_11,
author="Neef, Sebastian
and Oudeh, Maath",
editor="Maggi, Federico
and Egele, Manuel
and Payer, Mathias
and Carminati, Michele",
title="Bringing UFUs Back into the Air with FUEL: A Framework for Evaluating the Effectiveness of Unrestricted File Upload Vulnerability Scanners",
booktitle="Detection of Intrusions and Malware, and Vulnerability Assessment",
year="2024",
publisher="Springer Nature Switzerland",
address="Cham",
pages="207--226",
isbn="978-3-031-64171-8"
}
```

You can find a preprint of the paper [here](https://arxiv.org/abs/2405.16619) and the camera-ready version [here](https://doi.org/10.1007/978-3-031-64171-8_11).
