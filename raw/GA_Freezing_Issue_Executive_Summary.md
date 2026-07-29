**GA Freezing Issue --- Executive Summary**

Teams Chat: GA Freezing Issue \| \~March 9--24, 2026

JVL's gaming machines are freezing completely in the field --- going totally unresponsive, screen locked, no recovery --- across multiple markets including Georgia, South Dakota, and Nebraska. The problem appears random: not every machine is affected, it doesn't happen at the same time of day, and it hasn't been reproduced in the lab. Locations sometimes just reboot the machines themselves without calling JVL, which means the true scale of the problem is likely bigger than what's been reported.

The team investigated several possible causes --- synchronous communication between the Framework and Datacenter blocking the system, a Java crash triggered by the printer library, CPU power-saving features putting COM ports to sleep, and a known AMD Raven Ridge GPU driver bug that causes identical freeze behavior on the same processor platform. None of these theories have been confirmed or fully ruled out, and the root cause remains unknown. The fact that no crash logs are ever collected after a freeze strongly suggests the Linux operating system itself becomes non-operational, pointing toward a hardware or kernel-level issue rather than a pure software bug.

The most actionable discovery was that the hardware watchdog timer --- the safety net that should automatically reboot a frozen machine --- is completely non-functional. No external watchdog hardware is wired, and the CPU's built-in watchdog is disabled in the current software. A commented-out code parameter confirmed it was intentionally turned off at some point during a hardware revision. Val directed the team to re-enable or re-implement the watchdog immediately for upcoming Texas and Nebraska releases, while continuing to try to reproduce and diagnose the underlying freeze. In parallel, five machines known to frequently freeze were brought back from a customer site (Bulldog) to the Georgia office for monitored testing.

*Source: Teams group chat "GA Freezing Issue" --- Full summary available in companion document (Segment 1, 2, 3)*
