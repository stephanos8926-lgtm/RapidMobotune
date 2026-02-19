# RapidMobotune

**Android Performance Optimization Toolkit**

A comprehensive tool for Android users to optimize device performance through intelligent bloatware removal, system parameter tuning, and resource management using Termux, Shizuku, Python, and shell scripting.

## Features

### 🗑️ Bloatware Management
- Identify and remove bloatware, spyware, adware, and malware packages
- Research-based package analysis and classification
- Safe uninstallation and disabling of system packages
- Batch operations for efficient management

### ⚙️ System Parameter Tuning
- **PPK (Persistent Performance Kernel)** optimization
- **LMK (Low Memory Killer)** threshold tuning
- Memory management optimization
- I/O scheduler optimization
- CPU frequency scaling configuration
- Thermal management adjustments

### 📊 Advanced Monitoring & Control
- BatteryStats integration for battery optimization
- Android Intent Firewall configuration
- Process priority management (nice, renice, ionice)
- Real-time performance metrics
- Custom optimization profiles

### 🔧 Easy Setup
- Automated environment setup script
- Dependency installation
- One-command initialization

## Requirements

- Android device (5.0 or higher recommended)
- [Termux](https://termux.com/) installed
- [Shizuku](https://shizuku.rikka.app/) for privileged access
- Python 3.8+
- ADB (Android Debug Bridge) for initial setup

## Quick Start

### 1. Installation

```bash
# Clone the repository
git clone https://github.com/stephanos8926-lgtm/RapidMobotune.git
cd RapidMobotune

# Run the setup script
bash setup.sh
```

### 2. Initial Configuration

```bash
# Initialize environment
python3 src/initialize.py

# Verify Shizuku connection
python3 src/verify_permissions.py
```

### 3. Start Optimizing

```bash
# Interactive menu
python3 main.py

# Or run specific commands
python3 src/package_manager.py --analyze
python3 src/system_tuner.py --optimize
```

## Project Structure

```
RapidMobotune/
├── README.md                          # This file
├── setup.sh                           # Initial setup and dependency installation
├── main.py                            # Main entry point
├── requirements.txt                   # Python dependencies
│
├── src/
│   ├── __init__.py
│   ├── package_manager.py             # Bloatware identification & removal
│   ├── system_tuner.py                # System parameter optimization
│   ├── intent_firewall.py             # Android Intent Firewall configuration
│   ├── process_manager.py             # Process priority management
│   ├── battery_optimizer.py           # BatteryStats integration
│   ├── monitor.py                     # Real-time performance monitoring
│   └── shizuku_interface.py           # Shizuku permission handling
│
├── scripts/
│   ├── batterystats_analyzer.sh       # BatteryStats analysis tools
│   ├── optimization_profiles.sh       # Pre-built optimization profiles
│   ├── kernel_tuner.sh                # Kernel parameter tuning
│   ├── memory_optimizer.sh            # Memory tuning
│   └── io_scheduler.sh                # I/O optimization
│
├── config/
│   ├── bloatware_database.json        # Research-based package database
│   ├── profiles.json                  # Optimization profiles
│   └── default_settings.json          # Default configuration
│
├── docs/
│   ├── IMPLEMENTATION.md              # Technical implementation details
│   ├── RESEARCH.md                    # Research findings
│   ├── PPK_TUNING.md                  # PPK optimization guide
│   ├── LMK_TUNING.md                  # LMK tuning guide
│   └── TROUBLESHOOTING.md             # Common issues & solutions
│
└── tests/
    ├── test_package_manager.py
    ├── test_system_tuner.py
    └── test_integration.py
```

## Key Components

### Package Manager
- Scans installed packages against bloatware database
- Categorizes packages (bloatware, spyware, adware, malware)
- Provides safe removal with rollback capability
- Generates optimization reports

### System Tuner
- Configures kernel parameters for optimal performance
- Manages memory thresholds
- Optimizes I/O operations
- Tunes CPU governor and scaling

### Intent Firewall
- Blocks malicious Intent broadcasts
- Filters system broadcasts
- Reduces unnecessary inter-process communication

### Process Manager
- Adjusts process priorities with nice/renice
- Optimizes I/O priority with ionice
- Auto-tunes process scheduling

### Battery Optimizer
- Analyzes BatteryStats data
- Identifies power-hungry processes
- Suggests optimization strategies

## Configuration

Edit `config/default_settings.json` to customize:
- Bloatware detection sensitivity
- Optimization profile selection
- Safety thresholds
- Logging levels

## Safety & Backup

⚠️ **Important:** Always backup your device before making changes

- Automatic backup system included
- Dry-run mode for testing changes
- Easy rollback functionality
- Change logging for audit trail

## Contributing

Contributions welcome! Areas of interest:
- Expanded bloatware database
- Device-specific optimization profiles
- Additional kernel tuning parameters
- Performance benchmarking tools
- Documentation improvements

## Research & References

This project is based on extensive research into:
- Linux kernel parameter tuning
- Android system optimization
- Memory management strategies
- Power consumption analysis
- Security hardening

See `docs/RESEARCH.md` for detailed sources and findings.

## License

MIT License - See LICENSE file for details

## Disclaimer

This tool modifies system settings. Use at your own risk. The authors are not responsible for any damage, data loss, or bricking of devices. Always test in safe mode first and maintain backups.

## Support & Issues

For bugs, features, or questions:
- Open an [Issue](https://github.com/stephanos8926-lgtm/RapidMobotune/issues)
- Check [Troubleshooting Guide](docs/TROUBLESHOOTING.md)
- Review [Implementation Docs](docs/IMPLEMENTATION.md)

## Roadmap

- [ ] v0.1 - Core package manager and system tuner
- [ ] v0.2 - Intent firewall and battery optimization
- [ ] v0.3 - Advanced monitoring and profiling
- [ ] v0.4 - GUI interface
- [ ] v1.0 - Stable release with comprehensive testing

---

**RapidMobotune** - Making Android Fast Again 🚀
