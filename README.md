

<h1 align="center">📂 Image Commands Application</h1>

<p align="center">
    This repository contains a demonstration of applying various commands to image files as per the lecture on August 17, 2024. Below are detailed steps, commands, and the expected results with images.
</p>

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Prerequisites](#-prerequisites)
- [Setup Project Directory](#-setup-project-directory)
- [Steps](#-steps)
  - [1. Download Required Files](#1-download-required-files)
  - [2. Extract Files](#2-extract-files)
  - [3. Apply Commands](#3-apply-commands)
  - [4. Verify Results](#4-verify-results)
- [Expected Output](#-expected-output)
- [Resources](#-resources)
- [Notes](#-notes)

---

## 🔍 Project Overview

This project involves downloading, extracting, and applying specific Linux commands to image files provided in the lecture on August 17, 2024. The files are analyzed using tools such as `fdisk` and `affinfo`, and the results are documented in this README.

---

## 🛠 Prerequisites

Ensure the following tools are installed:

- **Linux OS** (Ubuntu recommended)
- **Packages**: `gzip`, `tar`, `afflib-tools` , `build-essential`, `libtool`, `autoconf`, `automake`, `git`, `libewf-dev`, `sleuthkit`, `afflib3`, `libssl-dev`, `libvmdk-dev`, `libvslm-dev`

You can install them using:

### gzip tar afflib-tools
```bash
sudo apt update
sudo apt install gzip tar afflib-tools
```
### build-essential libtool autoconf automake git libewf-dev
```bash
sudo apt install build-essential libtool autoconf automake git libewf-dev
```
### build-essential libtool autoconf automake git libewf-dev
1. Download sleuthkit from github
```bash 
git clone https://github.com/sleuthkit/sleuthkit.git
```

2. Start install requirement by using script bootstrap.sh
```bash 
./bootstrasp
or
sh bootstrap.sh
```
3. checking all needed requirement for installing sleuthkit
```bash 
./configure
```

### afflib3 (to support image of type “.aff”)
    
1. Download sleuthkit from github
```bash 
git clone https://github.com/sshock/AFFLIBv3.git
```
    
2. Start install requirement by using script bootstrap.sh
```bash 
./bootstrasp
or
sh bootstrap.sh
```
    
3. checking all needed requirement for installing AFFLIB3
```bash 
./configure
```
### libssl-dev (missing library for AFFLIB3)
1. install 
```bash 
sudo apt install libssl-dev
```
2. checking all needed requirement for installing AFFLIB3
```bash 
./configure
```
**pass**

3. go to AFFLIB3 directory
```bash 
cd AFFLIB3
```

4. make to billd
```bash 
make
sudo make install
```
5. go out then go to sleurhkit directory
```bash 
cd
cd sleurhkit
```
6. checking all needed requirement for installing sleurhkit
```bash 
./configure
```
**sleuthkit now supports afflib**

### sleuthkit supports all type of images
```bash 
cd
sudo apt install libvhdi-dev libvmdk-dev libvslm-dev
cd sleurhkit
./configure
```
after that 
```bash
make
sudo make install
```
Check images that sleuthkit support
```bash
Mmls –i list:
```
---
$$$$$$$$$$$$$$
<!--
## 📁 Setup Project Directory

First, create a dedicated directory for this project:

```bash
mkdir image-commands-project
cd image-commands-project
```

This directory will store all the downloaded files and the results of applied commands.

---

## 📝 Steps

### 1. Download Required Files

Download the necessary files using the commands below:

```bash
wget https://linuxleo.com/Files/gptimage.raw.gz
wget https://dftt.sourceforge.net/test10/index.html
wget https://linuxleo.com/Files/able2.tar.gz
wget https://digitalcorpora.s3.amazonaws.com/corpora/drives/nps-2009-ntfs1/ntfs1-gen1.aff
```

### 2. Extract Files

After downloading, extract the compressed files:

```bash
# Extract .gz file
gzip -d gptimage.raw.gz

# Extract .tar.gz file
tar -xzvf able2.tar.gz
```

### 3. Apply Commands

Now, apply the necessary commands to the extracted files:

- **Analyze `gptimage.raw`**:

    ```bash
    fdisk -l gptimage.raw
    ```

- **Analyze `ntfs1-gen1.aff`** with `affinfo`:

    ```bash
    affinfo ntfs1-gen1.aff
    ```

- **Explore the contents of `able2.tar.gz`**:

    ```bash
    cd able2
    ls -l
    ```

### 4. Verify Results

Check the outputs from the commands to ensure the image files were processed correctly:

```bash
fdisk -l gptimage.raw
affinfo ntfs1-gen1.aff
```

---

## 📊 Expected Output

Below are the expected outputs for each command, with screenshots included:

- **`fdisk` output for `gptimage.raw`**:

<p align="center">
  <img src="path/to/partition-output.png" alt="Partition Output" />
</p>

- **`affinfo` output for `ntfs1-gen1.aff`**:

<p align="center">
  <img src="path/to/affinfo-output.png" alt="AFF Info Output" />
</p>

- **Contents extracted from `able2.tar.gz`**:

<p align="center">
  <img src="path/to/able2-contents.png" alt="Able2 Contents" />
</p>

Replace `path/to/` with the actual path to your image files in the repository.

---

## 📂 Resources

- [gptimage.raw.gz](https://linuxleo.com/Files/gptimage.raw.gz)
- [test10 index](https://dftt.sourceforge.net/test10/index.html)
- [able2.tar.gz](https://linuxleo.com/Files/able2.tar.gz)
- [ntfs1-gen1.aff](https://digitalcorpora.s3.amazonaws.com/corpora/drives/nps-2009-ntfs1/ntfs1-gen1.aff)

---

## 💡 Notes

- Make sure that you have sufficient disk space to extract large files.
- If any commands fail due to missing packages, ensure the required packages are installed by running the command:

  ```bash
  sudo apt install <missing-package-name>
  ```

- The screenshots provided in this README should be replaced with your actual output to reflect the results of your execution.

<p align="center">🛠️ Created by <strong>Your Name</strong></p>

-->
