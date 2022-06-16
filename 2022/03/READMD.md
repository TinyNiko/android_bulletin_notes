# Framework

## Android runtime

### CVE-2021-39689

| CVE-2021-39689 | [A-206090748](https://android.googlesource.com/platform/system/security/+/9a374680df1912fb983bf174d88ddeb71932cec1) | EoP | Moderate |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | -------- |

## Framework

### CVE-2021-39692

| CVE-2021-39692 | [A-209611539](https://android.googlesource.com/platform/packages/apps/ManagedProvisioning/+/a07188111567974bc8a2c817825c28169c589535) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[Diff - a07188111567974bc8a2c817825c28169c589535^! - platform/packages/apps/ManagedProvisioning - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/ManagedProvisioning/+/a07188111567974bc8a2c817825c28169c589535%5E%21/#F1)

UI problem which leading to tapjacking.

### CVE-2021-39693

| CVE-2021-39693 | [A-208662370](https://android.googlesource.com/platform/frameworks/base/+/f14e212d82b32053d151eedf97ac59a4b5b18369) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[Diff - f14e212d82b32053d151eedf97ac59a4b5b18369^! - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/f14e212d82b32053d151eedf97ac59a4b5b18369%5E%21/#F0)

### CVE-2021-39695

| CVE-2021-39695 | [A-209607944](https://android.googlesource.com/platform/frameworks/base/+/b5efdf729385cc54f225496d3ba20f1cb5b68250) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[Diff - b5efdf729385cc54f225496d3ba20f1cb5b68250^! - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/b5efdf729385cc54f225496d3ba20f1cb5b68250%5E%21/#F0)

### CVE-2021-39697

| CVE-2021-39697 | [A-200813547](https://android.googlesource.com/platform/packages/providers/DownloadProvider/+/0dc5048914eb6a7f919c8749172b971cbb315870) [[2](https://android.googlesource.com/platform/packages/providers/DownloadProvider/+/9ff84f6d353a7647efba91d74e31d17ba6b765b7)] | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[Diff - 0dc5048914eb6a7f919c8749172b971cbb315870^! - platform/packages/providers/DownloadProvider - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/providers/DownloadProvider/+/0dc5048914eb6a7f919c8749172b971cbb315870%5E%21/#F0)

### CVE-2021-39624

| CVE-2021-39624 | [A-67862680](https://android.googlesource.com/platform/frameworks/base/+/a4ef9e0e00416d8e211bd749da42033ae4fd9eb2) [[2](https://android.googlesource.com/platform/frameworks/base/+/50db8a56a226e6afc0288d3894ca226938f4af4b)] | DoS | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[Diff - a4ef9e0e00416d8e211bd749da42033ae4fd9eb2^! - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/a4ef9e0e00416d8e211bd749da42033ae4fd9eb2%5E%21/#F0)

### CVE-2021-39690

| CVE-2021-39690 | [A-204316511](https://android.googlesource.com/platform/frameworks/native/+/2914a57d755051a3e5f05154d784a08019500946) | DoS | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[2914a57d755051a3e5f05154d784a08019500946 - platform/frameworks/native - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/native/+/2914a57d755051a3e5f05154d784a08019500946)

It' s not easy to find this problem.

## Media Framework

### CVE-2021-39667

| CVE-2021-39667 | [A-205702093](https://android.googlesource.com/platform/external/libavc/+/dc110841d6a3fb2f9c9f1af04b3b71da40fbd392) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |

[Diff - dc110841d6a3fb2f9c9f1af04b3b71da40fbd392^! - platform/external/libavc - Git at Google (googlesource.com)](https://android.googlesource.com/platform/external/libavc/+/dc110841d6a3fb2f9c9f1af04b3b71da40fbd392%5E%21/#F0)

Software decoder.

## System

### CVE-2021-39708

| CVE-2021-39708 | A-206128341 | EoP | Critical |
| -------------- | ----------- | --- | -------- |

In gatt_process_notification of gatt_cl.cc, there is a possible out of bounds write due to an incorrect bounds check. This could lead to remote escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation

Bluetooth problem.

### CVE-2021-0957

| CVE-2021-0957 | [A-193149550](https://android.googlesource.com/platform/frameworks/base/+/e4d9de5961d9ec2fa9dc7103e4eb652e60d624c3) | EoP | High |
| ------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[e4d9de5961d9ec2fa9dc7103e4eb652e60d624c3 - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/e4d9de5961d9ec2fa9dc7103e4eb652e60d624c3)

### CVE-2021-39701

| CVE-2021-39701 | [A-212286849](https://android.googlesource.com/platform/frameworks/base/+/d0e683b8f65ba43e596911324bbff2e4f9909303) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[d0e683b8f65ba43e596911324bbff2e4f9909303 - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/d0e683b8f65ba43e596911324bbff2e4f9909303)

### CVE-2021-39702

| CVE-2021-39702 | [A-205150380](https://android.googlesource.com/platform/packages/apps/Settings/+/db9333baac7c609a32536a2f8d66233132306aab) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[db9333baac7c609a32536a2f8d66233132306aab - platform/packages/apps/Settings - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Settings/+/db9333baac7c609a32536a2f8d66233132306aab)

System overlay Problem.

### CVE-2021-39703

| CVE-2021-39703 | [A-207057578](https://android.googlesource.com/platform/frameworks/base/+/54f4c1843d4d41fb784f416575ec8b9857e3d195) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[54f4c1843d4d41fb784f416575ec8b9857e3d195 - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/54f4c1843d4d41fb784f416575ec8b9857e3d195)

### CVE-2021-39704

| CVE-2021-39704 | [A-209965481](https://android.googlesource.com/platform/frameworks/base/+/b925955552885a049fcbff978415612dad3e447d) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[b925955552885a049fcbff978415612dad3e447d - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/b925955552885a049fcbff978415612dad3e447d)

### CVE-2021-39706

| CVE-2021-39706 | [A-200164168](https://android.googlesource.com/platform/packages/apps/Settings/+/6407b20ab3ab49318ba5cbfc0d6b59c675df67b4) [[2](https://android.googlesource.com/platform/packages/apps/Car/Settings/+/6a6489935d203715a755b21b374e1e3b3085aa3f)] | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[6407b20ab3ab49318ba5cbfc0d6b59c675df67b4 - platform/packages/apps/Settings - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Settings/+/6407b20ab3ab49318ba5cbfc0d6b59c675df67b4)

### CVE-2021-39707

| CVE-2021-39707 | [A-200688991](https://android.googlesource.com/platform/packages/apps/Settings/+/4fb753d22e6a2505b1667950d153bc03ad8ae422) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[4fb753d22e6a2505b1667950d153bc03ad8ae422 - platform/packages/apps/Settings - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Settings/+/4fb753d22e6a2505b1667950d153bc03ad8ae422)

### CVE-2021-39709

| CVE-2021-39709 | [A-208817618](https://android.googlesource.com/platform/packages/services/Telephony/+/7c9b65a4de4540a50a16781e9f55857544453bc2) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[7c9b65a4de4540a50a16781e9f55857544453bc2 - platform/packages/services/Telephony - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/services/Telephony/+/7c9b65a4de4540a50a16781e9f55857544453bc2)

Pending Intent problem.

### CVE-2021-39705

| CVE-2021-39705 | [A-186026746](https://android.googlesource.com/platform/packages/apps/Dialer/+/a38caf0ff62e0b3c8a7710c44277607244149fed) [[2](https://android.googlesource.com/platform/packages/apps/Dialer/+/02e1666deb3f1f638a0ca5510e75b126c13ddbf1)] [[3](https://android.googlesource.com/platform/packages/apps/Dialer/+/f7944b6c2d690bc27660124f4bd11593eee5bd05)] | ID | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -- | ---- |

[a38caf0ff62e0b3c8a7710c44277607244149fed - platform/packages/apps/Dialer - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Dialer/+/a38caf0ff62e0b3c8a7710c44277607244149fed)

## Google Play

### CVE-2021-39667

In ih264d_parse_decode_slice of ih264d_parse_slice.c, there is a possible out of bounds write due to a heap buffer overflow. This could lead to remote information disclosure with no additional execution privileges needed. User interaction is needed for exploitation

# Kernel

## Framework

### CVE-2021-39694

| CVE-2021-39694 | A-202312327 | EoP | High |
| -------------- | ----------- | --- | ---- |

In parse of RoleParser.java, there is a possible way for default apps to get permissions explicitly denied by the user due to a permissions bypass. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation

## Kernel components

### CVE-2020-29368

| CVE-2020-29368 | A-174738029``[Upstream kernel](https://android.googlesource.com/kernel/common/+/c444eb564fb16645c172d550359cb3d75fe8a040) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[
c444eb564fb16645c172d550359cb3d75fe8a040 - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/c444eb564fb16645c172d550359cb3d75fe8a040)

### CVE-2021-39685

| CVE-2021-39685 | A-210292376``[Upstream kernel](https://android.googlesource.com/kernel/common/+/b4604acd52a691c2fd33ad0a0fafb7cc19dee5de) [[2](https://android.googlesource.com/kernel/common/+/53afb231f54a69d827b882fa282b30bb10cb08a5)] [[3](https://android.googlesource.com/kernel/common/+/d3c17d5e271ab688cb117330ec85e125ebf24d88)] | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[b4604acd52a691c2fd33ad0a0fafb7cc19dee5de - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/b4604acd52a691c2fd33ad0a0fafb7cc19dee5de)

### CVE-2021-39686

| CVE-2021-39686 | A-200688826``[Upstream kernel](https://android.googlesource.com/kernel/common/+/d49297739550) [[2](https://android.googlesource.com/kernel/common/+/3af7a2f61023)] [[3](https://android.googlesource.com/kernel/common/+/11db2de0af2a)] [[4](https://android.googlesource.com/kernel/common/+/a4eacf3227bd)] | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[d49297739550 - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/d49297739550)

### CVE-2021-39698

| CVE-2021-39698 | A-185125206``[Upstream kernel](https://android.googlesource.com/kernel/common/+/42288cb44c4b) [[2](https://android.googlesource.com/kernel/common/+/a880b28a71e3)] [[3](https://android.googlesource.com/kernel/common/+/9537bae0da1f)] [[4](https://android.googlesource.com/kernel/common/+/363bee27e258)] [[5](https://android.googlesource.com/kernel/common/+/50252e4b5e98)] | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[42288cb44c4b - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/42288cb44c4b)

### CVE-2021-3655

| CVE-2021-3655 | A-197154735``[Upstream kernel](https://android.googlesource.com/kernel/common/+/d4dbef7046e2) [[2](https://android.googlesource.com/kernel/common/+/6ef81a5c0e22)] [[3](https://android.googlesource.com/kernel/common/+/ffca46766850)] [[4](https://android.googlesource.com/kernel/common/+/ccb79116c372)] | ID | High |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -- | ---- |

[d4dbef7046e2 - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/d4dbef7046e2)

## MediaTek components

### CVE-2022-20047

| CVE-2022-20047 | A-213120685``M-ALPS05917489[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| -------------- | --------------------------------------------------------------------------------------------- | ---- |

In video decoder, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

### CVE-2022-20048

| CVE-2022-20048`` | A-213116796``M-ALPS05917502[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| ---------------- | --------------------------------------------------------------------------------------------- | ---- |

In video decoder, there is a possible out of bounds write due to a missing bounds check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

### CVE-2022-20053

| CVE-2022-20053 | A-213120689``M-ALPS06219097[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| -------------- | --------------------------------------------------------------------------------------------- | ---- |

In ims service, there is a possible escalation of privilege due to a missing permission check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

## Qualcomm components

### CVE-2021-35088

| CVE-2021-35088 | A-204905738``[QC-CR#3007473](https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=6196d775c367df4dca39bf5c20546058bd4b6cc6) | High | WLAN |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |

[platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=6196d775c367df4dca39bf5c20546058bd4b6cc6)

### CVE-2021-35103

| CVE-2021-35103`` | A-209481110``[QC-CR#3033509](https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=dce054909b432773df3d1c8c4230bad7f12a2b45) | High | WLAN |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |

[platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=dce054909b432773df3d1c8c4230bad7f12a2b45)

### CVE-2021-35105

| CVE-2021-35105`` | A-209469958``[QC-CR#3034743](https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=c1c8190946b55edf536ec53432ebb94257280a2a) [[2](https://source.codeaurora.org/quic/la/kernel/msm-3.18/commit/?id=a134f476741492666ac75fd9dc14ed0f9d589d6e)] | High | Display |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------- |

[kernel/msm-4.9 - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=c1c8190946b55edf536ec53432ebb94257280a2a)

### CVE-2021-35106

| CVE-2021-35106`` | A-209481028``[QC-CR#3035196](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=5f44ff8a5b375fec9361bd460856f5e02b8b7746) [[2](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=e17be617ae39e9e9520d0bc65d2c4e08c7697267)] | High | WLAN |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ---- |

[platform/vendor/qcom-opensource/wlan/qcacld-3.0 - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=5f44ff8a5b375fec9361bd460856f5e02b8b7746)

### CVE-2021-35117

| CVE-2021-35117`` | A-209481202``[QC-CR#3028360](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=ef0f64fb81401bd7ea71d05f9416c57c3ab7937d) | High | WLAN |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |

[platform/vendor/qcom-opensource/wlan/qcacld-3.0 - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=ef0f64fb81401bd7ea71d05f9416c57c3ab7937d)

## Qualcomm closed-source components

### CVE-2021-1942

| CVE-2021-1942`` | A-199191104[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | Critical |
| --------------- | ----------------------------------------------------------------------------- | -------- |

Improper handling of permissions of a shared memory region can lead to memory corruption

### CVE-2021-35110

| CVE-2021-35110 | A-209469768[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | Critical |
| -------------- | ----------------------------------------------------------------------------- | -------- |

Possible buffer overflow to improper validation of hash segment of file while allocating memory

### CVE-2021-1950

| CVE-2021-1950`` | A-199191539[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| --------------- | ----------------------------------------------------------------------------- | ---- |

Improper cleaning of secure memory between authenticated users can lead to face authentication bypass

### CVE-2021-30328

| CVE-2021-30328 | A-199191341[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible assertion due to improper validation of invalid NR CSI-IM resource configuration

### CVE-2021-30329

| CVE-2021-30329`` | A-199191831[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| ---------------- | ----------------------------------------------------------------------------- | ---- |

Possible assertion due to improper validation of TCI configuration

### CVE-2021-30332

| CVE-2021-30332`` | A-199190643[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| ---------------- | ----------------------------------------------------------------------------- | ---- |

Possible assertion due to improper validation of OTA configuration

### CVE-2021-30333

| CVE-2021-30333 | A-199191889[*](https://source.android.com/security/bulletin/2022-03-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Improper validation of buffer size input to the EFS file can lead to memory corruption

## Google Play system updates

### CVE-2021-39694

In parse of RoleParser.java, there is a possible way for default apps to get permissions explicitly denied by the user due to a permissions bypass. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation
