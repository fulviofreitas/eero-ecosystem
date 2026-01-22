# 🌐 eero-ecosystem

> Unified workspace for the eero network management tools ecosystem

## 📦 Projects

| Project | Description | Links |
|---------|-------------|-------|
| 🐍 **eero-api** | Python SDK for the Eero API | [![GitHub](https://img.shields.io/badge/GitHub-eero--api-blue?logo=github)](https://github.com/fulviofreitas/eero-api) [![PyPI](https://img.shields.io/pypi/v/eero-api?logo=pypi&logoColor=white)](https://pypi.org/project/eero-api/) |
| ⌨️ **eeroctl** | Command-line interface for managing Eero networks | [![GitHub](https://img.shields.io/badge/GitHub-eeroctl-blue?logo=github)](https://github.com/fulviofreitas/eeroctl) |
| 🖥️ **eero-ui** | Web-based dashboard for Eero network management | [![GitHub](https://img.shields.io/badge/GitHub-eero--ui-blue?logo=github)](https://github.com/fulviofreitas/eero-ui) |
| 📊 **eero-prometheus-exporter** | Prometheus metrics exporter for Eero networks | [![GitHub](https://img.shields.io/badge/GitHub-eero--prometheus--exporter-blue?logo=github)](https://github.com/fulviofreitas/eero-prometheus-exporter) |
| 🍺 **homebrew-eeroctl** | Homebrew tap for eeroctl installation | [![GitHub](https://img.shields.io/badge/GitHub-homebrew--eeroctl-blue?logo=github)](https://github.com/fulviofreitas/homebrew-eeroctl) |

## 🏗️ Architecture

```mermaid
flowchart TB
    subgraph Cloud["☁️ Cloud"]
        API["🌐 Eero Cloud API"]
    end

    subgraph SDK["📦 SDK Layer"]
        EERO_API["🐍 eero-api<br/><i>Python SDK</i>"]
    end

    subgraph Applications["🚀 Applications"]
        CLI["⌨️ eeroctl<br/><i>CLI Tool</i>"]
        UI["🖥️ eero-ui<br/><i>Web Dashboard</i>"]
        EXPORTER["📊 eero-prometheus-exporter<br/><i>Metrics Exporter</i>"]
    end

    subgraph Distribution["📤 Distribution"]
        HOMEBREW["🍺 homebrew-eeroctl<br/><i>Homebrew Tap</i>"]
    end

    subgraph Monitoring["📈 Monitoring"]
        PROMETHEUS["Prometheus"]
        GRAFANA["Grafana"]
    end

    API --> EERO_API
    EERO_API --> CLI
    EERO_API --> UI
    EERO_API --> EXPORTER
    CLI -.-> HOMEBREW
    EXPORTER --> PROMETHEUS
    PROMETHEUS --> GRAFANA

    style Cloud fill:#e1f5fe,stroke:#01579b
    style SDK fill:#fff3e0,stroke:#e65100
    style Applications fill:#e8f5e9,stroke:#2e7d32
    style Distribution fill:#fce4ec,stroke:#880e4f
    style Monitoring fill:#f3e5f5,stroke:#6a1b9a
```

## ⚡ Quick Start

### Install eeroctl via Homebrew

```bash
brew tap fulviofreitas/eeroctl
brew install eeroctl
```

### Install eero-api via pip

```bash
pip install eero-api
```

## 📄 License

MIT License - see individual project repositories for details.
