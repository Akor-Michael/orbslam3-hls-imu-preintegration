# HLS-Compliant IMU Pre-Integration for ORB-SLAM3

**🚀 Code Release Coming September 2025**

This repository contains the first hardware-ready, HLS-compliant C++ kernel for IMU pre-integration in ORB-SLAM3, achieving up to **8.2× speedup** on desktop and **5.5× speedup** on ARM platforms.

## 📄 Paper

**"Fixed-Point Based IMU Pre-Integration for Accelerating ORB-SLAM 3"**  
*Michael Akor and Heoncheol Lee*  
Presented at ICMIC 2025 - The 4th International Conference on Mobile • Military • Maritime IT Convergence  
Kumoh National Institute of Technology, South Korea

## 🎯 Key Features

- **First-of-its-Kind**: First accelerator for ORB-SLAM3's IMU pre-integration module
- **Hardware-Ready**: HLS-compliant, dependency-free C++ implementation
- **High Performance**: 8.2× desktop speedup, 5.5× ARM speedup
- **Mathematical Fidelity**: Errors >20× smaller than typical MEMS IMU noise
- **Real-Time Capable**: >99% real-time slack at 200 Hz operation
- **Drop-in Replacement**: Perfect algorithmic equivalence with original ORB-SLAM3

## 🔧 Technical Highlights

- **Static Memory Design**: Eliminates dynamic allocation for predictable hardware synthesis
- **Custom SO(3) Operations**: Taylor expansion + Rodrigues formula implementation
- **Deterministic Timing**: σ/μ < 1% latency variance
- **FPGA-Ready**: Compatible with Zynq UltraScale+, Versal AI Edge, Intel Agilex

## 📊 Performance Results

| Platform | Original ORB-SLAM3 | Our HLS Kernel | Speedup |
|----------|-------------------|----------------|---------|
| Desktop (i7-13th Gen) | 10.6 μs | 1.29 μs | **8.2×** |
| ARM (Cortex-A53) | 221 μs | 40.0 μs | **5.5×** |

## 📋 What Will Be Released

### Core Implementation
- HLS-compliant IMU pre-integration kernel
- Static array-based matrix operations
- Custom SO(3) exponential map implementation
- Covariance propagation optimizations

### Integration Support
- ORB-SLAM3 integration guides
- CMake build configurations
- Cross-compilation scripts for ARM platforms
- Vivado HLS project files

### Validation Tools
- Benchmarking scripts (EuRoC MAV, TUM VI datasets)
- Accuracy validation utilities
- Performance measurement tools
- Hardware resource utilization reports

### Documentation
- Complete API documentation
- Hardware synthesis guidelines
- Deployment instructions for embedded platforms
- Technical implementation details

## 🏗️ Supported Platforms

### Development Platforms
- Intel Core i7-13th Gen + Ubuntu 20.04 LTS
- GCC 9 compiler support

### Target Hardware
- Xilinx Zynq UltraScale+ MPSoC (XCZU3EG)
- ARM Cortex-A53 processors
- FPGA platforms with HLS support

### Synthesis Tools
- Vivado HLS 2020.1 and newer
- Cross-compilation for embedded Linux

## 🎓 Academic Citation

```bibtex
@inproceedings{akor2025fixed,
  title={Fixed-Point Based IMU Pre-Integration for Accelerating ORB-SLAM 3},
  author={Akor, Michael and Lee, Heoncheol},
  booktitle={The 4th International Conference on Mobile, Military, Maritime IT Convergence (ICMIC)},
  year={2025},
  organization={Kumoh National Institute of Technology}
}
```

## 📞 Contact

**Authors:**
- Michael Akor - akormichael@kumoh.ac.kr
- Prof. Heoncheol Lee (Corresponding Author) - hclee@kumoh.ac.kr

**Affiliation:**  
Autonomous Intelligent Systems Lab (AISL)  
Department of ICT Convergence  
Kumoh National Institute of Technology  
Gumi-si, South Korea

## 🏷️ Keywords

`ORB-SLAM3` `IMU` `Pre-Integration` `FPGA` `HLS` `Real-Time` `Embedded Systems` `Visual-Inertial SLAM` `Hardware Acceleration` `Mobile Robotics`

## ⚖️ License

License information will be provided with the code release in September 2025.

## 🔔 Updates

- **August 2025**: Repository created, paper presented at ICMIC 2025
- **September 2025**: Full source code and documentation release planned

---

*This work reveals "a promising and previously neglected avenue for practical SLAM acceleration on constrained hardware."*
