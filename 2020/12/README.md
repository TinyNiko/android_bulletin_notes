## Framework

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
