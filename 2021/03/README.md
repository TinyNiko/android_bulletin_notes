## Framework

### `CVE-2021-0395`: EoP High

UAF In StopServicesAndLogViolations of reboot.cpp. In reboot, it will stop services, but if services is already died, it's will cause UAF.

Hongli Han (@hexb1n) and Guang Gong (@oldfresher) of 360 Alpha Lab working with 360 BugCloud

### `CVE-2021-0391`: EoP High

Protect account chooser activities against overlay.
UI hijack in core/java/android/accounts/ChooseAccountActivity
7h0r

### `CVE-2021-0398`： EoP High

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
