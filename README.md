# vLLM kdevops Benchmark Results Demo

This repository contains benchmark results from a kdevops demonstration of vLLM (Versatile Large Language Model) performance testing across different configurations.

## Test Results

### VM Benchmark Report (Real vLLM Production Stack)
**64 vCPUs | 64 GiB RAM | Real vLLM Engine**

- **HTML Report**: [View Report](https://htmlpreview.github.io/?https://github.com/mcgrof/demo-vllm-benchmark/blob/master/vm-results/index.html) | [Raw HTML](vm-results/index.html)
- **Performance Visualizations**:
  - [Throughput Comparison](vm-results/throughput_chart.png)
  - [Latency Distribution](vm-results/latency_chart.png)
  - [Success Rate Overview](vm-results/success_rate_chart.png)

### CPU Benchmark Report (Real Hardware - Production Server)
**128 CPUs | 1 TiB RAM | 2x Intel Xeon Gold 6438Y+ | Real vLLM Engine**

- **HTML Report**: [View Report](https://htmlpreview.github.io/?https://github.com/mcgrof/demo-vllm-benchmark/blob/master/cpu-results/index.html) | [Raw HTML](cpu-results/index.html)
- **Performance Visualizations**:
  - [Throughput Comparison](cpu-results/throughput_chart.png)
  - [Latency Distribution](cpu-results/latency_chart.png)
  - [Success Rate Overview](cpu-results/success_rate_chart.png)

**System Specifications**:
- **Processor**: 2x Intel Xeon Gold 6438Y+ (32 cores/socket, 2 threads/core)
- **Total Threads**: 128
- **Memory**: 1 TiB
- **NUMA Nodes**: 2
- **Architecture**: x86_64
- **CPU Max MHz**: 4000.0000

### GPU Benchmark Report (GPU Acceleration)
**1 vCPU | 227 GiB RAM | GPU-Accelerated vLLM Engine**

- **HTML Report**: [View Report](https://htmlpreview.github.io/?https://github.com/mcgrof/demo-vllm-benchmark/blob/master/gpu-results/index.html) | [Raw HTML](gpu-results/index.html)
- **Performance Visualizations**:
  - [Throughput Comparison](gpu-results/throughput_chart.png)
  - [Latency Distribution](gpu-results/latency_chart.png)
  - [Success Rate Overview](gpu-results/success_rate_chart.png)

### Benchmark Report
- **HTML Report**: [View Report](https://htmlpreview.github.io/?https://github.com/mcgrof/demo-vllm-benchmark/blob/master/index.html) | [Raw HTML](index.html)
- **Performance Visualizations**:
  - [Throughput Comparison](throughput_chart.png)
  - [Latency Distribution](latency_chart.png)
  - [Success Rate Overview](success_rate_chart.png)

## Key Performance Metrics

- **Total Requests**: 244,200
- **Average Throughput**: 4,036 requests/sec
- **P50 Latency**: 2.5ms
- **P95 Latency**: 5.8ms
- **P99 Latency**: 12.3ms
- **Success Rate**: 81.9%

## Test Environment

| Host | Distribution | Kernel | CPUs | Memory | Virtualization |
|------|--------------|--------|------|---------|----------------|
| debian13-vllm | Debian 13 | 6.11.4-amd64 | 8 | 8,192 MB | KVM |
| debian13-vllm-dev | Debian 13.1 | 6.12.41+deb13-amd64 | 1 | 3,912 MB | KVM |

## About

This demo showcases vLLM inference performance testing using kdevops infrastructure. The benchmarks were conducted using the Facebook OPT-125M model in CPU inference mode, demonstrating the scalability and performance characteristics of vLLM across different system configurations.

The results provide insights into:
- Request throughput capabilities
- Latency distribution patterns
- Success rate under load
- Performance optimization opportunities for LLM inference deployments

## Configuration

- **Model**: facebook/opt-125m
- **Inference Mode**: CPU
- **Max Model Length**: 2048 tokens
- **Test Framework**: kdevops vLLM workflow

## Usage

To view the detailed results, click on the HTML report link above or clone this repository and open the `index.html` file locally in your browser.