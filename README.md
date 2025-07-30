# F1 RaceFlux - Formula 1 Data Pipeline

A comprehensive real-time Formula 1 data processing pipeline with advanced ML lifecycle management, analytics, and prediction capabilities. This project collects, processes, and visualizes F1 telemetry data using a modern data engineering and MLOps stack with MLflow integration.

## 🏎️ Overview

F1 RaceFlux is a complete data pipeline that:
- Captures real-time Formula 1 race telemetry data
- Processes and enriches the data using Apache Spark
- Stores the processed data in MongoDB
- Provides RESTful API access to the data
- Visualizes race analytics through an interactive Streamlit dashboard

## 🚀 Architecture

The pipeline consists of the following components:

- **Producer**: Collects F1 telemetry data using FastF1 library and publishes to Kafka topics
- **Kafka**: Message broker for data streaming
- **Spark Processor**: Consumes and processes the data streams from Kafka
- **MongoDB**: Stores processed race, telemetry, and analytics data
- **MLflow**: ML lifecycle management for experiment tracking, model registry, and deployment
- **PostgreSQL**: Backend storage for MLflow metadata and model versioning
- **API**: Provides RESTful endpoints for accessing the processed data
- **Streamlit App**: Interactive dashboard for data visualization and race analytics

## 🛠️ Technologies Used

- **Apache Kafka**: Real-time data streaming
- **Apache Spark**: Distributed data processing with MLlib for machine learning
- **MongoDB**: NoSQL database for storage
- **MLflow**: ML lifecycle management, experiment tracking, and model registry
- **PostgreSQL**: Relational database for MLflow backend
- **FastAPI**: API development
- **Streamlit**: Data visualization and dashboard
- **FastF1**: Formula 1 data collection
- **Docker & Docker Compose**: Containerization and orchestration

## 📊 Features

### Data Processing & Analytics
- Real-time telemetry visualization
- Driver performance comparison
- Track speed heatmaps
- Lap time analysis
- Historical data analysis
- Race result summaries

### Machine Learning & Predictions
- **ML Model Training**: Gradient Boosting models for race outcome prediction
- **Experiment Tracking**: Complete MLflow integration for tracking experiments, parameters, and metrics
- **Model Registry**: Versioned model storage with staging/production lifecycle management
- **Automated Model Evaluation**: Custom F1-specific metrics (position accuracy, podium prediction rates)
- **Model Artifacts**: Automated logging of training plots, model performance visualizations
- **A/B Testing**: Compare model performance across different feature sets and hyperparameters

### Advanced Analytics
- Race prediction and simulation using 2025 driver lineups
- Weather impact analysis on race performance
- Tire degradation modeling and strategy optimization
- Driver performance forecasting across different circuits

## 🏁 Getting Started

### Prerequisites

- Docker and Docker Compose
- Git

### Installation & Setup

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/f1-data-pipeline.git
   cd f1-data-pipeline
   ```

2. Start the services using Docker Compose:
   ```
   docker-compose up -d
   ```

3. Access the applications:
   - **Streamlit Dashboard**: http://localhost:8501
   - **MLflow Tracking UI**: http://localhost:5001
   - **API Documentation**: http://localhost:8000/docs

## 📝 Usage

### Data Visualization Mode
1. Open the Streamlit dashboard
2. Select "Data Visualization" mode
3. Choose a race year, Grand Prix, and session type
4. Click "Process Data" to fetch and process the data
5. Explore the various visualization tabs:
   - Race Results
   - Telemetry Visualization
   - Lap Comparison
   - Driver Simulation
   - Track Speed Heatmap

### ML Prediction Mode
1. Switch to "Race Predictions" mode in the sidebar
2. Select a 2025 Grand Prix event
3. Configure training data years (default: 2022-2024)
4. Click "Run Race Prediction" to train the model and generate predictions
5. View detailed race predictions with:
   - Position forecasts for 2025 driver lineup
   - Lap-by-lap position progression
   - Weather impact analysis
   - Tire degradation modeling

### ML Experiment Tracking
1. Switch to "ML Experiments" mode in the sidebar
2. Monitor and compare different model training runs
3. View experiment metrics, parameters, and artifacts
4. Manage model versions in the MLflow registry
5. Compare model performance across different configurations
6. Access detailed model artifacts and visualizations

## 🔬 MLflow Integration & ML Lifecycle Management

This project demonstrates enterprise-level ML lifecycle management using MLflow:

### Experiment Tracking
- **Automated Logging**: All model training runs automatically log parameters, metrics, and artifacts
- **Custom Metrics**: F1-specific metrics like position accuracy, podium prediction rates, and DNF rates
- **Parameter Tracking**: Hyperparameters, data splits, and model configurations
- **Run Comparison**: Side-by-side comparison of different experiments and their performance

### Model Registry & Versioning
- **Centralized Registry**: All trained models are automatically registered with versioning
- **Staging Lifecycle**: Models progress through Development → Staging → Production stages
- **Model Lineage**: Complete traceability from data to deployed model
- **Rollback Capability**: Easy rollback to previous model versions if needed

### Automated Artifacts
- **Training Visualizations**: Prediction vs actual plots, residual analysis, error distributions
- **Model Performance**: Comprehensive evaluation reports with custom F1 metrics
- **Data Profiling**: Training and validation data summaries and statistics
- **Feature Importance**: Understanding which factors most influence race predictions

### Production Deployment
- **Model Serving**: MLflow model serving endpoints for real-time predictions
- **A/B Testing**: Compare different model versions in production
- **Performance Monitoring**: Track model drift and performance degradation over time
- **Scalable Infrastructure**: PostgreSQL backend with artifact storage for enterprise deployment

### Key Benefits for ML Teams
- **Reproducibility**: Every experiment is fully reproducible with tracked parameters and code versions
- **Collaboration**: Team members can easily share and compare experiments
- **Governance**: Full audit trail of model development and deployment decisions
- **Efficiency**: Automated logging reduces manual tracking overhead
- **Quality**: Systematic evaluation and comparison ensures only the best models reach production


