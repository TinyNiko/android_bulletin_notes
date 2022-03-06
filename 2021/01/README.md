## Framework

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
