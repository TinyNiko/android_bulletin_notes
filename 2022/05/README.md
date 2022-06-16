# Framework

## Framework

### CVE-2021-39662

| CVE-2021-39662 | [A-197302116](https://android.googlesource.com/platform/packages/providers/MediaProvider/+/76f725361312644461b9021380ba4d0d9d32108e) | EoP | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20004

| CVE-2022-20004 | [A-179699767](https://android.googlesource.com/platform/frameworks/base/+/b55656825844f8ac1d776da0b3290a4e9948ba4f) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20005

| CVE-2022-20005 | [A-219044664](https://android.googlesource.com/platform/frameworks/base/+/5df6c3f7099d3d2e237f54c41692bdef5f090d45) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20007

| CVE-2022-20007 | [A-211481342](https://android.googlesource.com/platform/frameworks/base/+/9a1dfd9a9de3bb33cd81e3003251b49f7862f276) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2021-39700

| CVE-2021-39700 | [A-201645790](https://android.googlesource.com/platform/system/sepolicy/+/ac15c76a51cebb2114f80f6fc2863fc671e7e2c4) | ID | Moderate |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | -------- |

## System

### CVE-2022-20113


| CVE-2022-20113 | [A-205996517](https://android.googlesource.com/platform/packages/apps/Settings/+/875f42e1d3a6ac5083f7f42c7d549a6e09e69484) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20114

| CVE-2022-20114 | [A-211114016](https://android.googlesource.com/platform/packages/services/Telecomm/+/a2f52c2d771e0acea6bb27fdbe6dae2b37f2df04) | EoP | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20116

| CVE-2022-20116 | [A-212467440](https://android.googlesource.com/platform/frameworks/base/+/35998a72b71c1c18a77815e40a6b08bd9e93c97b) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

### CVE-2022-20010

| CVE-2022-20010 | [A-213519176](https://android.googlesource.com/platform/system/bt/+/2dceafe75bda383e609910b3c882a155a32584af) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------- | -- | ---- |

### CVE-2022-20011

| CVE-2022-20011 | [A-214999128](https://android.googlesource.com/platform/frameworks/base/+/f315ba91df3829d862371fbab9da584ce0a59bc6) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |

bluetooth protocol stack

### CVE-2022-20115

| CVE-2022-20115 | [A-210118427](https://android.googlesource.com/platform/frameworks/base/+/abb41637225c95d5530bff275531a446be66a18c) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |


### CVE-2021-39670

| CVE-2021-39670 | [A-204087139](https://android.googlesource.com/platform/frameworks/base/+/b1b01433f5b8dc0702c0e1abde5f7b86b708a849) | DoS | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |


### CVE-2022-20112

| CVE-2022-20112 | [A-206987762](https://android.googlesource.com/platform/packages/apps/Settings/+/c5d1f8d5b16153a046403e910eb4ff2224306cc9) | DoS | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |


# Kernel

## Kernel

### ** CVE-2022-0847

| CVE-2022-0847 | A-220741611``[Upstream kernel](https://android.googlesource.com/kernel/common/+/b9b8fd203dba3) [[2](https://android.googlesource.com/kernel/common/+/b19ec7afa9297)] [[3](https://android.googlesource.com/kernel/common/+/aa3e9c7480830f38390a61501386be4a03efb88d)] | EoP | High | pipes |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --- | ---- | ----- |


### ** CVE-2022-20009

| CVE-2022-20009 | A-213172319``[Upstream kernel](https://android.googlesource.com/kernel/common/+/528615555b59cbd659186d44b3c6db69c30414eb) [[2](https://android.googlesource.com/kernel/common/+/823fc2b264f1ec12678564271c5fa34e3250cf83)] | EoP | High | Linux |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | ---- | ----- |


### CVE-2022-20008

| CVE-2022-20008 | A-216481035``[Upstream kernel](https://android.googlesource.com/kernel/common/+/2aea7dc18f4249dc53e53598db50b59c26a60aeb) [[2](https://android.googlesource.com/kernel/common/+/8a3679a75730c1babde6bf63e35d227f3305bd90)] [[3](https://android.googlesource.com/kernel/common/+/8f66dc1a78a743ea3c3f039500d2aa0cddd776d5)] | ID | High | SD MMC |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -- | ---- | ------ |

### CVE-2021-22600

| CVE-2021-22600 | A-213464034``[Upstream kernel](https://android.googlesource.com/kernel/common/+/27fc5a7c6972bd73ac0cc0cf811ec2ecb989014f) | EoP | Moderate | Kernel |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------- | --- | -------- | ------ |


## MediaTek components

### CVE-2022-20084

| CVE-2022-20084 | A-223071148``M-ALPS06498874 [*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High | telephony |
| -------------- | ----------------------------------------------------------------------------------------------------- | ---- | --------- |

In telephony, there is a possible way to disable receiving emergency broadcasts due to a missing permission check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

### CVE-2022-20109

| CVE-2022-20109 | A-223072269``M-ALPS06399915 [*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High | ion |
| -------------- | ----------------------------------------------------------------------------------------------------- | ---- | --- |

In ion, there is a possible use after free due to improper update of reference count. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation

### CVE-2022-20110

| CVE-2022-20110 | A-223071150``M-ALPS06399915 [*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High | ion |
| -------------- | ----------------------------------------------------------------------------------------------------- | ---- | --- |

In ion, there is a possible use after free due to a race condition. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

## Qualcomm components

### CVE-2022-22057

| CVE-2022-22057 | A-218337595``[QC-CR#3077687](https://source.codeaurora.org/quic/la/kernel/msm-5.4/commit/?id=339824df70a0e9e08f2a7151b776d72421050f04) | High | Display |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ------- |

UAF

### CVE-2022-22064

| CVE-2022-22064 | A-218338071``[QC-CR#3042282](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=9e8dbd5b761e9a152cb77562ec20124b5b69c7cf)``[QC-CR#3048959](https://source.codeaurora.org/quic/le/platform/vendor/qcom-opensource/wlan/prima/commit/?id=b84f0da6a06d2f4c6f497b1bf3c291e71fb37838)``[QC-CR#3056532](https://source.codeaurora.org/quic/le/platform/vendor/qcom-opensource/wlan/prima/commit/?id=d2a6e223866ca0de9af3fad7a2ad7a44658f479d)``[QC-CR#3049158](https://source.codeaurora.org/quic/le/platform/vendor/qcom-opensource/wlan/qcacld-2.0/commit/?id=6fba8935de694cc61a13bba40fd1251097cdc014) [[2](https://source.codeaurora.org/quic/le/platform/vendor/qcom-opensource/wlan/qcacld-2.0/commit/?id=ba9e94231a2b072f44ba702682bd0dc23cb37edc)] | High | WLAN |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |

### CVE-2022-22065

| CVE-2022-22065 | A-218337597``[QC-CR#3042293](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=d737412829798dd54e8355074f4653662a763c02)``[QC-CR#3064612](https://source.codeaurora.org/quic/le/platform/vendor/qcom-opensource/wlan/prima/commit/?id=edc957bca2d254d202765b7fd131261ad2b75a29) | High | WLAN |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |

### CVE-2022-22068

| CVE-2022-22068 | A-218337596``[QC-CR#3084983](https://source.codeaurora.org/quic/la/kernel/msm-5.4/commit/?id=57a6844ba565447f802abecc9e47b39f33187ef2) [[2](https://source.codeaurora.org/quic/le/kernel/msm-4.19/commit/?id=0098ef73cc8d83fce4583252d3fe5e95642e9a9f)] | High | Kernel |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------ |

### CVE-2022-22072

| CVE-2022-22072 | A-218339149``[QC-CR#3073345](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=34fa11aeb2d9232d4ed4b4babab0e4760f04aa92) [[2](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=18eae871c458008b7b7fcb729a3c9a73e4fdc135)] | High | WLAN |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ---- |

## Qualcomm closed-source components


| CVE-2021-35090 | A-204905205[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | Critical | Closed-source component |
| -------------- | ----------------------------------------------------------------------------- | -------- | ----------------------- |
| CVE-2021-35072 | A-204905110[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35073 | A-204905209[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35076 | A-204905151[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35078 | A-204905326[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35080 | A-204905287[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35086 | A-204905289[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35087 | A-204905111[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35094 | A-204905838[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35096 | A-204905290[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
| CVE-2021-35116 | A-209469826[*](https://source.android.com/security/bulletin/2022-05-01#asterisk) | High     | Closed-source component |
