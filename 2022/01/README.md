# Framework

## Framework

### CVE-2021-39630

| CVE-2021-39630 | [A-202768292](https://android.googlesource.com/platform/frameworks/base/+/b2dc041a4e84986e3a6932b127d3a18ef02b6d0a) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

Shell uid can create Fabricated Overlay which can only used by system apps and root

[zacharee/FabricateOverlay (github.com)](https://github.com/zacharee/FabricateOverlay)

[Diff - b2dc041a4e84986e3a6932b127d3a18ef02b6d0a^! - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/b2dc041a4e84986e3a6932b127d3a18ef02b6d0a%5E%21/#F0)

### CVE-2021-39632

| CVE-2021-39632 | [A-202159709](https://android.googlesource.com/platform/bootable/recovery/+/f0a760b3a154ad328c682ec8559287befff14945) | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------ | --- | ---- |

OOB write in events.cpp (Recovery mode), write \0 at the end of pevent->name, but how to trigger/exploit it?

```cpp
-    pevent->name[pevent->len] = '\0';
-    if (strncmp(pevent->name, "event", 5)) {
+    std::string event_name(pevent->name, pevent->len);
+    if (!android::base::StartsWith(event_name, "event")) {
       continue;
     }
```

[Diff - f0a760b3a154ad328c682ec8559287befff14945^! - platform/bootable/recovery - Git at Google (googlesource.com)](https://android.googlesource.com/platform/bootable/recovery/+/f0a760b3a154ad328c682ec8559287befff14945%5E%21/#F0)

### CVE-2020-0338

| CVE-2020-0338 | [A-123700107](https://android.googlesource.com/platform/frameworks/base/+/6ebf410b818c6a525130d5fcb72381217fec8e7a) | ID | High |
| ------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |

[Diff - 6ebf410b818c6a525130d5fcb72381217fec8e7a^! - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/6ebf410b818c6a525130d5fcb72381217fec8e7a%5E%21/#F0)

## Media Framework

### CVE-2021-39623

| CVE-2021-39623 | [A-194105348](https://android.googlesource.com/platform/frameworks/av/+/5753afcd4c87f5566f4014cce1cbc8d767572331) | EoP | High |
| -------------- | -------------------------------------------------------------------------------------------------------------- | --- | ---- |

OOB write in SimpleDecodingSource.cpp. This is a memcpy problem find by OPPO.

```cpp
-                    memcpy(in_buffer->base() + cpLen, &numPageSamples, sizeof(numPageSamples));
+                    if (cpLen + sizeof(numPageSamples) <= in_buffer->capacity()) {
+                        memcpy(in_buffer->base() + cpLen, &numPageSamples, sizeof(numPageSamples));
+                        cpLen += sizeof(numPageSamples);
+                    } else {
+                        ALOGW("Didn't have enough space to copy kKeyValidSamples");
+                    }
```

[Diff - 5753afcd4c87f5566f4014cce1cbc8d767572331^! - platform/frameworks/av - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/av/+/5753afcd4c87f5566f4014cce1cbc8d767572331%5E%21/#F0)

## System

### CVE-2021-39618

| CVE-2021-39618 | A-196855999[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

In multiple methods of EuiccNotificationManager.java, there is a possible way to `install existing packages without user consent due to an unsafe PendingIntent`. This could lead to local escalation of privilege with User execution privileges needed. User interaction is not needed for exploitation

### CVE-2021-39620

| CVE-2021-39620 | [A-203847542](https://android.googlesource.com/platform/frameworks/native/+/f2e0a95700a937e421647623a60c9fc01d6e5d87) | EoP | High |
| -------------- | ------------------------------------------------------------------------------------------------------------------ | --- | ---- |

[f2e0a95700a937e421647623a60c9fc01d6e5d87 - platform/frameworks/native - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/native/+/f2e0a95700a937e421647623a60c9fc01d6e5d87)

### CVE-2021-39621

| CVE-2021-39621 | [A-185126319](https://android.googlesource.com/platform/packages/apps/Dialer/+/9c452d9f25d8fb41fd3ec627293a2481fde778d4) | EoP | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | --- | ---- |

PendingIntent problem.

[9c452d9f25d8fb41fd3ec627293a2481fde778d4 - platform/packages/apps/Dialer - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Dialer/+/9c452d9f25d8fb41fd3ec627293a2481fde778d4)

### CVE-2021-39622

| CVE-2021-39622 | A-192663648[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

In GBoard, there is a possible way to bypass Factory Reset Protection due to a missing permission check. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

What' s GBoard?

### CVE-2021-39625

| CVE-2021-39625 | A-194695347[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

In showCarrierAppInstallationNotification of EuiccNotificationManager.java, there is a possible way to gain an access to MediaProvider content due to an unsafe PendingIntent. This could lead to local escalation of privilege with User execution privileges needed. User interaction is needed for exploitation.

PendingIntent Again?

### CVE-2021-39626

| CVE-2021-39626 | [A-194695497](https://android.googlesource.com/platform/packages/apps/Settings/+/3f280c15b1808a94acd3ce2c4145c74e6f183855) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |

Fix make Bluetooth discoverable without additional permission

[3f280c15b1808a94acd3ce2c4145c74e6f183855 - platform/packages/apps/Settings - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Settings/+/3f280c15b1808a94acd3ce2c4145c74e6f183855)

### CVE-2021-39627

| CVE-2021-39627 | [A-185126549](https://android.googlesource.com/platform/packages/apps/Dialer/+/9c452d9f25d8fb41fd3ec627293a2481fde778d4) | EoP | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | --- | ---- |

PendingIntent problem?

[9c452d9f25d8fb41fd3ec627293a2481fde778d4 - platform/packages/apps/Dialer - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Dialer/+/9c452d9f25d8fb41fd3ec627293a2481fde778d4)

### CVE-2021-39629

| CVE-2021-39629 | [A-197353344](https://android.googlesource.com/platform/hardware/nxp/nfc/+/63162916491d3ad034e0288fb2e254cf2b66db92) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------- | --- | ---- |

Use after free in phTmlNfc_TmlThread.

How to fuzz NFC.

[Diff - 63162916491d3ad034e0288fb2e254cf2b66db92^! - platform/hardware/nxp/nfc - Git at Google (googlesource.com)](https://android.googlesource.com/platform/hardware/nxp/nfc/+/63162916491d3ad034e0288fb2e254cf2b66db92%5E%21/#F0)

### CVE-2021-0643

| CVE-2021-0643 | [A-183612370](https://android.googlesource.com/platform/frameworks/opt/telephony/+/f6bb9b20840c29e74a37ea2b880e63b3fc9470ff) | ID | High |
| ------------- | ------------------------------------------------------------------------------------------------------------------------- | -- | ---- |

ID in telephony module.

[Diff - f6bb9b20840c29e74a37ea2b880e63b3fc9470ff^! - platform/frameworks/opt/telephony - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/opt/telephony/+/f6bb9b20840c29e74a37ea2b880e63b3fc9470ff%5E%21/#F0)

### CVE-2021-39628

| CVE-2021-39628 | [A-189575031](https://android.googlesource.com/platform/frameworks/base/+/b34e3b0cb7d0d5227e845a05fe58d3e286348a7a) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |

[b34e3b0cb7d0d5227e845a05fe58d3e286348a7a - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/b34e3b0cb7d0d5227e845a05fe58d3e286348a7a)

### CVE-2021-39659

| CVE-2021-39659 | [A-208267659](https://android.googlesource.com/platform/packages/services/Telecomm/+/f1cae30e2c9837d1587a3a732bcc9398bd1f9e63) | DoS | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

Fix the integer overflow/underflow caused by sorting of duplicate phoneaccounts during emergency call attempt.

[f1cae30e2c9837d1587a3a732bcc9398bd1f9e63 - platform/packages/services/Telecomm - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/services/Telecomm/+/f1cae30e2c9837d1587a3a732bcc9398bd1f9e63)

# kernel

## Android Runtime

### CVE-2021-0959

| CVE-2021-0959 | A-200284993 | EoP | High |
| ------------- | ----------- | --- | ---- |

In jit_memory_region.cc, there is a possible bypass of memory restrictions due to a logic error in the code. This could lead to local escalation of privilege with User execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-12Android ID: A-200284993.

[jit_memory_region.cc - Android Code Search](https://cs.android.com/android/platform/superproject/+/master:art/runtime/jit/jit_memory_region.cc;l=76?q=200284993&sq=&hl=zh-cn)

## kernel components

### CVE-2021-39634

| CVE-2021-39634 | A-204450605``[Upstream kernel](https://android.googlesource.com/kernel/common/+/f8d4f44df056c5b504b0d49683fb7279218fd207) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[Diff - f8d4f44df056c5b504b0d49683fb7279218fd207^! - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/f8d4f44df056c5b504b0d49683fb7279218fd207%5E%21/#F0)

### CVE-2021-39633

| CVE-2021-39633 | A-150694665``[Upstream kernel](http://android.googlesource.com/kernel/common/+/1d011c4803c72f3907eccfc1ec63caefb852fcbf) | ID | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | -- | ---- |

[Diff - 1d011c4803c72f3907eccfc1ec63caefb852fcbf^! - kernel/common - Git at Google (googlesource.com)](https://android.googlesource.com/kernel/common/+/1d011c4803c72f3907eccfc1ec63caefb852fcbf%5E%21/#F0)

## MTK

### CVE-2021-31345

### CVE-2021-31346

### CVE-2021-31890

### CVE-2021-40148

### CVE-2021-31889

I can't find useful infomation for mtk bugs.

## Unisoc

### CVE-2021-1049

reported from hackerone

## Qualcomm

### CVE-2021-30319

| CVE-2021-30319 | A-202025735``[QC-CR#2960714](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=c3baa174ab2cafb6b65ba34d935eb24e56609cd3) | High |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |

bufferoverflow in wma

```cpp
-	if (p2p_ie_len)
+
+	if (tmpl_len > WMI_BEACON_TX_BUFFER_SIZE) {
+		wma_err("tmpl_len: %d > %d. Invalid tmpl len", tmpl_len,
+			WMI_BEACON_TX_BUFFER_SIZE);
+		return -EINVAL;
+	}
+
+	if (p2p_ie_len) {
+		if (tmpl_len <= p2p_ie_len) {
+			wma_err("tmpl_len %d <= p2p_ie_len %d, Invalid",
+				tmpl_len, p2p_ie_len);
+			return -EINVAL;
+		}
 		tmpl_len -= (uint32_t) p2p_ie_len;
+	}
+

```

[platform/vendor/qcom-opensource/wlan/qcacld-3.0 - Unnamed repository (codeaurora.org)](https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=c3baa174ab2cafb6b65ba34d935eb24e56609cd3)

### CVE-2021-30353

| CVE-2021-30353 | A-202025599``[QC-CR#2993069](https://source.codeaurora.org/quic/le/platform/hardware/qcom/audio/commit/?id=af30f0103a50df510a71a12047b5c68b4e3b8a72) [[2](https://source.codeaurora.org/quic/le/platform/hardware/qcom/audio/commit/?id=37a434f57bddfad4544102c4d15f93120bbac71d)] | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |

[platform/hardware/qcom/audio - Unnamed repository; edit this file &#39;description&#39; to name the repository. (codeaurora.org)](https://source.codeaurora.org/quic/le/platform/hardware/qcom/audio/commit/?id=af30f0103a50df510a71a12047b5c68b4e3b8a72)

### CVE-2021-30313

Use After Free in Wired Connectivity

Use after free condition can occur in wired connectivity due to a race condition while creating and deleting folders


## Qualcomm closed-source

### CVE-2021-30285

| [CVE-2021-30285](https://www.qualcomm.com/company/product-security/bulletins/january-2022-bulletin#_cve-2021-30285) | Critical | Critical | KERNEL |
| ---------------------------------------------------------------------------------------------------------------- | -------- | -------- | ------ |

Improper validation of memory region in Hypervisor can lead to incorrect region mapping

### CVE-2021-30287

| CVE-2021-30287 | A-193070556[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible assertion due to improper validation of symbols configured for PDCCH monitoring

### CVE-2021-30300

| CVE-2021-30300 | A-193071116[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible denial of service due to incorrectly decoding hex data for the SIB2 OTA message and assigning a garbage value to choice when processing the SRS configuration

### CVE-2021-30301

| CVE-2021-30301 | A-193070342[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible denial of service due to out of memory while processing RRC and NAS OTA message

### CVE-2021-30307

| CVE-2021-30307 | A-193070700[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible denial of service due to improper validation of DNS response when DNS client requests with PTR, NAPTR or SRV query type

### CVE-2021-30308

| CVE-2021-30308 | A-193070594[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Buffer Copy Without Checking Size of Input in Modem

Possible buffer overflow while printing the HARQ memory partition detail due to improper validation of buffer size

### CVE-2021-30311

| CVE-2021-30311 | A-193070557[*](https://source.android.com/security/bulletin/2022-01-01#asterisk) | High |
| -------------- | ----------------------------------------------------------------------------- | ---- |

Possible heap overflow due to lack of index validation before allocating and writing to heap buffer

### CVE-2021-30330

Possible null pointer dereference due to improper validation of APE clip

### CVE-2021-30314

Lack of validation for third party application accessing the service can lead to information disclosure
