
# FusionX Kernel Stable Release Changelogs  

## **FusionX v1.6-r**  
- Synced with **N0k** upstream changes  
- Upstreamed to Linux **4.19.329**  
- Merged latest **Google ASB** security tag  
- **Performance:**  
  - Improved console output latency  
  - Optimized scheduler efficiency & IRQ/thread placement  
  - Added **TEO (Timer Events Oriented)** idle governor  
  - Relaxed CPU latency for power savings  
  - Enhanced CPU scaling + early governor registration  
  - **Tri-cluster API** support for better CPU efficiency  
- **GPU/Graphics:**  
  - **KGSL** optimizations: fixed races, better scheduling  
  - Increased GPU processing limits + storage I/O size  
  - **OC/UV support:** 683MHz → 150MHz  
- **Memory:**  
  - Refactored **zRAM** handling  
  - Tweaked memory pressure for 6GB+ devices  
- **Security:**  
  - Updated **jitterentropy** RNG  
  - Reimplemented **WireGuard** (upstreamed)  
- **Tree-wide cleanup:** *(Source-level optimizations)*  
  - Removed **HDMI/external display** drivers  
  - Nuked unused **MTK** platform configs  
  - Disabled obsolete ARM errata patches  
  - Dropped debug-heavy thermal drivers  
  - Nuked redundant commits (history cleanup)  
- **Fixes:**  
  - Fixed **Roblox** crashes
  - Reverted Kernel-panic-prone commits  
  - **REVERT:** "Battery: allow write any learned capacity"

## **FusionX v1.5**  
- **Thermal:**  
  - Replaced Xiaomi’s static profile with **dynamic** control  
  - Stripped debug code from thermal driver  
- **Memory:**  
  - Fixed kernel memory leaks  
  - Reduced alignment overhead (ARM-specific)  
- **Debugging:**  
  - Disabled **coresight** in `kona` DT  
  - Faked LineageOS packages in `/proc` (compatibility)  
- **Tree-wide cleanup:** *(Source-level)*  
  - Debloated kernel (reduced image size)  
  - Removed **Shamiko** hooks (risk: `/data` leaks via `susfs`)  
- **Misc:**  
  - Improved idle battery drain   
- **Credits:** @sk113r  

---  
