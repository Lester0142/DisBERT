# DisBERT: Discrepancy Modeling with Transformers for Metaphor Detection

This repository contains the Python script for training a metaphor identification model that leverages BERT. The model is trained using dataset in `.tsv` format, containing sentences with corresponding labels for word-level metaphor identification. The performance is evaluated using F1-score, Precision, and Recall metrics.

## Prerequisites

Before running the script, ensure that you have Python 3.7.6 and Nvidia CUDA installed on your machine.

Python 3.7.6: https://www.python.org/downloads/release/python-376/ \
CUDA: https://developer.nvidia.com/cuda-downloads

Also these are some dependencies required for Ubuntu System to pip install pillow:
#### Debian-based systems
```
sudo apt-get update
sudo apt-get install libtiff4-dev libjpeg8-dev zlib1g-dev libfreetype6-dev liblcms2-dev libwebp-dev tcl8.5-dev tk8.5-dev python-tk
```

To ensure the appropriate requirements are successfully installed. Run the following in your terminal. The terminal respond should be similar as shown in the block below.
```
python -V
>>> Python 3.7.6

nvcc --version
>>> nvcc: NVIDIA (R) Cuda compiler driver
>>> ...
```


## Run the Script

#### 1. Clone the repository locally
```
git clone git@github.com:Lester0142/DisBERT.git
```

#### 2. Set up and activate Environment
```
cd DisBERT

python -m venv venv

linux:
    source venv/bin/activate
windows:
    .\venv\Scripts\activate
```

#### 3. Install required depencies and packages
```
pip install -r requirements.txt
```

#### 4. Amend the config file as required
```
config file can be found in src/config/model_config.cfg
```

#### 5. Run the script
```
python ./src/main.py
```

## Acknowledgements
This project makes use of the dataset provided by [MelBERT](https://github.com/jin530/MelBERT).  
Please refer to their paper and repository for more details:
- [Choi, M., Lee, S., Choi, E., Park, H., Lee, J., Lee, D., & Lee, J. (2021).  
  *MelBERT: Metaphor Detection via Contextualized Late Interaction using Metaphorical Identification Theories*.](https://aclanthology.org/2021.naacl-main.141/)
- [MelBERT GitHub Repository](https://github.com/jin530/MelBERT)

