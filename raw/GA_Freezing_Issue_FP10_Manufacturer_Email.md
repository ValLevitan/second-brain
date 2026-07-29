**FP10 Motherboard Manufacturer Response**

Email Chain: FP10 based V1605B; Freezing Investigation

March 20--24, 2026 \| Related to: GA Freezing Issue investigation

**Why This Email Matters**

This email chain contains a direct response from the FP10 motherboard manufacturer (Maxtang/Datang) to JVL's freezing investigation. It provides three critical pieces of information: a specific diagnosis pointing to Linux kernel compatibility with the AMD Vega 8 GPU, a recommended kernel upgrade path, and confirmation that the FP10 board has a hardware watchdog timer configurable through BIOS.

**Participants**

**Internal:** Genadi Peari (Electromechanical Dept. Manager), Pavel Frolov (Director of Engineering), Efim Podvoiski, Alexander Biratko, Anton Leshkevich, Val Levitan, Juan Martinez

**External:** Hilda Huang, Sales Manager, Maxtang Overseas BU (hilda.huang@datangpc.com)

**Email Chain (Oldest to Newest)**

**Email 1: Genadi Peari → Hilda Huang (Maxtang)**

**From:** Genadi Peari (GenadiP@jvl.ca)

**To:** Hilda Huang (hilda.huang@datangpc.com)

**Date:** Friday, March 20, 2026

**Subject:** FP10 based V1605B; Investigation

Genadi contacted the motherboard manufacturer describing the freezing issue: machines display a frozen picture and only a hard reboot resolves it. He suspected it was related to the Linux OS and asked two specific questions:

1.  Is the FP10 equipped with any type of mechanism that can be used as a watchdog?

2.  Or is the only available watchdog the one embedded in the CPU itself?

**Email 2: Hilda Huang (Maxtang) → Genadi Peari**

**From:** Hilda Huang (hilda.huang@datangpc.com)

**To:** Genadi Peari (GenadiP@jvl.ca)

**Date:** Monday, March 23, 2026, 1:38 AM

**Subject:** Re: FP10 based V1605B; Investigation

**This is the key email. The manufacturer's engineering team responded with a structured troubleshooting guide and hardware watchdog instructions.**

**Recommended Troubleshooting Priority:**

**Priority 1 --- System & Kernel**

- Confirm whether the issue started after upgrading the Linux kernel or OS version.

- Try rolling back to a previously stable kernel version.

**Priority 2 --- GPU Driver Stack**

- Reinstall and update the matching Mesa graphics library and AMD GPU firmware packages.

- If freezing persists after the update: check dmesg logs for the keywords \"AMDGPU hang\" and \"gpu reset\" --- these are the telltale log entries for a Vega 8 driver freeze.

- Upgrade the kernel to Linux 5.10 or 5.15 LTS. These versions offer optimal compatibility with the AMD Vega series.

**CRITICAL NOTE FROM MANUFACTURER:** \"The Vega 8 integrated GPU on the FP10 is sensitive to Linux kernel versions. We do not recommend using non-LTS kernels below 5.4 or above 6.0; please prioritize the officially validated 5.10/5.15 LTS versions instead. For the FP10 motherboard, the kernel version is the key factor for display stability --- the AMD GPU driver for the Vega 8 is built into the kernel, and an OS version usually comes with a default kernel that can be upgraded or downgraded independently without changing the entire OS.\"

**JVL is currently running Linux kernel 4.19, which falls below the manufacturer's minimum recommended version of 5.4.**

**Hardware Watchdog Function**

The manufacturer confirmed that the FP10 motherboard is equipped with an onboard hardware watchdog, configurable through BIOS:

3.  Power on the device and press Delete to enter BIOS setup.

4.  Switch to the Advanced tab.

5.  Locate the Watch Dog Configuration option.

6.  Set WDT Timeout Mode from Disabled to the desired value (configurable in minutes or seconds).

**Email 3: Genadi Peari → Pavel Frolov (+ team)**

**From:** Genadi Peari (GenadiP@jvl.ca)

**To:** Pavel Frolov (pavelf@jvl.ca)

**CC:** Efim Podvoiski, Alexander Biratko, Anton Leshkevich, Val Levitan, Juan Martinez

**Date:** Monday, March 23, 2026, 9:32 AM

**Subject:** Fw: FP10 based V1605B; Freezing Investigation

Genadi forwarded the manufacturer's reply to the internal team, noting: \"Please see reply from motherboard manufacturer. Seems this is a right direction for the investigation.\"

**Email 4: Pavel Frolov → Genadi Peari (+ team)**

**From:** Pavel Frolov (pavelf@jvl.ca)

**To:** Genadi Peari (GenadiP@jvl.ca)

**CC:** Efim Podvoiski, Alexander Biratko, Anton Leshkevich, Val Levitan, Juan Martinez

**Date:** Tuesday, March 24, 2026, 7:53 AM

**Subject:** RE: FP10 based V1605B; Freezing Investigation

Pavel replied: \"Good Point, good to know. Initially it was try to use WDT from the BIOS but it was not be able to ping it (due to lack of specification). Currently We use internal APU watchdog. Actually no need to make changes in BIOS.\"

**Key Takeaways**

**1. Kernel Version Is the Primary Suspect**

The motherboard manufacturer explicitly states that the Vega 8 GPU is sensitive to Linux kernel versions and that kernel 4.19 (which JVL is running) falls below their minimum recommended version. They recommend upgrading to Linux 5.10 or 5.15 LTS as the priority fix. This aligns with the AMD Raven Ridge forum posts that Genadi previously shared in the Teams chat.

**2. Two Watchdog Timers Exist on the FP10 Board**

Genadi later clarified (in the Teams chat on March 24) that the FP10 actually has two watchdog timers: one provided by the IT8786 SuperIO chip on the board, and one internal to the APU. The BIOS-configurable watchdog is the SuperIO chip --- not the APU's internal watchdog.

**3. Pavel's Response Needs Follow-Up**

Pavel's reply states they tried to use the BIOS WDT but could not ping it \"due to lack of specification,\" and that they are currently using the internal APU watchdog. However, this appears to conflict with what he said in the Teams chat on Friday (\"Currently we do not have external Watchdog wired. CPU hosted watchdog is not enabled on current software\"). The status of which watchdog is actually active in the current production software needs clarification.

**4. Diagnostic Log Check Available**

The manufacturer provided a specific diagnostic step: check dmesg logs for \"AMDGPU hang\" and \"gpu reset\" keywords. These would confirm whether the Vega 8 GPU driver is the source of the freezes. This is a quick, zero-risk check that could be run on any machine that has experienced a freeze (if logs survived) or on test machines.

*Source: Email chain \"RE: FP10 based V1605B; Freezing Investigation\" --- Companion to GA Freezing Issue chat summaries*
