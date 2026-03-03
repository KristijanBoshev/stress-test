# 🚀 FastAPI CPU Stress Testing Dashboard

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.13+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/FastAPI-0.116+-green.svg" alt="FastAPI Version">
  <img src="https://img.shields.io/badge/Platform-macOS-lightgrey.svg" alt="Platform">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen.svg" alt="Status">
</div>

## 📋 Overview

A comprehensive CPU stress testing application built with FastAPI that pushes your Mac's CPU to its limits using parallel algorithms. Features real-time monitoring, performance analytics, and an intuitive web dashboard to measure your system's computational capabilities.

## ✨ Features

### 🔥 Stress Testing Algorithms
- **Prime Number Generation** - Sieve of Eratosthenes with parallel processing
- **Matrix Multiplication** - Large-scale matrix operations across all cores
- **Fibonacci Sequence** - Recursive calculations with multiprocessing
- **Parallel Sorting** - Advanced merge sort implementation
- **Monte Carlo π Calculation** - Statistical computation using random sampling

### 📊 Real-time Monitoring
- **CPU Usage** - Per-core and aggregate utilization tracking
- **Memory Monitoring** - RAM usage and availability
- **Temperature Sensors** - CPU temperature monitoring (when available)
- **Performance Metrics** - Operations per second, execution time analysis
- **Live Dashboard** - Real-time updates during stress tests
- **Data Export** - Download detailed metric history as JSON for analysis


### 🌐 Web Interface
- **Interactive Dashboard** - Clean, responsive web interface
- **Test Controls** - One-click stress test execution
- **Results History** - Detailed logs of all test runs
- **API Documentation** - Auto-generated OpenAPI/Swagger docs
- **WebSocket Support** - Live metrics streaming

## 🛠️ Installation

### Prerequisites
- Python 3.13+
- macOS (optimized for Mac hardware)
- 4+ CPU cores recommended

### Quick Setup

```bash
# Clone the repository
git clone <repository-url>
cd cc_test

# Install dependencies
pip install -r requirements.txt

# Run the application
python main.py
```

## 🚀 Usage

### Live Deployment

Test the app online at: **https://stresstest.kristijanboshev.com/**

### Web Dashboard
1. Start the application:
   ```bash
   python main.py
   ```

2. Open your browser and navigate to:
   - **Dashboard:** http://localhost:8000
   - **API Documentation:** http://localhost:8000/docs

3. Click any test button to start stress testing your CPU!

### Command Line Testing
Run the standalone test script to verify functionality:
```bash
python test_stress.py
```

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Main dashboard |
| GET | `/health` | Health check |
| GET | `/api/system-info` | System specifications |
| GET | `/api/current-metrics` | Real-time CPU/memory stats |
| POST | `/api/stress-test/prime` | Prime number generation test |
| POST | `/api/stress-test/matrix` | Matrix multiplication test |
| POST | `/api/stress-test/fibonacci` | Fibonacci sequence test |
| POST | `/api/stress-test/sorting` | Parallel sorting test |
| POST | `/api/stress-test/monte-carlo` | Monte Carlo π test |
| GET | `/api/test-results` | Historical test results |

## 📈 Performance Results

### Sample Benchmarks (10-core Mac)
```
🔢 Prime Generation: 19,826 primes/second
🔢 Matrix Multiplication: 82M operations/second  
🔢 Fibonacci Sequence: 575 calculations/second
🔢 Monte Carlo π: 4.8M iterations/second
🔥 Peak CPU Usage: Up to 79.8%
```

## 🏗️ Architecture

### Core Components

```
├── main.py                 # FastAPI application & web server
├── Dockerfile              # Builds container image
├── stress_tests.py         # CPU-intensive algorithms
├── cpu_monitor.py          # System monitoring utilities
├── test_stress.py          # Standalone testing script
├── requirements.txt        # Python dependencies
└── templates/
    └── dashboard.html      # Web interface template
└── .github/workflows
    └── docker.yaml         # Build and push pipeline
```

### Key Classes

- **`CPUStressTester`** - Main stress testing engine
- **`StressTestMonitor`** - Real-time system monitoring
- **`CPUMonitor`** - Low-level metrics collection

## 🔧 Configuration

### Test Parameters

Customize test intensity by modifying parameters:

```python
# Prime generation
max_number = 1000000  # Upper limit for prime search

# Matrix multiplication  
size = 1000  # Matrix dimensions (size x size)

# Fibonacci sequence
max_n = 50000  # Maximum Fibonacci number to calculate

# Parallel sorting
array_size = 100000  # Number of elements to sort

# Monte Carlo π
iterations = 10000000  # Number of random samples
```

### Monitoring Settings

```python
# CPU monitoring interval
interval = 1.0  # seconds

# History retention
max_history_size = 1000  # number of samples
```

## 📊 Metrics Explained

### CPU Performance
- **Operations per second** - Raw computational throughput
- **Execution time** - Total time for test completion
- **CPU utilization** - Percentage of CPU cores in use
- **Peak performance** - Maximum sustained performance

### Memory Usage
- **RAM consumption** - Memory used during testing
- **Memory efficiency** - Operations per MB of RAM
- **Peak memory** - Maximum memory usage during test

## 🔍 Troubleshooting

### Common Issues

**High CPU usage is normal** - This application intentionally maxes out your CPU
**Temperature monitoring unavailable** - Some Macs don't expose temperature sensors
**Tests taking too long** - Reduce test parameters for faster completion

### Performance Tips

- Close other applications during testing
- Ensure adequate cooling for sustained testing
- Monitor system temperature during intensive tests
- Use smaller datasets for development/testing

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## 📝 License

This project is open source and available under the MIT License.

## 🏆 Acknowledgments

- Built with [FastAPI](https://fastapi.tiangolo.com/) for high-performance web framework
- [NumPy](https://numpy.org/) for efficient numerical computations
- [psutil](https://psutil.readthedocs.io/) for system monitoring
- [Uvicorn](https://www.uvicorn.org/) for ASGI server

---

<div align="center">
  <strong>🔥 Push your CPU to the limit! 🔥</strong>
</div>