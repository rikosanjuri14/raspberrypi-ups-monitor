Features List

I. Comprehensive Power Monitoring
	•	AC Input Monitoring
	•	Input Voltage (
 continuously measured
	•	Input Current (A) – monitored and reported
	•	Input Power (W) – calculated and displayed
	•	AC Power State – presence/absence detection
	•	DC Output Monitoring
	•	Output Voltage (V) – monitored at UPS to Raspberry Pi
	•	Output Current (A) – tracked for load demand
	•	Output Power (W) – calculated and reported
	•	Brownout/Undervoltage Alerts – triggers if below safe thresholds
	•	Battery Monitoring
	•	Pack Voltage (V) – live reporting
	•	Charge/Discharge Current (A) – direction and magnitude
	•	Remaining Capacity (%) – via calibration table or fuel gauge
	•	Bank Support – one or two batteries, with automatic detection

⸻

II. LED Battery Visualization
	•	Always-Visible LED Chart
	•	4 rows displayed at all times for consistency
	•	Bright LED = active, Dim LED = inactive
	•	Capacity Mapping Table
	•	76–100% → 4 LEDs lit
	•	51–75% → 3 LEDs lit
	•	26–50% → 2 LEDs lit
	•	5–25% → 1 LED lit
	•	<5% → Critical Warning (blinking or highlighted)
	•	Quick Reference Status
	•	GOOD – system on AC, battery healthy
	•	CHARGING – battery charging from AC
	•	DISCHARGING – running on battery
	•	CRITICAL – low battery state, shutdown imminent
	•	UNKNOWN – no battery detected or invalid state

⸻

III. Advanced Analytics
	•	Runtime Estimation
	•	Calculates estimated minutes of operation under load
	•	Uses load averages and calibrated discharge profiles
	•	Power Smoothing
	•	Exponential moving averages for stable real-time readings
	•	Calibration Profiles
	•	Voltage-to-percentage mapping by chemistry (per bank)
	•	Guided calibration routine for full charge/discharge

⸻

IV. Event Logging & Diagnostics
	•	System Log Capture
	•	journalctl (current and previous boots)
	•	dmesg (kernel buffer)
	•	/var/log/syslog tail
	•	UPS Event Logs
	•	AC ↔ DC transitions
	•	Low battery warnings
	•	Undervoltage detections
	•	Diagnostic Snapshots
	•	JSON export of live sensor data for reporting and GitHub issues
	•	Boot splash/plymouth log integration (optional)

⸻

V. Reliability & Safety Protocols
	•	Secure Command Execution
	•	All hardware/system commands require sudo
	•	UUID/device verification required before formatting
	•	Data Protection
	•	rsync --dry-run enforced before copy/move operations
	•	System Integrity
	•	Automatic regeneration of GRUB after partition changes
	•	Documentation update triggers alongside system updates

⸻

VI. Integration & Extensibility
	•	Cross-Platform Compatibility
	•	Raspberry Pi OS, Ubuntu, MX Linux, and future distributions
	•	Data Sharing
	•	Unified /mnt/data partition structure for documents/configs across OSes
	•	Service Integration
	•	Optional systemd service for 24/7 monitoring
	•	Scalability
	•	Ready for GUI extensions (tray widgets, panels)
	•	Future Docker/Kubernetes integration for sandboxed deployments

⸻

VII. Documentation & User Experience
	•	Embedded Legends
	•	ANSI color chart and LED thresholds always displayed in UI
	•	Professional Documentation
	•	Full README with screenshots, calibration guides, and troubleshooting steps
	•	Open Roadmap
	•	Transparent roadmap and contribution guidelines
