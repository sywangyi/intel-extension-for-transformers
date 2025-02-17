# Installation

1. [Linux Installation](#linux-installation)

    1.1. [Prerequisites](#prerequisites)

    1.2. [Install from Pypi](#install-from-pypi)

    1.3. [Install from Source](#install-from-source)

2. [Windows Installation](#windows-installation)

    2.1. [Prerequisites](#prerequisites-1)

    2.2. [Install from Pypi](#install-from-pypi-1)

    2.3. [Install from Source](#install-from-source-1)

3. [System Requirements](#system-requirements)

   3.1. [Validated Hardware Environment](#validated-hardware-environment)

   3.2. [Validated Software Environment](#validated-software-environment)

## Linux Installation
### Prerequisites
The following prerequisites and requirements must be satisfied for a successful installation:

- Python version: 3.7 or 3.8 or 3.9 or 3.10
```
# Install Dependency
pip install -r requirements.txt
```
>**Note**: Recommend install protobuf <= 3.20.0 if use onnxruntime <= 1.11

### Install from Pypi

```Bash
# install stable basic version from pypi
pip install intel-extension-for-transformers
```
```Bash
# install nightly version
pip install -i https://test.pypi.org/simple/ intel-extension-for-transformers
# or install nightly version with only backend
pip install -i https://test.pypi.org/simple/ intel-extension-for-transformers-backend
```
```Shell
# install stable basic version from from conda
conda install -c intel intel-extension-for-transformers
```

### Install from Source
```Bash
git clone https://github.com/intel/intel-extension-for-transformers.git intel_extension_for_transformers
cd intel_extension_for_transformers
# Install Dependency
pip install -r requirements.txt
git submodule update --init --recursive
# Install intel_extension_for_transformers
python setup.py install
```

## Windows Installation

### Prerequisites

The following prerequisites and requirements must be satisfied for a successful installation:

- Python version: 3.7 or 3.8 or 3.9
- Visual Studio

### Install from Pypi

```Bat
pip install intel-extension-for-transformers
```

### Install from Source

```Bat
git clone https://github.com/intel/intel-extension-for-transformers.git intel_extension_for_transformers
cd intel_extension_for_transformers
# Install Dependency
pip install -r requirements.txt
git submodule update --init --recursive
# Install intel_extension_for_transformers
python setup.py install
  ```

## System Requirements
### Validated Hardware Environment
Intel® Extension for Transformers supports systems based on [Intel 64 architecture or compatible processors](https://en.wikipedia.org/wiki/X86-64) that are specifically optimized for the following CPUs:

* Intel Xeon Scalable processor (formerly Cascade Lake, Icelake)
* Future Intel Xeon Scalable processor (code name Sapphire Rapids)

### Validated Software Environment

* OS version: CentOS 8.4, Ubuntu 20.04
* Python version: 3.7, 3.8, 3.9  

<table class="docutils">
<thead>
  <tr>
    <th>Framework</th>
    <th>Intel TensorFlow</th>
    <th>PyTorch</th>
    <th>IPEX</th>
  </tr>
</thead>
<tbody>
  <tr align="center">
    <th>Version</th>
    <td class="tg-7zrl"><a href=https://github.com/Intel-tensorflow/tensorflow/tree/v2.10.0>2.10.0</a><br>
    <a href=https://github.com/Intel-tensorflow/tensorflow/tree/v2.9.1>2.9.1</a><br>
    <td class="tg-7zrl"><a href=https://download.pytorch.org/whl/torch_stable.html>1.13.0+cpu</a><br>
    <a href=https://download.pytorch.org/whl/torch_stable.html>1.12.0+cpu</a><br>
    <a href=https://download.pytorch.org/whl/torch_stable.html>1.11.0+cpu</a><br>
    <td class="tg-7zrl"><a href=https://github.com/intel/intel-extension-for-pytorch/tree/1.11.0>1.13.0</a><br>
    <a href=https://github.com/intel/intel-extension-for-pytorch/tree/v1.10.0>1.12.0</a></td>
  </tr>
</tbody>
</table>

* OS version: Windows 10
* Python version: 3.7, 3.8, 3.9  

<table class="docutils">
<thead>
  <tr>
    <th>Framework</th>
    <th>Intel TensorFlow</th>
    <th>PyTorch</th>
  </tr>
</thead>
<tbody>
  <tr align="center">
    <th>Version</th>
    <td><a href=https://github.com/Intel-tensorflow/tensorflow/tree/v2.9.1>2.9.1</a><br>
    <td><a href=https://download.pytorch.org/whl/torch_stable.html>1.13.0+cpu</a><br>
  </tr>
</tbody>
</table>
