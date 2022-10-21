---
layout: post
title: SALUS (MLSys'20) Review
tags: [research, mlsys]
comments: false
---

DL 학습 시 GPU memory 사용 비중을 분석
- model: 비중 상대적으로 적음
- iteration 별로 ephemeral 하게 메모리 사용하는 비중 굉장히 큼

모델은 메모리에 올라가 있는 상태에서 특정 job의 한 iteration 끝나면 같은 lane에 있는 다른 job의 iteration을 같은 GPU에서 실행해주는 방식
즉, 두 job의 모델은 모두 GPU memory에 올라가 있는 상태에서 (모델이 차지하는 크기 상대적으로 크지 않음) job 들이 번갈아가면서 각자의 iteration 에 대해 model update 할 수 있게 해줌


TODO
- GPU stream 개념