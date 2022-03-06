## Framework

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
