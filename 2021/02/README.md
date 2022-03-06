## framework

### CVE-2021-0341 ID High

In verifyHostName of OkHostnameVerifier.java, there is a possible way to accept a certificate for the wrong domain due to improperly used crypto. This could lead to remote information disclosure with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-8.1 Android-9 Android-10 Android-11Android ID: A-171980069

### CVE-2021-0302 EoP High

tapjacking

### CVE-2021-0305 EoP High

tapjacking

### CVE-2021-0314 EoP High

UI problem

### CVE-2021-0327 EoP High

activityManagerService.java

### *CVE-2021-0330 EoP High

proto_loaded is not thread safe, so we must protect it with
a mutex proto_lock.

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### CVE-2021-0334 EoP High

Bug: 163358811

### CVE-2021-0337 EoP High

When the file is deleted, renamed or moved, revoke all uri
permissions with the file

### CVE-2021-0339 EoP High

For security reason, we also need to restrict app transition animation
duration as 3 secs to prevent malicious app may set a long duration or
infinity repeat counts through ActivityOption#makeCustomAnimation or
Activity#overridePendingTransition with custom animation set.

Bug: 145728687

### CVE-2021-0340 EoP High

Interge Overflow.

### CVE-2021-0338 Eop High

fix font size scale validator????

### CVE-2021-0325 RCE High

first_mb_in_slice shouldn't be >= mbs in the picture. Bug in libavc

### CVE-2021-0332 EoP High

May be a UAF in surfaceflinger.

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### CVE-2021-0335 ID High

Bug in stagefright.

### CVE-2021-0326 RCE Critical

error in wpa

### CVE-2021-0328 EoP High

Permission check in bluetooth app.

### CVE-2021-0329 EoP High

bluetooth app
Check if advertiserId value matches valid advertiser

Passing non-existing advertiserId can result in OOB

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### *CVE-2021-0331 EoP High

Prevent non-system overlays from showing over notification listener consent dialog
src/com/android/settings/notification/NotificationAccessConfirmationActivity.java
In onCreate of NotificationAccessConfirmationActivity.java, there is a possible overlay attack due to an insecure default value. This could lead to local escalation of privilege and notification access with User execution privileges needed. User interaction is needed for exploitation

### *CVE-2021-0333 EoP High

Prevent overlay drawing on top of Bluetooth activity dialog
src/com/android/settings/bluetooth/BluetoothPermissionActivity.java
`SYSTEM_FLAG_HIDE_NON_SYSTEM_OVERLAY_WINDOWS`

### *CVE-2021-0336 EoP High

Add bluetooth package to permission request intent

Limit the component that may resolve this intent to the
bluetooth package.

## kernel

### *CVE-2017-18509 EoP High

https://github.com/torvalds/linux/commit/99253eb750fda6a644d5188fb26c43bad8d5a745

### CVE-2020-11272 Cirtal

uaf in wlan0

### CVE-2020-11271 High

maybe race condition in audio

### CVE-2020-11277 High

Camera

### CVE-2020-11282 High

permission

### CVE-2020-11286 Hgih

/drivers/usb/dwc3/ep0.c

### CVE-2020-11297 High

https://source.codeaurora.org/quic/la/platform/vendor/qcom-opensource/wlan/qcacld-3.0/commit/?id=2a10c7aa8cdd3277e35176207c44ade90a567e73

### Qualcomm closed-source components

CVE-2020-11163	A-162751928*		Critical	Closed-source component
CVE-2020-11170	A-162753079*		Critical	Closed-source component
CVE-2020-11177	A-162755362*		High	Closed-source component
CVE-2020-11180	A-168050602*		High	Closed-source component
CVE-2020-11187	A-162755638*		High	Closed-source component
CVE-2020-11253	A-168722706*		High	Closed-source component
CVE-2020-11269	A-172348983*		High	Closed-source component
CVE-2020-11270	A-172349024*		High	Closed-source component
CVE-2020-11275	A-172348985*		High	Closed-source component
CVE-2020-11276	A-172349003*		High	Closed-source component
CVE-2020-11278	A-172349045*		High	Closed-source component
CVE-2020-11280	A-172348987*		High	Closed-source component
CVE-2020-11281	A-161714839*		High	Closed-source component
CVE-2020-11283	A-168918306*		High	Closed-source component
CVE-2020-11287	A-172348989*		High	Closed-source component
CVE-2020-11296	A-172348729*		High	Closed-source component
