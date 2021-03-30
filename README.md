# android_bulletin_notes

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
# 2020.12
# 2020.11
# 2020.10


# biubiubiu

I prefer native c/c++ bugs which may have more security problems.