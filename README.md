# Semantic Image Synthesis of Photorealistic Landscape

My implementation of Photorealistic landscape drawings using the Nvidia SPADE model. 

## Installation
1) Install requirements.
```bash
pip install -r requirements
```
2) Download pretrained checkpoints from [here](https://drive.google.com/drive/folders/1-4XLgT6yda7tODN2zOebZ-VS2XzdH9O4?usp=sharing) and extract them in pretrained folder.

3) Set FLASK_APP enviroment variable, and run flask.
- Unix Bash:
    ```bash
    export FLASK_APP='flask/app.py'
    flask run
    ```
- Windows CMD:
    ```bat
    set FLASK_APP='flask/app.py'
    flask run
    ```
- Windows PowerShell:
    ```powershell
    $env:FLASK_APP='flask/app.py'
    flask run
    ```
## Directory Structure
```cmd
SISPL
│   .gitignore
│   build.sh
│   Dockerfile
│   README.md
│   requirements.txt
│
├───flask
│   │   app.py
│   │   test.py
│   │
│   ├───spade
│   │       dataset.py
│   │       generator.py
│   │       model.py
│   │       normalizer.py
│   │
│   ├───static
│   │       index.html
│   │
│   └───sync_batchnorm
│           batchnorm.py
│           batchnorm_reimpl.py
│           comm.py
│           replicate.py
│           unittest.py
│           __init__.py
│
├───images
│       sc1.png
│       sc2.png
│
└───pretrained
        classes_list.txt
        iter.txt
        latest_net_D.pth
        latest_net_G.pth
        loss_log.txt
        opt.pkl
        opt.txt
        README.md

```
## Results

![screenshot_1](images/sc1.png)

![screenshot_2](images/sc2.png)
## Acknowledgement 
Semantic Image Synthesis with Spatially-Adaptive Normalization. Taesung Park, Ming-Yu Liu, Ting-Chun Wang, and Jun-Yan Zhu.
In CVPR 2019 (Oral). [Paper](https://arxiv.org/pdf/1903.07291.pdf) 


Also, Thank Jiayuan Mao for his Synchronized Batch Normalization code. [Repository Link](https://github.com/vacancy/Synchronized-BatchNorm-PyTorch)