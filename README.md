# Navai — Intelligence Layer

Navai is an intelligent navigation system designed to generate optimized routes by combining traffic prediction with graph-based route planning.

This repository contains the **Intelligence Layer** of Navai, responsible for traffic prediction, road-network processing, and A* based route optimization.

> **Note:** The current implementation uses a **sample dataset** for traffic prediction and experimentation. It is not a live real-time traffic dataset.

## Features

- Traffic congestion prediction using machine learning
- Sample dataset for training and testing
- Road-network graph generation
- Traffic-based road weighting
- A* algorithm for optimized route calculation
- Support for traffic-aware route selection
- API layer for communication with the Navai application

## Intelligence Pipeline

    Sample Traffic Dataset
              ↓
       Data Preprocessing
              ↓
       Traffic Prediction
              ↓
       Congestion Estimate
              ↓
       Road Network Graph
              ↓
      Traffic-based Weights
              ↓
          A* Algorithm
              ↓
        Optimized Route

## Traffic Prediction

The intelligence layer uses a machine learning model to predict congestion based on traffic and road-related features.

The repository contains a **sample dataset** that is used to:

- Preprocess traffic data
- Train the prediction model
- Test the model
- Generate congestion estimates
- Experiment with traffic-aware routing

The sample dataset is intended for development and demonstration purposes. It can later be replaced with larger historical datasets and real-time traffic data.

## Route Planning

Navai represents the road network as a weighted graph.

- **Nodes** represent locations or intersections.
- **Edges** represent road segments.
- **Edge weights** represent the cost of travelling through a road.
- Traffic predictions can be incorporated into these weights.
- The **A*** algorithm is used to calculate the optimized route.

The routing process is:

    Road Network
          ↓
    Graph Construction
          ↓
    Traffic-based Edge Weights
          ↓
        A* Search
          ↓
      Optimized Route

## Technology Stack

### Machine Learning

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow Lite

### Routing

- NetworkX
- A* Algorithm
- OpenStreetMap
- Overpass API

### Backend

- Flask
- REST API

### Application Integration

- Android Studio
- Java
- XML
- Firebase
- OSMDroid

## Project Structure

    Navai-Intelligence/
    │
    ├── data/
    │   └── sample_dataset.csv
    │
    ├── model/
    │   ├── training/
    │   ├── preprocessing/
    │   └── model.tflite
    │
    ├── routing/
    │   ├── astar/
    │   └── graph.py
    │
    ├── api/
    │   └── app.py
    │
    ├── notebooks/
    │   └── experiments/
    │
    ├── requirements.txt
    └── README.md

## API Integration

The intelligence layer can communicate with the Navai Android application through a Flask REST API.

    Android Application
            ↓
         Flask API
            ↓
    ┌─────────────────────┐
    │ Intelligence Layer │
    ├─────────────────────┤
    │ Traffic Prediction  │
    │ Graph Processing    │
    │ A* Route Planning   │
    └─────────────────────┘
            ↓
      Navigation Result

## Installation

### Clone the Repository

    git clone <repository-url>
    cd Navai-Intelligence

### Create a Virtual Environment

    python -m venv venv

### Activate the Environment

Windows:

    venv\Scripts\activate

Linux/macOS:

    source venv/bin/activate

### Install Dependencies

    pip install -r requirements.txt

## Running the Intelligence Layer

Start the Flask API:

    python app.py

The API can then be accessed by the Navai application to request traffic predictions and route calculations.

## Scope

### Included

- Sample traffic dataset
- Traffic prediction
- Data preprocessing
- Machine learning model
- Road-network processing
- Graph construction
- Traffic-based edge weighting
- A* route planning
- Flask API

### Not Included

- Android application UI
- Firebase authentication
- Firebase database implementation
- GPS and location handling
- Complete navigation interface

These components belong to the main Navai application.

## Future Improvements

- Integration with real-time traffic data
- Larger historical traffic datasets
- Improved congestion prediction
- Dynamic route updates
- Real-time GPS-based rerouting
- Improved ETA prediction
- On-device ML inference
- User-reported potholes and road hazards

## About Navai

Navai is a vehicle-aware intelligent navigation system that combines **machine learning, traffic prediction, road-network data, and A* pathfinding** to improve route planning under changing traffic conditions.

This repository focuses specifically on the **Intelligence Layer** of Navai.