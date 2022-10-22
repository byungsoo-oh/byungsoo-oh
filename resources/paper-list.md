---
layout: post
title: Paper List of Systems for Machine Learning
tags: [research, mlsys]
comments: false
---

# Paper List of Systems for Machine Learning

## Venues
CS conferences in systems, AI, data management (DB), and networking
- Systems / Computer architecture: SOSP, OSDI, ATC, EuroSys, FAST, ISCA, ASPLOS, HPCA
- AI: NeurIPS, ICML, ICLR
- Data management: VLDB, SIGMOD, ICDE
- Networking: NSDI, SIGCOMM

## Category
1. Data Processing
2. Training System
3. Inference System
4. ML Infrastructure

## Keywords
1. Data Processing
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

2. Training System
   - `DL scheduling`
   - `elastic training`
   - `gpu sharing`
   - `gpu memory wall`
   - `parallelism`, `distributed DL`
   - `model checkpointing`


## 1. Data Processing

### 1.1 Data pipeline optimization
#### 1.1.1 General
- [MLSys'22] Plumber: Diagnosing and Removing Performance Bottlenecks in Machine Learning Data Pipelines
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [ISCA'22] Understanding Data Storage and Ingestion for Large-Scale Deep Recommendation Model Training
  - `stall analysis` `prep stall` `fetch stall` `caching` 
- [SIGMOD'22] Where Is My Training Bottleneck? Hidden Trade-Offs in Deep Learning Preprocessing Pipelines
  - `stall analysis` `prep stall` `fetch stall` `caching` `offline-online prep` 
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

### 1.5 Data labeling automation
- [VLDB'18] Snorkel: Rapid Training Data Creation with Weak Supervision

## 2. Training System
### 2.1 DL scheduling
- [EuroSys'18] Optimus: an efficient dynamic resource scheduler for deep learning clusters
- [OSDI'18] Gandiva: Introspective Cluster Scheduling for Deep Learning

- [NSDI'19] Tiresias: A GPU Cluster Manager for Distributed Deep Learning
- [ATC'19] Analysis of Large-Scale Multi-Tenant GPU Clusters for DNN Training Workloads (*Philly*)

- [EuroSys'20] Balancing efficiency and fairness in heterogeneous GPU clusters for deep learning (*GandivaFair*)
- [NSDI'20] Themis: Fair and Efficient GPU Cluster Scheduling
- [OSDI'20] HiveD: Sharing a GPU Cluster for Deep Learning with Guarantees
- [OSDI'20] Heterogeneity-Aware Cluster Scheduling Policies for Deep Learning Workloads (*Gavel*)
- [EuroSys'20] AlloX: Compute Allocation in Hybrid Clusters
- [MLSys'20] Resource Elasticity in Distributed Deep Learning
  - `elastic training`

- [MLSys'21] Wavelet: Efficient DNN Training with Tick-Tock Scheduling
- [OSDI'21] Privacy Budget Scheduling (*DPF*)
- [NSDI'21] Elastic Resource Sharing for Distributed Deep Learning (*AFS*)
  - `elastic training`
- [OSDI'21] Pollux: Co-adaptive Cluster Scheduling for Goodput-Optimized Deep Learning
  - `elastic training`

- [NSDI'22] MLaaS in the wild: workload analysis and scheduling in large-scale heterogeneous GPU clusters (*PAI*)
- [OSDI'22] Looking Beyond GPUs for DNN Scheduling on Multi-Tenant Clusters (*Synergy*)
  - `elastic training`
- [SIGCOMM'22] Multi-resource interleaving for deep learning training (*Muri*)

### 2.2 GPU sharing
- [MLSys'20] Salus: Fine-Grained GPU Sharing Primitives for Deep Learning Applications
- [OSDI'20] AntMan: Dynamic Scaling on GPU Clusters for Deep Learning
- [OSDI'20] PipeSwitch: Fast Pipelined Context Switching for Deep Learning Applications
- [ATC'21] Zico: Efficient GPU Memory Sharing for Concurrent DNN Training

### 2.3 GPU memory wall
- [ASPLOS'20] SwapAdvisor: Pushing Deep Learning Beyond the GPU Memory Limit via Smart Swapping
- [SC'20] ZeRO: memory optimizations toward training trillion parameter models
- [VLDB'22] Harmony: Overcoming the Hurdles of GPU Memory Capacity to Train Massive DNN Models on Commodity Servers

### 2.4 Parallelism / Distributed training
- [ICML'18] Exploring Hidden Dimensions in Parallelizing Convolutional Neural Networks
- [SOSP'19] PipeDream: Generalized Pipeline Parallelism for DNN Training
- [MLSys'19] Beyond data and model parallelism for deep neural networks
- [MLSys'19] PyTorch-BigGraph: A Large-scale Graph Embedding System
- [SOSP'19] A Generic Communication Scheduler for Distributed DNN Training Acceleration
- [NeurIPS'19] Mesh-TensorFlow: Deep Learning for Supercomputers
- [OSDI'20] A Unified Architecture for Accelerating Distributed DNN Training in Heterogeneous GPU/CPU Clusters (*BytePS*)
- [VLDB'21] Distributed Deep Learning on Data Systems: A Comparative Analysis of Approaches
- [HPDC'22] Hare: Exploiting Inter-job and Intra-job Parallelism of Distributed Machine Learning on Heterogeneous GPUs
- [OSDI'22] Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning
- [NSDI'22] Accelerating Collective Communication in Data Parallel Training across Deep Learning Frameworks
- *[Survey Paper][ACM CSUR ('19)] Scalable Deep Learning on Distributed Infrastructures: Challenges, Techniques, and Tools*

### 2.5 DL job failures
- [ICSE'20] An Empirical Study on Program Failures of Deep Learning Jobs
- [ATC'22] Sibylla: To Retry or Not To Retry on Deep Learning Job Failure

### 2.6 GPU memory usage estimate
- [ESEC/FSE'20] Estimating GPU memory consumption of deep learning models

### 2.7 Model checkpointing
- [FAST'21] CheckFreq: Frequent, Fine-Grained DNN Checkpointing

## 3. Inference System
TBD

## 4. ML Infrastructure
- [CIDR '21] Ease.ML: A Lifecycle Management System for MLDev and MLOps
