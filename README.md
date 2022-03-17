# Generated Latent Fingerprint Dataset
The dataset consists of 484 Latent-Sensor and Latent-Latent pair of fingerprint images. Latent fingerprint images were generated from  2 public datasets FVC Dataset 2000-2004 [1] and Tsinghua Distorted Fingerprint Dataset [2] by using CycleGan [3]. The dataset was used in the "MinNet: Minutia Patch Embedding Network for Automated Latent Fingerprint Recognition" study to evalute the matching performance of proposed method.

| Dataset Name  | # Pair Image  |
| ------------- |:-------------:|
|FVC-Latent_Test_Dataset| 316 |
|Tsinghua-Latent_Test_Dataset| 168|

## FVC-Latent_Test_Dataset
Latent-Sensor pair images are placed in the same directory. The directory name can be translate to original FVC directory by VC2000DbsDb2a1 => FVC2000_Dbs/Db2_a/

FVC-Latent_Test_Dataset/ <br />
└── data <br />
    ├── VC2000DbsDb2a1   <br />
    │   ├── clean    <br />
    │   │   ├── 1_2.png   <br /> 
    │   │   └── 1_2.xyt    <br />
    │   └── latent    <br />
    │       ├── 1_5.png    <br />
    │       └── 1_5.xyt <br />
    ├── VC2000DbsDb2a10 <br />
    │   ├── clean <br />
    │   │   ├── 10_7.png <br />
    │   │   └── 10_7.xyt <br />
    │   └── latent <br />
    │       ├── 10_6.png <br />
    │       └── 10_6.xyt <br />

## Tsinghua-Latent_Test_Dataset

Tsinghua-Latent_Test_Dataset/ <br />
└── Latent_Latent <br />
    ├── 1 <br />
    │   ├── latent <br />
    │   │   ├── 3_1_fake_0_25.xyt <br />
    │   │   └── 3_1_fake.png <br />
    │   └── sensor <br />
    │       ├── 3_2_fake_0.xyt <br />
    │       └── 3_2_fake.png <br />
    ├── 10 <br />
    │   ├── latent <br />
    │   │   ├── 93_1_fake_0_25.xyt <br />
    │   │   └── 93_1_fake.png <br />
    │   └── sensor <br />
    │       ├── 93_2_fake_0.xyt <br />
    │       └── 93_2_fake.png <br />


## References
[1] D. Maio, D. Maltoni, R. Cappelli, J.L. Wayman, and A.K.Jain. Fvc2000: fingerprint verification competition. IEEE Transactions on Pattern Analysis and Machine Intelligence, 24(3):402–412, 2002


[2] Xuanbin Si, Jianjiang Feng, Jie Zhou, and Yuxuan Luo. Detection and rectification of distorted fingerprints. IEEE Transactions on Pattern Analysis and Machine Intelligence, 37(3):555–568, 2015

[3]Jun-Yan Zhu, Taesung Park, Phillip Isola, and Alexei A. Efros. Unpaired image-to-image translation using cycle-consistent adversarial networks. In 2017 IEEE International Conference on Computer Vision (ICCV), pages 2242–2251, 2017.
