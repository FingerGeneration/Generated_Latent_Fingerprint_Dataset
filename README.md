# Generated Latent Fingerprint Dataset
The dataset consists of 484 Latent-Sensor and Latent-Latent pair of fingerprint images. Latent fingerprint images were generated from  two public datasets FVC Dataset 2000-2004 [1] and Tsinghua Distorted Fingerprint Dataset [2] by using CycleGan [3]. The datasets were used in the "MinNet: Minutia Patch Embedding Network for Automated Latent Fingerprint Recognition" study to evalute the matching performance of proposed method.

| Dataset Name  | # Pair Image  |
| ------------- |:-------------:|
|FVC-Latent_Test_Dataset| 316 |
|Tsinghua-Latent_Test_Dataset| 168|

## FVC-Latent_Test_Dataset
Latent-Sensor pair images are placed in the same directory. Query latent image (in the latent folder) must be match with pair sensor image (in the clean folder) in the same directory against all sensor image by matcher. The directory names can be translate to original FVC directory by VC2000DbsDb2a1 => FVC2000_Dbs/Db2_a/

### Directory Tree 
FVC-Latent_Test_Dataset/ <br />
├── data <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── VC2000DbsDb2a1   <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── clean    <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 1_2.png   <br /> 
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 1_2.xyt    <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── latent    <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 1_5.png    <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 1_5.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── VC2000DbsDb2a10 <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── clean <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 10_7.png <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 10_7.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── latent <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 10_6.png <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 10_6.xyt <br />

## Tsinghua-Latent_Test_Dataset
 
Latent-Latent pair images are placed in the same directory. Query latent image (in the Latent folder) must be match with pair sensor image (in the sensor folder) in the same directory against all image which is placed in the sensor directory by matcher.

**Tsinghudataset.xlsx :** 4-columns show the RangeStart-RangeEnd for each fingerprint ID. For instance, 2nd rows shows that images from 1_1.png to 10_1.png belong to same ID (therefore same finger). Therefore, we assigned the same ID name for these images. Unfortunately, dataset also contains multiple images of the same finger in non sequential manner.For instance, as row 7 shows that images 51_1.png to 60_1.png belong to finger ID number 6, but image names 103_1.png and 104_1.png (see row 13) also belong to the same finger. Therefore, we only use row 13 images when building the dataset. So, if SameID column value is not empty, it contains the ID number of the same image ID names. SameID values are not included in the final dataset.


### Directory Tree
Tsinghua-Latent_Test_Dataset/ <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├──  Latent_Latent <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── 1 <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── latent <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 3_1_fake_0_25.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 3_1_fake.png <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── sensor <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── 3_2_fake_0.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;└── 3_2_fake.png <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── 10 <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── latent <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;├── 93_1_fake_0_25.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 93_1_fake.png <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── sensor <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;├── 93_2_fake_0.xyt <br />
&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;└── 93_2_fake.png <br />


## References
[1] D. Maio, D. Maltoni, R. Cappelli, J.L. Wayman, and A.K.Jain. Fvc2000: fingerprint verification competition. IEEE Transactions on Pattern Analysis and Machine Intelligence, 24(3):402–412, 2002


[2] Xuanbin Si, Jianjiang Feng, Jie Zhou, and Yuxuan Luo. Detection and rectification of distorted fingerprints. IEEE Transactions on Pattern Analysis and Machine Intelligence, 37(3):555–568, 2015

[3]Jun-Yan Zhu, Taesung Park, Phillip Isola, and Alexei A. Efros. Unpaired image-to-image translation using cycle-consistent adversarial networks. In 2017 IEEE International Conference on Computer Vision (ICCV), pages 2242–2251, 2017.
