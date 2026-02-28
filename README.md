# 🌐 NetDiag - Network Diagnostic & Connectivity Toolkit

![Python](https://img.shields.io/badge/Python-3.12-blue.svg?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.120-009688?logo=fastapi)
![Prometheus](https://img.shields.io/badge/Prometheus-Metrics-E6522C?logo=prometheus)
![HTTPX](https://img.shields.io/badge/HTTPX-0.28-lightgrey)
![Threading](https://img.shields.io/badge/Threading-Enabled-orange)

------------

## 📖 Overview

**NetDiag** is a lightweight **Python-based network diagnostic tool** built with **FastAPI**.  
It provides a simple web API for testing **connectivity, latency, and HTTP endpoints** with built-in **Prometheus metrics** for monitoring.

Key Features:
- 🌐 Test connectivity to hosts and ports  
- ⏱ Measure request latency using `httpx`  
- 📊 Prometheus metrics for request count & latency histograms  
- 🧪 Fully testable endpoints with FastAPI `TestClient`  
- ⚡ Multi-threaded server support  
- 🐳 Ready for Docker deployment  

-----------

## 🛠️ Tech Stack

| Layer                | Tool/Library          | Why we use it |
|----------------------|---------------------|---------------|
| **Programming**      | ![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python) | Fast scripting & network libraries |
| **Web Framework**    | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white) | Async API, auto-docs |
| **Networking**       | ![HTTPX](https://img.shields.io/badge/HTTPX-0.28-lightgrey) | Async HTTP requests |
| **Monitoring**       | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus) | Metrics scraping & monitoring |
| **Concurrency**      | Threading            | Run server and tasks simultaneously |
| **Dev Tools**        | nest_asyncio, pytest | Async support in notebooks & tests |

-----

## 🌐 Architecture

1. **User** sends GET or POST requests to endpoints (e.g., `/ping`, `/http_check`)  
2. **FastAPI server** handles requests and measures latency/connection status  
3. **Prometheus metrics** track request counts & durations  
4. Can run in **Docker**, **Kubernetes**, or **local environment**  

---

## 📦 Repository Structure

```bash
netdiag/
├── app/
│   └── main.py             # FastAPI application
├── tests/
│   └── test_endpoints.py   # Unit tests
├── requirements.txt        # Dependencies
├── Dockerfile              # Container build
├── README.md               # This documentation
└── Makefile                # Developer commands
