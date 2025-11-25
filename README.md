# Active Learning on Graph Data: Enhanced Clustering on Cora Dataset Using AlphaMixSampling

---

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Parameters](#parameters)
- [Results](#results)
- [Original Repository](#original-repository)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

Active learning reduces the need for large labeled datasets by selecting the most informative samples for labeling. This project applies the AlphaMixSampling strategy, which mixes features to enhance active learning, on graph-structured data using the Cora dataset. The method improves clustering performance with fewer labeled samples.

---

## Features

- AlphaMixSampling active learning implementation.
- Application on graph data (Cora dataset).
- Improved clustering accuracy.
- Easy-to-run code with customizable parameters.
- Logging support for training monitoring.

---

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    cd your-repo-name
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

Run training on the Cora dataset with:

```bash
python main.py \
    --data_name Cora --data_dir your_data_directory --log_dir your_log_directory \
    --n_init_lb 100 --n_query 100 --n_round 10 --learning_rate 0.001 --n_epoch 1000 --model mlp \
    --strategy AlphaMixSampling --alpha_opt
