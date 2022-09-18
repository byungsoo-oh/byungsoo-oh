---
layout: post
title: Paper List of Systems for Machine Learning
tags: [research, mlsys]
comments: false
---

# Paper List of Systems for Machine Learning

## Venues:
CS conferences in systems, AI, data management (DB), and network
- Systems: SOSP, OSDI, ATC, EuroSys, FAST, ISCA, ASPLOS, HPCA
- AI: NeurIPS, ICML, ICLR
- Data management: VLDB, SIGMOD, ICDE
- Network: NSDI, SIGCOMM

## Category
- Data Processing
- Training System
- Inference System
- ML Infrastructure

## Keywords
- `stall analysis`
- `prep stall`
- `fetch stall`
- `caching`
- `offloading`
- `auto-scaling`
- `data labeling`
- `data format`
- `DLRM`
- `GNN`
- `offline-online prep`
- `scehduling`
- `parallelism`
- `mlops`
- `DAG optimization`

## 1. Data Processing

### 1.1 Data pipeline optimization
#### 1.1.1 General
- [MLSys'22] Plumber: Diagnosing and Removing Performance Bottlenecks in Machine Learning Data Pipelines
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [ISCA'22] Understanding Data Storage and Ingestion for Large-Scale Deep Recommendation Model Training
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [SIGMOD'22] Where Is My Training Bottleneck? Hidden Trade-Offs in Deep Learning Preprocessing Pipelines
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [VLDB'21] Analyzing and Mitigating Data Stalls in DNN Training
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [VLDB'21] tf.data: A Machine Learning Data Processing Framework
  - `prep stall` `fetch stall`


#### 1.1.2 Prep stalls
- [ATC'22] Cachew: Machine Learning Input Data Processing as a Service
  - `prep stall` `offloading` `auto-scaling` `caching`
- [OSDI'22] Looking Beyond GPUs for DNN Scheduling on Multi-Tenant Clusters
  - `scheduling` `prep stall` `fetch stall`


#### 1.1.3 Fetch stalls (I/O)
- [ICPP'22] Lobster: Load Balance-Aware I/O for Distributed DNN Training
- [SC'21] Clairvoyant Prefetching for Distributed Machine Learning I/O


#### 1.1.4 Specific workloads (GNN, DLRM)
- [NSDI'23] (to appear) BGL: GPU-Efficient GNN Training by Optimizing Graph Data I/O and Preprocessing
- [DAC'22] A Joint Management Middleware to Improve Training Performance of Deep Recommendation Systems with SSDs
- [VLDB'22] Accelerating Recommendation System Training by Leveraging Popular Choices


### 1.2 Caching
- [ICDE'22] Fluid: Dataset Abstraction and Elastic Acceleration for Cloud-native Deep Learning Training Jobs
- [ATC'21] Refurbish Your Training Data: Reusing Partially Augmented Samples for Faster Deep Neural Network Training
- [FAST'20] Quiver: An Informed Storage Cache for Deep Learning
- [ICPP'20] DIESEL: A Dataset-Based Distributed Storage and Caching System for Large-Scale Deep Learning Training
- [arXiv preprint ('19)] Faster Neural Network Training with Data Echoing
- [HotCloud'19] The Case for Unifying Data Loading in Machine Learning Clusters


### 1.3 Data formats
- [ECCV'22] L3: Accelerator-Friendly Lossless Image Format for High-Resolution, High-Throughput DNN Training
- [VLDB'21] Progressive compressed records: Taking a byte out of deep learning data

### 1.4 Data pipeline fairness & correctness
- [CIDR'21] Lightweight Inspection of Data Preprocessing in Native Machine Learning Pipelines

### 1.5 Data Labeling Automation
- [VLDB'18] Snorkel: Rapid Training Data Creation with Weak Supervision

## 2. Training System
TBD

## 3. Inference System
TBD

## 4. ML Infrastructure
- [CIDR '21] Ease.ML: A Lifecycle Management System for MLDev and MLOps
