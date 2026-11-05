## krane@latitude7280

```bash
sudo tlp-stat -p
```

```
--- TLP 1.8.0 --------------------------------------------

+++ Processor
CPU model = Intel(R) Core(TM) i5-6300U CPU @ 2.40GHz

/sys/devices/system/cpu/cpu0/cpufreq/scaling_driver    = intel_pstate
/sys/devices/system/cpu/cpu0/cpufreq/scaling_governor  = powersave
/sys/devices/system/cpu/cpu0/cpufreq/scaling_available_governors = performance powersave
/sys/devices/system/cpu/cpu0/cpufreq/scaling_min_freq  =   400000 [kHz]
/sys/devices/system/cpu/cpu0/cpufreq/scaling_max_freq  =  3000000 [kHz]
/sys/devices/system/cpu/cpu0/cpufreq/cpuinfo_min_freq  =   400000 [kHz]
/sys/devices/system/cpu/cpu0/cpufreq/cpuinfo_max_freq  =  3000000 [kHz]
/sys/devices/system/cpu/cpu0/cpufreq/energy_performance_preference = balance_power [EPP]
/sys/devices/system/cpu/cpu0/cpufreq/energy_performance_available_preferences = default performance balance_performance balance_power power 

/sys/devices/system/cpu/cpu1..cpu3: omitted for clarity, use -v to show all

/sys/devices/system/cpu/intel_pstate/status            = active
/sys/devices/system/cpu/intel_pstate/min_perf_pct      =  13 [%]
/sys/devices/system/cpu/intel_pstate/max_perf_pct      = 100 [%]
/sys/devices/system/cpu/intel_pstate/no_turbo          =   0
/sys/devices/system/cpu/intel_pstate/hwp_dynamic_boost =   0
/sys/devices/system/cpu/intel_pstate/turbo_pct         =  23 [%]
/sys/devices/system/cpu/intel_pstate/num_pstates       =  27
/sys/module/workqueue/parameters/power_efficient       = Y
/proc/sys/kernel/nmi_watchdog                          = 0

+++ Platform Profile
/sys/firmware/acpi/platform_profile                    = balanced
/sys/firmware/acpi/platform_profile_choices            = cool quiet balanced performance
```

---
### To check the profile

```bash
cat /sys/firmware/acpi/platform_profile
balanced
```

---
### To change the profile

```bash
echo cool | sudo tee /sys/firmware/acpi/platform_profile
cool
```
> to change - cool -> cool
----
### To change the turbo option

```bash
echo 1 | sudo tee /sys/devices/system/cpu/intel_pstate/no_turbo
1
```
> to change - 1 -> turbo off - 0 -> turbo on
---
