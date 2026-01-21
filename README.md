# Quant Research Data, Signal Evaluation & AI Platform on Google Cloud  
*A Production-Grade Data, Signal & AI Engineering Platform for Financial Market Research*

This project implements a **realistic, end-to-end data, signal, and AI platform** designed to support **quantitative research, signal validation, and market intelligence workflows** in financial services.

It combines **cloud-native data engineering**, **time-aware signal evaluation**, **vector-based AI workloads**, and **daily research insight delivery**, closely mirroring how modern **quant research and pre-trade signal platforms** operate in production environments.

The solution emphasizes **data quality, reproducibility, signal integrity, and researcher-facing usability**, ensuring outputs are suitable for downstream **strategy development and trading research**.

---

## Architecture Overview
![Architecture](Assets/Quant-research.png)

---

## Business Use Case

**Industry:** Financial Services  
**Primary Users:** Quantitative Researchers, Quant Trading Teams, Data Scientists, AI Engineers  

**Objectives:**
- Ingest and standardise multi-source financial market data
- Produce AI- and signal-ready, embedding-optimised datasets
- Generate and evaluate predictive research signals daily
- Validate signal quality using leakage-safe, time-aware metrics
- Deliver research and signal insights to researchers before market open
- Support historical comparison, walk-forward analysis, and research reproducibility

---

## Key Features

### Financial Data Engineering (Production-Grade)

- **Scheduled ingestion** of structured and semi-structured financial data
- **Append-only raw data storage** for traceability and replay
- **Schema enforcement and validation** using Delta Live Tables
- **Deterministic transformations** ensuring reproducible model and signal inputs
- **Partitioned, time-aware datasets** optimised for research and signal evaluation workloads

---

### AI-Ready Data & Vectorisation

- Feature engineering tailored for:
  - Time series analysis
  - Market regime detection
  - Cross-asset research
  - NLP-driven financial insight extraction
- Embedding generation aligned with **vector database best practices**
- Optimised storage for similarity search, retrieval, and downstream AI and signal use cases

---

### Research Signal Generation & Evaluation (Quant-Focused)

- Generation of **daily predictive research signals**, including:
  - Forward return expectations
  - Volatility and risk forecasts
  - Regime classification signals
- **Leakage-safe signal alignment**, ensuring all features strictly precede prediction horizons
- **Walk-forward signal evaluation**, measuring:
  - Information Coefficient (IC)
  - Hit rate and directional accuracy
  - Signal decay and stability over time
- Time-aware signal versioning, enabling **point-in-time comparison of model and signal outputs**
- Signal outputs stored as **research-grade, trade-adjacent datasets**, suitable for downstream strategy and portfolio construction

---

### Model Training & Research Workloads

- **Vertex AI** for managed training, experimentation, and model versioning
- **TPU-backed workloads** for high-throughput model execution
- **Hugging Face models** for financial NLP and representation learning
- **Gemini models on Vertex AI** for advanced market summarisation and reasoning
- Daily retraining or inference pipelines driven by fresh market and macro data

---

### Research & Signal Insight Delivery

- **Daily automated research and signal summaries**
- Delivered via a **Streamlit frontend** designed for quant researchers
- Dropdown-based navigation allowing:
  - Current day research and signal views
  - Historical signal performance (up to previous 7 days)
- Clear separation between:
  - Data processing
  - Signal and model execution
  - Research and signal consumption

---

## Data Pipeline Design

### Ingestion Layer
**Sources include:**
- Market prices & volumes
- Macroeconomic indicators
- Corporate fundamentals
- Financial news & metadata

Data is fetched via external APIs and landed in **Google Cloud Storage** in an immutable format.

---

### Processing & Validation (Delta Live Tables)

**Bronze**
- Raw API responses  
- Append-only  
- Full lineage preserved  

**Silver**
- Schema validation  
- Normalisation and enrichment  
- Time alignment across sources  
- Missing data handling  
- Feature readiness validation for signal generation  

**Gold**
- AI-ready feature sets  
- Signal-ready datasets  
- Embedding-optimised tables  
- Research- and trading-adjacent outputs  

---

## Orchestration Strategy

- **Apache Airflow (Cloud Composer)**
- Daily DAG schedule:
  - API ingestion
  - Spark transformation
  - Data quality checks
  - Feature engineering
  - Signal generation
  - Signal evaluation
  - Vectorisation
  - Model execution
  - Insight and signal summary generation

**SLA-driven design:**  
Research and signal insights are guaranteed to be available before the start of the trading and research day.

---

## Frontend & Research Experience

### Streamlit Research & Signal Console
- Clean, minimal UI for quant workflows
- Daily research insights and predictive signal views
- Signal performance metrics and stability indicators
- Historical comparison and walk-forward evaluation support
- Model, data, and signal versioning displayed explicitly

---

## Tech Stack

| Layer | Technology | Purpose |
|------|-----------|---------|
| Cloud Platform | Google Cloud Platform | Core infrastructure |
| Orchestration | Apache Airflow | Scheduling & dependencies |
| Processing | Apache Spark | Large-scale transformations |
| Data Quality | Delta Live Tables | Validation & enforcement |
| Storage | Google Cloud Storage | Lakehouse storage |
| Vector Store | Pinecone | Embedding search & retrieval |
| AI Platform | Vertex AI | Training & inference |
| Accelerators | TPU | High-performance compute |
| Models | Hugging Face, Gemini | Financial NLP & reasoning |
| Frontend | Streamlit | Research & signal delivery |
| Language | Python | Pipelines, signals & modelling |

---

## Engineering Principles Demonstrated

- Separation of data, signal, model, and presentation layers
- Reproducible, time-aware research and signal pipelines
- Leakage-safe feature and signal evaluation
- Production-style orchestration and SLAs
- AI and quant systems built on governed, high-quality data
- Research- and trading-adjacent UX design

---

## Project Outcome

This repository demonstrates **how modern quant research and signal platforms are actually built**, combining:

- Cloud-scale data engineering  
- AI-ready lakehouse design  
- Quant signal validation practices  
- Vector-native architectures  
- Managed ML infrastructure  
- Researcher-facing signal delivery  

---

**Status:** Portfolio / Demonstration Project  
**Audience:** Data Engineers, Research Engineers, Machine Learning Engineers, Quantitative Research & Trading Technology Teams  