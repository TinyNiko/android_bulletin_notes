# android_bulletin_notes

# 2021。04


# 2021.03

## framework

### `CVE-2021-0395`: EoP High
UAF In StopServicesAndLogViolations of reboot.cpp. In reboot, it will stop services, but if services is already died, it's will cause UAF.

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### `CVE-2021-0391`: Eop High

Protect account chooser activities against overlay.
UI hijack in core/java/android/accounts/ChooseAccountActivity
7h0r

### `CVE-2021-0398`： Eop High

Pass original callingPid and callingUid into
shouldAllowWhileInUsePermissionInFgsLocked() after
Binder.clearCallingIdentity().

Michał Bednarski (michalbednarski)


### `*CVE-2021-0397`: RCE Critical

/bta/ag/bta_ag_sdp.cc 

if p_disc_db != nullptr ， it will reassign a addr which may cause a AAW

```c 
if (p_scb->p_disc_db != nullptr) {
    android_errorWriteLog(0x534e4554, "174052148");
    APPL_TRACE_ERROR("Discovery already in progress... returning.");
    return;
  }
  /* allocate buffer for sdp database */
  p_scb->p_disc_db = (tSDP_DISCOVERY_DB*)osi_malloc(BTA_AG_DISC_BUF_SIZE);
  /* set up service discovery database; attr happens to be attr_list len */
  if (SDP_InitDiscoveryDb(p_scb->p_disc_db, BTA_AG_DISC_BUF_SIZE, num_uuid,
                          uuid_list, num_attr, attr_list)) {
    if (SDP_ServiceSearchAttributeRequest(
            p_scb->peer_addr, p_scb->p_disc_db,
            bta_ag_sdp_cback_tbl[bta_ag_scb_to_idx(p_scb) - 1])) {
      return;
    } else {
      LOG(ERROR) << __func__ << ": failed to start SDP discovery for "
                 << p_scb->peer_addr;
    }
```

Fei, Wenwen Wang, and Cusas of L.O.Team

### CVE-2017-14491: REC High

heap overflow in dnsmasq, third party

Fix heap overflow in DNS code. This is a potentially serious
security hole. It allows an attacker who can make DNS
requests to dnsmasq, and who controls the contents of
a domain, which is thereby queried, to overflow
(by 2 bytes) a heap buffer and either crash, or
even take control of, dnsmasq.


### * CVE-2021-0393： RCE High

v8 problem

https://bugs.chromium.org/p/chromium/issues/detail?id=914736

Qidan He (@flanker_hqd"

### * CVE-2021-0396: RCE High

Fix off-by-one in parameter count check 

https://bugs.chromium.org/p/chromium/issues/detail?id=902610

In Builtins::Generate_ArgumentsAdaptorTrampoline of builtins-arm.cc and related files, there is a possible out of bounds write due to an incorrect bounds check. This could lead to remote code execution in an unprivileged process with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android-8.1 Android-9 Android-10 Android-11Android ID: A-160610106

### CVE-2021-0390: EoP High

service/java/com/android/server/wifi/WifiConfigManager.java


Roshan Pius of Google

### * CVE-2021-0392: EoP High

Fix UAF problem in wificond

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### CVE-2021-0394: ID High

ID in NewStringUTF

Steven Moreland of Google

## kernel

### *CVE-2021-0399: EoP High

UAF 

In qtaguid_untag of xt_qtaguid.c, there is a possible memory corruption due to a use after free. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.Product: AndroidVersions: Android kernelAndroid ID: A-176919394References: Upstream kernel

### CVE-2020-11223
TODO

### CVE-2020-11290 High Drm

Add event to event_list after msm_register_event is successful to avoid
use-after-free vulnerability.

https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=1f383b13c485d9b2d083b01c0bda52641e2a83bd

360 Alpha Lab

### CVE-2020-11308 High Bootloader

QcomModulePkg: Buffer overflow maybe occur when convert string from ASCII to Unicode
The max size of ptn_name is 72, the max size of PartitionNameFromMeta is
36, it will cause the buffer overflow issue if the actual string size of
ptn_name is lager than 36 when covent string form ASCII to Unicore.

https://source.codeaurora.org/quic/le/abl/tianocore/edk2/commit/?id=c468f18421e113057ba72b83edf985c53fe4705d

Gengjia Chen ( @chengjia4574 ) of IceSword Lab, Qihoo 360 Technology Co. Ltd.

### CVE-2020-11309 High Display

Don't allow IOCTL_KGSL_MAP_USER_MEM to import user memory that was
already allocated and mapped by KGSL in the first place.  Remapping
memory never makes sense and it messes up reference counting in the
pools.

Jun Yao (姚俊) (@_2freeman) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### Qualcomm closed-source components

TODO how to find these issues

https://www.qualcomm.com/company/product-security/bulletins/march-2021-bulletin#_cve-2020-11192 

CVE-2020-11192  A-168050025*		Critical	Closed-source component
CVE-2020-11204	A-162750025*		Critical	Closed-source component
CVE-2020-11218	A-168049956*		Critical	Closed-source component
CVE-2020-11227	A-168050276*		Critical	Closed-source component
CVE-2020-11228	A-168050345*		Critical	Closed-source component
CVE-2020-11165	A-160605782*		High	Closed-source component
CVE-2020-11166	A-168051733*		High	Closed-source component
CVE-2020-11171	A-168050346*		High	Closed-source component
CVE-2020-11178	A-160605529*		High	Closed-source component
CVE-2020-11186	A-168049957*		High	Closed-source component
CVE-2020-11188	A-168050859*		High	Closed-source component
CVE-2020-11189	A-168051051*		High	Closed-source component
CVE-2020-11190	A-168051033*		High	Closed-source component
CVE-2020-11194	A-162756908*		High	Closed-source component
CVE-2020-11195	A-162756604*		High	Closed-source component
CVE-2020-11198	A-162756735*		High	Closed-source component
CVE-2020-11199	A-168050860*		High	Closed-source component
CVE-2020-11220	A-168050239*		High	Closed-source component
CVE-2020-11221	A-168051035*		High	Closed-source component
CVE-2020-11222	A-168050578*		High	Closed-source component
CVE-2020-11226	A-168050240*		High	Closed-source component
CVE-2020-11299	A-175038625*		High	Closed-source component

# 2021.02

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

###  Qualcomm closed-source components

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

# 2021.01

## framework

### * CVE-2021-0313 	DoS	Critical

minikin?
https://android.googlesource.com/platform/frameworks/minikin/+/ffb33bcf2520208166cb29f47c60add9c0e37349

### * CVE-2021-0303 	EoP	High

Grpc Graph - fix use after free

GrpcGraph initializes StreamSetObserver - which triggers a thread to
notify GrpcGraph of termination. If GrpcGraph is destroyed, this will
result in use after free. Fix this by enforcing that GrpcGraph object is
not destroyed before StreamSetObserver.

https://android.googlesource.com/platform/packages/services/Car/+/768c8bfbe91db71e11eae2c57fb678ff2a5bf15e

### CVE-2021-0306 * EoP	High

permission

https://android.googlesource.com/platform/frameworks/base/+/03da463b2a94c36e3b46f0a110ec43710b82d404

### CVE-2021-0307   EoP	High

permission
https://android.googlesource.com/platform/cts/+/a8a90255d43845e307b6d133c710b802dbece622

### * CVE-2021-0310 	EoP	High

libbinder: Add ClientCounterCallbackImpl to LazyServiceRegistrar

This extra layer of indirection below ClientCounterCallback fixes a shared pointer ownership issue between LazyServiceRegistrar and ServiceManager. It also allows for implementation changes (like this one) without changing headers and breaking VNDK.

https://android.googlesource.com/platform/frameworks/native/+/dc6cb05ebe2cefdce215d797a8e418ba26c8c86c


### CVE-2021-0315 	EoP	High

UI
Protect GrantCredentialsPermissionActivity against overlay.

https://android.googlesource.com/platform/frameworks/base/+/828fe0b915f30e22fec03dc1ed2e66220ceebd3e

### * CVE-2021-0317 	EoP	High

permisson 

https://android.googlesource.com/platform/frameworks/base/+/c4ce178c261e6a2dc1aa4c1e1d570f0efd980e47


### * CVE-2021-0318 	EoP	High

think how?

Prevent mEventCache UAF in SensorEventConnection

Since there is no check to see if SensorEventConnection has been
destroyed, the mEventCache pointer can still be used even after it
was freed.

https://android.googlesource.com/platform/frameworks/native/+/adb416ac460cb28ca03e7898bdd154b1d0f8c16b

### * CVE-2021-0319 	EoP	High
RESTRICT AUTOMERGE
Fix CDM package check

CDM was using a pckage check that returns a value intead of throwing,
resulting in failing to throw on querying other package's associations

https://android.googlesource.com/platform/frameworks/base/+/0c17049d39b5a8867f030f6f36433564140e124a

### * CVE-2021-0304 	ID	High

PendingIntent problem?
Mutable pending intents are a security risk. This change adds the
IMMUTABLE flag to all PendingIntents created in GlobalScreenshot.
https://android.googlesource.com/platform/frameworks/base/+/9f42cf00e94afc61eee1edbf5ecde11f6c38e37f

### * CVE-2021-0309 	ID	High

Ignore GrantCredentials call with unexpected calling uid.

Activity can be used only in two cases.
1) Calling uid matches uid grantee.
2) Calling uid is is system. This flow is used by getToken methods with
notifyAuthFailure=true.

https://android.googlesource.com/platform/frameworks/base/+/0b610a27ba60047842b9416dd0537c68f0dd22b2

### CVE-2021-0321 	ID	High

permission check?

* https://android.googlesource.com/platform/frameworks/base/+/b57d1409c52478d37f006145949be8b4591b9898

### * CVE-2021-0322   ID	High
Fix the issue provider can be wrong when requesting slice permission

SlicePermissionActivity reads provider_pkg from intent, which can be
modified at will. As a result user might see incorrect package name in
the dialog granting slice permission.
https://android.googlesource.com/platform/frameworks/base/+/a185996c829a159bb27446697329b01464ab3c03

### CVE-2019-9376   DoS	High

Check that Account Parcel has name and type.
https://android.googlesource.com/platform/frameworks/base/+/32e85796389f57e2539c28f9e670277ab610459a

### * CVE-2020-15999  RCE	Moderate

https://android.googlesource.com/platform/external/freetype/+/358c238408a1fdc357d9afef6811369a7701e004

### CVE-2016-6328 RCE	High

libexif

fixes some (not all) buffer overreads during decoding pentax makernote entries.

### * CVE-2021-0311 ID	High

Fix memory overflow in ESQueue

https://android.googlesource.com/platform/frameworks/av/+/8ea3bdb5ef11dad8e11a2c2cad34e91ad11657d0%5E%21/#F0

### CVE-2021-0312 ID	High
 
Fix potential overflow in WAV extractor

https://android.googlesource.com/platform/frameworks/av/+/bb460899b97f260e7ed556b578318b1133335e1c

### * CVE-2021-0316 RCE	Critical

Fix potential OOB write in libbluetooth?

https://android.googlesource.com/platform/system/bt/+/f328ab46d5419632aec221f95b186ec71077176e

https://android.googlesource.com/platform/system/bt/+/f328ab46d5419632aec221f95b186ec71077176e%5E%21/#F0

### CVE-2020-0471 EoP	High

???
https://android.googlesource.com/platform/system/bt/+/ca6b0a211eb39ba85eed60ea740c85d1122fc6bc%5E%21/#F0

### * CVE-2021-0308 EoP	High	

A maliciously formatted USB or SD Card device when inserted into an Android device could crash sgdisk. This crash occurs because sgdisk does does not validate the number of cyclic partitions, which leads to an integer underflow ultimately causing a negative indexed stack write.

Fix this by making sure the number of partitions don't go negative.

https://android.googlesource.com/platform/external/gptfdisk/+/6d369451868ce71618144c4f4bd645ae48f0d1c5

### CVE-2021-0320 ID	High

Make mIsDeviceLockedForUser synchronized.


## kernel 

### CVE-2020-10732 ID High

Uninitialized data in core dump.
https://android.googlesource.com/kernel/common/+/1d605416fb7175e1adf094251466caa52093b413

### CVE-2020-10766 ID High

Prevent rogue cross-process SSBD shutdown

### CVE-2020-10767 ID High

Avoid force-disabling IBPB based on STIBP and enhanced IBRS.

### CVE-2021-0301 High

MTK ged 

### *CVE-2020-11233 High 

Time of Check Time of Use Race Condition in Boot

https://source.codeaurora.org/quic/le/kernel/lk/commit/?id=d87aa073d641fd955330754008563549146235db

### CVE-2020-11239 High

Use after free issue when importing a DMA buffer by using the CPU address of the buffer due to attachment is not cleaned up properly
https://source.codeaurora.org/quic/la/kernel/msm-3.18/commit/?id=20e2434473b259b40b590099da9fbce02a37cc8a

### CVE-2020-11240 High

Memory corruption due to ioctl command size was incorrectly set to the size of a pointer and not enough storage is allocated for the copy of the user argument
https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=2e138f8bc21ac08898547d2320e11c073073216d

### CVE-2020-11250 High

Use after free due to race condition when reopening the device driver repeatedly
https://source.codeaurora.org/quic/la/kernel/msm-4.14/commit/?id=827c2fcadb0569bd94bdff386483fb404145687b


### CVE-2020-11261 High

Memory corruption due to improper check to return error when user application requests memory allocation of a huge size

https://source.codeaurora.org/quic/la/kernel/msm-4.19/commit/?id=b8d6a6665e15224b6913c48ac6641d6a9f42db61

### CVE-2020-11262 High
	
https://source.codeaurora.org/quic/la/kernel/msm-4.14/commit/?id=10527de01e5fb34139487a3bc4e4dbbfa97eae0e

A race between command submission and destroying the context can cause an invalid context being added to the list leads to use after free issue.


### Qualcomm closed-source components

CVE-2020-11134	A-170138862*		Critical	Closed-source component
CVE-2020-11182	A-168722721*		Critical	Closed-source component
CVE-2020-11126	A-170139227*		High	Closed-source component
CVE-2020-11159  A-170138666*		High	Closed-source component
CVE-2020-11181	A-168051034*		High	Closed-source component
CVE-2020-11235	A-170138866*		High	Closed-source component
CVE-2020-11238	A-170139099*		High	Closed-source component
CVE-2020-11241	A-170139229*		High	Closed-source component
CVE-2020-11260	A-168918332*		High	Closed-source component

# 2020.12

## framework

### *CVE-2020-0099 Eop High

UI
https://android.googlesource.com/platform/frameworks/base/+/d0746b46a5d8049a7105a16eb25c44810376527e

### * CVE-2020-0294 EoP High

Make WallpaperMS bind wallpaper component PendingIntent immutable.
https://android.googlesource.com/platform/frameworks/base/+/d4bd69cef05d379555418a8fe748ec94ff6bd6d0

### * CVE-2020-0440 EoP High

https://android.googlesource.com/platform/frameworks/base/+/11725e1206645e567cfdd70100d64d1e0a85180d

### * CVE-2020-0459 ID High

https://android.googlesource.com/platform/frameworks/opt/net/wifi/+/db04b29f0f6a96b19850fc17e23818855f800d61

### CVE-2020-0464 ID High

https://android.googlesource.com/platform/system/netd/+/e1ec3b167754930d4d87b48414f9d707554a02f0

### * CVE-2020-0467 ID High

vpn problem
https://android.googlesource.com/platform/frameworks/base/+/61b620ad4f773e86c03e0719ae24268babcc62a9

### *CVE-2020-0468 ID High

improve location check
https://android.googlesource.com/platform/frameworks/base/+/af35aa5ac57a8c7c4534d82d8cd6cfb4f049bbfe%5E%21/#F0

### * CVE-2020-0469 Dos High

https://android.googlesource.com/platform/frameworks/base/+/1a6f1fb402b96df561b9672aef1e4fce8a13de80

### *CVE-2020-0458 RCE Critical

In SPDIFEncoder::writeBurstBufferBytes and related methods of SPDIFEncoder.cpp, there is a possible out of bounds write due to an integer overflow. This could lead to remote code execution with no additional execution privileges needed.

https://android.googlesource.com/platform/system/media/+/4523a5863f7d8f449600e85e946cfdc9cff408b2

### *CVE-2020-0470 ID High

topsec 
libaom 

### CVE-2020-0460 ID High

https://android.googlesource.com/platform/packages/apps/KeyChain/+/ed1888ebc3888399ec5144491e43bf7d871028e5 


### CVE-2020-0463 ID High
interesting 
https://android.googlesource.com/platform/system/bt/+/938a5cd87c38bf35d15ffa3414c3a74faecb8bf8%5E%21/#F0

### CVE-2020-15802 ID High

https://android.googlesource.com/platform/system/bt/+/775a5e72b34b70ff92d61d8bcc47c6bde663f02e%5E%21/#F0

## kernel

### CVE-2020-0444 EoP	High

Kernel Audit System
In audit_free_lsm_field of auditfilter.c, there is a possible bad kfree due to a logic error in audit_data_to_entry. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation.

syzkaller, kernel fuzzer

### CVE-2020-0465 EoP	High

https://android.googlesource.com/kernel/common/+/35556bed836f

### CVE-2020-0466 EoP	High

In do_epoll_ctl and ep_loop_check_proc of eventpoll.c, there is a possible use after free due to a logic error. This could lead to local escalation of privilege with no additional execution privileges needed. User interaction is not needed for exploitation

https://android.googlesource.com/kernel/common/+/52c479697c9b

### Broadcom components

CVE-2020-0016 A-171413483 *		High	Broadcom middleware
CVE-2020-0019 A-171413798 *		High	Broadcom middleware

### MediaTek components

CVE-2020-0455 A-170372514 M-ALPS05324771 *		High	vcu
CVE-2020-0456 A-170378843 M-ALPS05304125 *		High	vcu
CVE-2020-0457 A-170367562 M-ALPS05304170 *		High	vcu

### * CVE-2020-11225 Critical	WLAN

Out of bound access in WLAN driver due to lack of validation of array length before copying into array
https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=fe1e85068c57d8c4e4557ed6b265ac6b9694c3a1


### *CVE-2020-11146 High	Kernel

HIOS

Out of bound write while copying data using IOCTL due to lack of check of array index received from user
https://source.codeaurora.org/quic/la/kernel/msm-4.14/commit/?id=a480ed6e37d2dc2c7f56371365cdac7d5358b50c

### CVE-2020-11167 High	Bluetooth

Integer overflow to Buffer Overflow Issue in Bluetooth Host
Memory corruption while calculating L2CAP packet length in reassembly logic when remote sends more data than expected
https://source.codeaurora.org/quic/le/platform/system/bt/commit/?id=cfdb42d512704965acd551b9ffb6de37aac51bf7
https://source.codeaurora.org/quic/la/platform/system/bt/commit/?id=a741d8d2f59b2a090694be71cd538c821cf95ce5

### CVE-2020-11185 High	WLAN

Use of Out-of-Range Pointer Offset in WLAN
Out of bound issue in WLAN driver while processing vdev responses from firmware due to lack of validation of data received from firmware
https://source.codeaurora.org/quic/qsdk/platform/vendor/qcom-opensource/wlan/qca-wifi-host-cmn/commit/?id=227ff6c08ac997241a5a0513ad25f89072096d02

### *CVE-2020-11217 High	Audio

Double Free
A possible double free or invalid memory access in audio driver while reading Speaker Protection parameters
https://source.codeaurora.org/quic/la/platform/vendor/opensource/audio-kernel/commit/?id=b8630beb74fab51dbb5b7c769fecfa9534d12b4a

### Qualcomm closed-source components

CVE-2020-3685 A-157905813 *		Critical	Closed-source component
CVE-2020-3686 A-157906329 *		Critical	Closed-source component
CVE-2020-3691 A-157906171 *		Critical	Closed-source component
CVE-2020-11136 A-157905860 *		Critical	Closed-source component
CVE-2020-11137 A-157905869 *		Critical	Closed-source component
CVE-2020-11138 A-157905657 *		Critical	Closed-source component
CVE-2020-11140 A-157906530 *		Critical	Closed-source component
CVE-2020-11143 A-157905814 *		Critical	Closed-source component
CVE-2020-11119 A-168051735 *		High	Closed-source component
CVE-2020-11139 A-157905659 *		High	Closed-source component
CVE-2020-11144 A-157906670 *		High	Closed-source component
CVE-2020-11145 A-157905870 *		High	Closed-source component
CVE-2020-11179 A-163548240 *		High	Closed-source component
CVE-2020-11197 A-168050278 *		High	Closed-source component
CVE-2020-11200 A-168049958 *		High	Closed-source component
CVE-2020-11212 A-168050603 *		High	Closed-source component
CVE-2020-11213 A-168050861 *		High	Closed-source component
CVE-2020-11214 A-168049138 *		High	Closed-source component
CVE-2020-11215 A-168049960 *		High	Closed-source component
CVE-2020-11216 A-168050579 *		High	Closed-source component


# 2020.11

## framework

## kernel

### mediaTek

CVE-2020-0445 A-168264527 M-ALPS05253566 *		High	video encoder
CVE-2020-0446 A-168264528 M-ALPS05257259* M-ALPS05316810*		High	video decoder
CVE-2020-0447 A-168251617 M-ALPS05287879 *		High	ptp3

### Qualcomm closed-source components

CVE-2020-3639 A-155653490 *		Critical	Closed-source component
CVE-2020-3632 A-155652696 *		High	Closed-source component
CVE-2020-11123 A-155652382 *		High	Closed-source component
CVE-2020-11127 A-155653795 *		High	Closed-source component
CVE-2020-11168 A-162756122 *		High	Closed-source component
CVE-2020-11175 A-162756020 *		High	Closed-source component
CVE-2020-11184 A-162756352 *		High	Closed-source component
CVE-2020-11193 A-162756585 *		High	Closed-source component
CVE-2020-11196 A-162756960 *		High	Closed-source component
CVE-2020-11205 A-162757240 *		High	Closed-source component

# 2020.10

## framework

### * CVE-2020-0408 EoP High

string16 bug
https://android.googlesource.com/platform/system/core/+/4048e49956a2dfd49af3adf0f78881bf15f3550f%5E%21/#F0

### * CVE-2020-0420 EoP High

setUpdatableDriverPath should only be called by system_server and
developer driver path needs to be protected by a lock.

### * CVE-2020-0421 EoP High

string 8
https://android.googlesource.com/platform/system/core/+/bad50ed24f9d48d001fcedd332d59f162dc3432d%5E%21/#F0

### CVE-2020-0246 ID High

permission check

https://android.googlesource.com/platform/frameworks/opt/telephony/+/cfaf9f980aa8d3ca51cd8555ca27cd0ef561cb02

### * CVE-2020-0412 ID High

permission check

### * CVE-2020-0419 ID High

https://android.googlesource.com/platform/frameworks/base/+/6bc126b040718d9252ec72d2dd5207c7a4913238

### CVE-2020-0213 ID High

https://android.googlesource.com/platform/external/libhevc/+/75db1b8e484ffd9256c553cb28dcd0b5d7a3c274

### CVE-2020-0411 ID High

https://android.googlesource.com/platform/frameworks/av/+/7c67c79fff14cf28a19fda1bfb532804759f85fe


### CVE-2020-0414 ID High

https://android.googlesource.com/platform/frameworks/av/+/33403f0ef8ec7e6217f4969879fa81101e6b84ee

### * CVE-2019-2194 EoP Moderate

https://android.googlesource.com/platform/frameworks/native/+/76923a32ab6ea25115b65ff86ade7235ba7b3a33%5E%21/#F0

### * CVE-2020-0215

https://android.googlesource.com/platform/packages/apps/Nfc/+/8a414674747f166171f68294836967660905d068%5E%21/#F0

### * CVE-2020-0416
UI
https://android.googlesource.com/platform/packages/apps/Settings/+/4794b798c427c53a9d0f8c608c367a3e6469ed5f

### CVE-2020-0377

bluetooth
Fix possible OOB when receive gatt read type response data
Chong Wang (王冲) (csddl147@gmail.com)


### * CVE-2020-0378

[Passpoint] Remove R2 broadcasts

Remove R2 broadcasts for Icon, deauth imminent and subscription
remediation. These broadcasts are not used and not necessary,
and also leaked the Passpoint AP BSSID without location
permission.

### * CVE-2020-0398

PendingIntent
Use PendingIntent.FLAG_IMMUTABLE in PendingIntent in NotificationMgr

Require that the PendingIntent be immutable so that a malicious app is
 not able to hijack and mutate any of the details.

### CVE-2020-0400

Use PendingIntent.FLAG_IMMUTABLE in PendingIntent in NotificationMgr

Require that the PendingIntent be immutable so that a malicious app is
 not able to hijack and mutate any of the details

### CVE-2020-0410

SAP: Ensure pending intent is immutable

### CVE-2020-0413

bluetooth
Fix possible OOB when receive gatt read type response data

### CVE-2020-0415

Mark implicit PendingIntents as immutable

### CVE-2020-0422

Correct vulnerability when setting pending intents on import/export notifications by setting FLAG_IMMUTABLE

For cases where we were setting an empty content intent, setContentIntent has not been required since Gingerbread


## kernel

### * CVE-2020-0423 EoP High

In binder_release_work of binder.c, there is a possible use-after-free due to improper locking. This could lead to local escalation of privilege in the kernel with no additional execution privileges needed

### CVE-2020-11125 High

Out of bound access can happen in MHI command process due to lack of check of channel id value received from MHI devices
https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=146e6bb29827f0d3d1fb05ed980400bb53af13c2

### CVE-2020-11162 High

Possible buffer overflow in MHI driver due to lack of input parameter validation of EOT events received from MHI device side

https://source.codeaurora.org/quic/la/kernel/msm-4.14/commit/?id=d37bbae685207dbc67f31bc7f4ad0c6a7545abcf

### * CVE-2020-11173 High

Two threads running simultaneously from user space can lead to race condition in fastRPC driver
https://source.codeaurora.org/quic/la/kernel/msm-4.14/commit/?id=99d604642ea81f1596bb3734d82896da19f29ede

### * CVE-2020-11174 High
https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/?id=cd83646c66cdfecb5168a5585498fdcab8e65944
Array index underflow issue in adsp driver due to improper check of channel id before used as array index.

Jun Yao (姚俊) (@_2freeman) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud(https://bugcloud.360.cn/)


### MediaTek components

CVE-2020-0283	A-163008257 M-ALPS05229282*	High	KeyInstall
CVE-2020-0339	A-162980705 M-ALPS05194445*	High	Widevine
CVE-2020-0367 A-162980455 M-ALPS05194445*	High	Widevine
CVE-2020-0371	A-163008256 M-ALPS05229226*	High	KeyInstall
CVE-2020-0376 A-163003156 M-ALPS05194415*	High	ISP

### Qualcomm closed-source components

CVE-2020-3654	A-153346045*	Critical	Closed-source component
CVE-2020-3657	A-153344684*	Critical	Closed-source component
CVE-2020-3673	A-153345154*	Critical	Closed-source component
CVE-2020-3692	A-153345116*	Critical	Closed-source component
CVE-2020-11154 A-160605708*	Critical	Closed-source component
CVE-2020-11155	A-160605404*	Critical	Closed-source component
CVE-2020-3638	A-153346253*	High	Closed-source component
CVE-2020-3670	A-153345118*	High	Closed-source component
CVE-2020-3678	A-153345398*	High	Closed-source component
CVE-2020-3684	A-153346047*	High	Closed-source component
CVE-2020-3690	A-153344723*	High	Closed-source component
CVE-2020-3703	A-160605749*	High	Closed-source component
CVE-2020-3704	A-160605508*	High	Closed-source component
CVE-2020-11141	A-160606016*	High	Closed-source component
CVE-2020-11156	A-160605294*	High	Closed-source component
CVE-2020-11157	A-160605864*	High	Closed-source component
CVE-2020-11164	A-160605595*	High	Closed-source component
CVE-2020-11169	A-160605405*	High	Closed-source component

# biubiubiu

I prefer native c/c++ bugs which may have more security problems.

for Qualcomm https://www.qualcomm.com/company/product-security/bulletins
