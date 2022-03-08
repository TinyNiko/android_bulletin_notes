# Framework

## Framework

### CVE-2021-39619

| CVE-2021-39619 | [A-197399948](https://android.googlesource.com/platform/frameworks/base/+/a70c46b8a5ac697c87017f9c3fdebb03d3cc0292) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |

[a70c46b8a5ac697c87017f9c3fdebb03d3cc0292 - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/a70c46b8a5ac697c87017f9c3fdebb03d3cc0292)

### CVE-2021-39663

| CVE-2021-39663 | A-200682135[*](https://source.android.com/security/bulletin/2022-02-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

In openFileAndEnforcePathPermissionsHelper of MediaProvider.java, there is a possible bypass of a permissions check due to a confused deputy. This could lead to local escalation of privilege with User execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-10Android ID: A-200682135

### * CVE-2021-39676

| CVE-2021-39676 | A-197228210[*](https://source.android.com/security/bulletin/2022-02-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

In writeThrowable of AndroidFuture.java, there is a possible parcel serialization/deserialization mismatch due to improper input validation. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-11Android ID: A-197228210

### * CVE-2021-39664

| CVE-2021-39664 | [A-203938029](https://android.googlesource.com/platform/frameworks/base/+/18c66d8fee0e0dd8681182a59b59119a21e09c0c) | ID | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | -- | ---- |

```cpp
  if (!lib_alias) {
+          LOG(ERROR) << "RES_TABLE_STAGED_ALIAS_TYPE is too small.";
+          return {};
+        }
+        if ((child_chunk.data_size() / sizeof(ResTable_staged_alias_entry))
+            < dtohl(lib_alias->count)) {
+          LOG(ERROR) << "RES_TABLE_STAGED_ALIAS_TYPE is too small to hold entries.";
           return {};
         }
```

[18c66d8fee0e0dd8681182a59b59119a21e09c0c - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/18c66d8fee0e0dd8681182a59b59119a21e09c0c)

## Media Framework

### CVE-2020-13112

| CVE-2020-13112 | A-194342672[*](https://source.android.com/security/bulletin/2022-02-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

An issue was discovered in libexif before 0.6.22. Several buffer over-reads in EXIF MakerNote handling could lead to information disclosure and crashes. This is different from CVE-2020-0093.

### CVE-2020-13113

| CVE-2020-13113 | A-196085005[*](https://source.android.com/security/bulletin/2022-02-01#asterisk) | EoP | High |
| -------------- | ----------------------------------------------------------------------------- | --- | ---- |

An issue was discovered in libexif before 0.6.22. Use of uninitialized memory in EXIF Makernote handling could lead to crashes and potential use-after-free conditions.

### CVE-2021-39665

| CVE-2021-39665 | [A-204077881](https://android.googlesource.com/platform/frameworks/av/+/d0e524f58873f81549c7abfade30d8c9d2406a1c) | ID | High |
| -------------- | -------------------------------------------------------------------------------------------------------------- | -- | ---- |

OOB write.

[Diff - d0e524f58873f81549c7abfade30d8c9d2406a1c^! - platform/frameworks/av - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/av/+/d0e524f58873f81549c7abfade30d8c9d2406a1c%5E%21/#F0)

### CVE-2021-39666

| CVE-2021-39666 | [A-204445255](https://android.googlesource.com/platform/frameworks/av/+/1b3b20e3ffbee16770c382d14ecbc4ec28cea88d) [[2](https://android.googlesource.com/platform/frameworks/av/+/fc120151250f8627b34e72ea3b01060bd9819c22)] | ID | High |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -- | ---- |

[Diff - 1b3b20e3ffbee16770c382d14ecbc4ec28cea88d^! - platform/frameworks/av - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/av/+/1b3b20e3ffbee16770c382d14ecbc4ec28cea88d%5E%21/#F0)

## System

### * CVE-2021-39675

| CVE-2021-39675 | [A-205729183](https://android.googlesource.com/platform/system/nfc/+/fef77a189022aa7ac53136e582a1444b1d2ef5f0) | EoP | Critical |
| -------------- | ----------------------------------------------------------------------------------------------------------- | --- | -------- |

[Diff - fef77a189022aa7ac53136e582a1444b1d2ef5f0^! - platform/system/nfc - Git at Google (googlesource.com)](https://android.googlesource.com/platform/system/nfc/+/fef77a189022aa7ac53136e582a1444b1d2ef5f0%5E%21/#F0)

### * CVE-2021-39668

| CVE-2021-39668 | [A-193445603](https://android.googlesource.com/platform/frameworks/base/+/f84fdf2e6a98b81c7b55517227bd4cb53318d5aa) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------------- | --- | ---- |


```
Controls - Do not recreate intent

Recreating the control's intent in SystemUI can be exploited to launch
Intent's with SystemUI's privileges, rather than what is limited to
the application. Use the fillInIntent parameter to supply additional
parameters to the application.
```

Maybe a PendingIntentProblem

[f84fdf2e6a98b81c7b55517227bd4cb53318d5aa - platform/frameworks/base - Git at Google (googlesource.com)](https://android.googlesource.com/platform/frameworks/base/+/f84fdf2e6a98b81c7b55517227bd4cb53318d5aa)

### * CVE-2021-39669

| CVE-2021-39669 | [A-196969991](https://android.googlesource.com/platform/packages/apps/Settings/+/3dd874316af29ccd08d99dfea672ccd8a5d06452) | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------- | --- | ---- |

```
What is SYSTEM_FLAG_HIDE_NON_SYSTEM_OVERLAY_WINDOWS
```

[Diff - 3dd874316af29ccd08d99dfea672ccd8a5d06452^! - platform/packages/apps/Settings - Git at Google (googlesource.com)](https://android.googlesource.com/platform/packages/apps/Settings/+/3dd874316af29ccd08d99dfea672ccd8a5d06452%5E%21/#F0)

### CVE-2021-39671

| CVE-2021-39671 | [A-206718630](https://android.googlesource.com/platform/system/tools/aidl/+/dd0d78f0ead984881caee291751226001f92587e) [[2](https://android.googlesource.com/platform/system/tools/aidl/+/3f4f24f1fc01aabae8253eb041c6cb236e54402b)] | EoP | High |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | ---- |

[dd0d78f0ead984881caee291751226001f92587e - platform/system/tools/aidl - Git at Google (googlesource.com)](https://android.googlesource.com/platform/system/tools/aidl/+/dd0d78f0ead984881caee291751226001f92587e)

### * CVE-2021-39674

| CVE-2021-39674 | [A-201083442](https://android.googlesource.com/platform/system/bt/+/eeefcc7c75af2f41caba0de0175d3d843c4e882f) | EoP | High |
| -------------- | ---------------------------------------------------------------------------------------------------------- | --- | ---- |

UAF in bt

[eeefcc7c75af2f41caba0de0175d3d843c4e882f - platform/system/bt - Git at Google (googlesource.com)](https://android.googlesource.com/platform/system/bt/+/eeefcc7c75af2f41caba0de0175d3d843c4e882f)

### *CVE-2021-0706

| CVE-2021-0706 | A-193444889[*](https://source.android.com/security/bulletin/2022-02-01#asterisk) | DoS | High |
| ------------- | ----------------------------------------------------------------------------- | --- | ---- |

In startListening of PluginManagerImpl.java, there is a possible way to disable arbitrary app components due to a missing permission check. This could lead to local denial of service with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-10 Android-11Android ID: A-193444889

This bug is interesting.

[CVE_2021_0706.java - Android Code Search](https://cs.android.com/android/platform/superproject/+/master:cts/hostsidetests/securitybulletin/src/android/security/cts/CVE_2021_0706.java;l=41?q=193444889&hl=zh-cn)

# Kernel

## System

### CVE-2021-39631

## Amlogic components

### CVE-2021-39672

## MTK

### CVE-2022-20024

### CVE-2022-20025

### CVE-2022-20026

### CVE-2022-20027

### CVE-2022-20028

## Unisoc

### CVE-2021-39616

### CVE-2021-39635

### CVE-2021-39658

## Qualcomm

### CVE-2021-35068

### CVE-2021-35069

### CVE-2021-35074

### CVE-2021-35075

### CVE-2021-35077

## Qualcomm closed-source

### CVE-2021-30317

### CVE-2021-30309

### CVE-2021-30318

### CVE-2021-30322

### CVE-2021-30323

### CVE-2021-30326
