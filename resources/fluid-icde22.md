---
layout: post
title: Fluid (ICDE'22) Review
tags: [research, mlsys]
comments: false
---

## Fluid: Dataset Abstraction and Elastic Acceleration for Cloud-native Deep Learning Training Jobs (ICDE'22)

Keywords: `DL on cloud-native infra`, `fetch stall`, `auto-tuned distributed cache`, `auto-scaling cache`, `sharing cache`

### Background & Problem
- DL 학습 시 자원을 효율적으로 활용하기 위해 k8s 등을 기반으로 한 cloud-native infrastructure 활용하는 것이 일반화되고 있음
- Cloud-native infrastructure에서 compute resource를 보다 효과적으로 scaling 하기 위해 storage를 **decouple** 하는 경우가 일반적임
- **문제**: Storage service가 decouple 된 *cloud 환경에서* **data fetch 작업이 학습의 bottleneck** 되는 경우 증가하고 있음 (fetch stall)


### Limits of Existing Approaches
Fetch stall 문제 해결 위한 기존 솔루션들은 **Cloud-native 환경에서** 여러 한계 있음

1. Heterogeneous cloud storage로부터의 효과적인 data fetch 어려움 [Q: <U>하나의 DL job</U> 내에서 hetero storage로부터 fetch?]
    - Cloud 환경에서는 여러 heterogeneous storage (S3, HDFS, Ceph 등)으로부터 data fetch 하는 경우 일반적
    - Application에서 manual하게 여러 storage에 대한 fetch를 효율적으로 수행하기 위한 통합적인 방법 부재함
    - 또한, 각 storage의 underlying caching system을 서로 다른 dataset에 대해 최적으로 tune 하는 것 어려움
2. Cache system의 scaling 어려움
   - 워크로드에 따라 compute resource를 유연하게 scaling 하는 방법은 많이 연구되었음
   - 하지만 이러한 compute resource scaling에 맞춰 caching을 scaling 하는 방법은 연구 X
     - [Q: compute resource 더 많이 필요 == cache capacity 더 많이 필요? vice versa? Online 전처리 시 CPU 사용량 증가함에 따라 CPU 할당량 증가 &rarr; cache capacity도 증가? / 학습 속도가 느리면 compute resource 증가 &rarr; cache도 더 많이 해야됨?]
3. 같은 dataset을 여러 DL job에서 사용 시 효과적인 cache sharing 방법 없음


### Solution Overview
1. Cloud-native dataset abstraction (*Fluid Dataset*)
   - *Fluid Dataset*: Heterogeneous dataset에 transparent 하게 접근할 수 있는 unified logical interface (k8s PVC)
   - *Fluid Dataset*은 내부적으로 [Alluxio](https://docs.alluxio.io/os/user/stable/en/Overview.html) runtime과 같은 auto-tuned cache runtime을 통해 사용자의 cache manual tuning 어려움 줄임

2. On-the-fly cache system autoscaler
   - 학습 속도 tracking을 통한 cache scaling 방법 디자인 및 구현
   - 학습 속도가 느림 &rarr; 할당되는 compute 늘리기 + **cache capacity도 자동으로 늘리기**

3. Cache sharing based job scheduling
   - 여러 DL job에서 효과적으로 cache share 시 cache thrash (빈번한 cache misses) 발생하지 않게 하기 위한 효과적인 cache sharing 방법 연구


[Q: Training dynamics 변화에 대한 고려? 본 연구와는 orthogonal?]

### System Design
#### Fluid Dataset: High-level data abstraction
A. Dataset abstraction and management
- Fluid Dataset [TBD]
- Cache runtime [TBD]

B. Automatic configuration for distributed cache systems
[TBD]


#### Cache system autoscaling mechanism and cache sharing based job scheduling
A. On-the-fly cache system autoscaling mechanism
[TBD]

B. Cache sharing based scheduling policy
[TBD]

### System Implementation
A. System Architecture
[TBD]

B. Key Components in Fluid
[TBD]
1) Fluid controller
2) Fluid CSI plugin
3) Cache system autoscaler
4) Fluid scheduler

C. Fluid Usage
[TBD]
