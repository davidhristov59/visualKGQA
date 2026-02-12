# VisualKGQA: Multi-Hop Reasoning Path Visualization

An interactive platform that combines on-demand subgraph loading with multi-hop reasoning path visualization to support both exploratory knowledge graph navigation and visual question answering.
 Developed by <br/> 
 
## Overview

VisualKGQA addresses two critical challenges in knowledge graph utilization:
1. **Scalable exploration** of large graphs without overwhelming visualizations
2. **Transparent, explainable** multi-hop question answering with visible reasoning paths

Rather than rendering entire graphs, the interface incrementally expands neighborhoods through user interactions and question-scoped retrieval, keeping the visible subgraph relevant and manageable. An aging-based shading mechanism dynamically adjusts node opacity based on recency, interaction frequency, and structural connectivity, producing an intuitive visual gradient of exploration history.

## System Architecture

### Backend
- **Framework**: Spring Boot 3.4.6 with Java 21
- **RDF Processing**: Apache Jena 5.3.0
- **Supported Formats**: RDF, OWL, Turtle, N-Triples
- **Query Engine**: SPARQL via Apache Jena ARQ

### Frontend
- **Framework**: React 19
- **Visualization**: D3.js force-directed layouts
- **API Communication**: RESTful endpoints

## Use Cases

### Research
Discover implicit cross-domain relationships without multiple database queries. Trace complex pathways from symptoms through genes to drug targets.

### Education
Teach knowledge representation concepts through interactive exploration. Students learn semantic relationships by directly engaging with graph structures.

### Domain Analysis
Enable domain experts in medicine, law, or finance to investigate specialized knowledge bases without learning query languages.

##  How to Start the Application

You can start the application using Docker (recommended) or manually.

###  Start with Docker

1. Ensure [Docker](https://www.docker.com/products/docker-desktop/) is installed and running.
2. Pull and start the containers using Docker Compose:
   ```bash
   docker-compose up --build -d
### If you prefer manually

-  Backend (Java Spring Boot — Port 8080)
   ```bash
    cd backend
    ./mvnw spring-boot:run
    On Windows, use mvnw spring-boot:run instead.
    ```
-  Frontend (React + Vite — Port 5173)
   ```bash
    cd frontend
    npm install
    npm run dev
    ```
###  Prerequisites

Ensure the following are installed on your system:

- [Node.js](https://nodejs.org/) (version 18 or higher recommended)
- [Java JDK](https://adoptium.net/) (version 21)
- [Maven](https://maven.apache.org/) (comes bundled with Spring Boot projects)
- Git

