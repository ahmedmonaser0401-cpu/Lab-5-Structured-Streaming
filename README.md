# Spark Structured Streaming — Wikimedia Events

## Project Overview
This project demonstrates real-time data processing using Apache Kafka and Apache Spark Structured Streaming. It collects Wikimedia edit events, streams them through Kafka, and analyzes them with PySpark.

## Technologies
- Python
- Apache Kafka
- Apache Spark (PySpark)
- Docker & Docker Compose
- Jupyter Notebook
- Wikimedia EventStreams API

## Features
- Wikimedia event collection using a Kafka Producer.
- Real-time data processing with Spark Structured Streaming.
- Analysis of human and bot edits.
- Tumbling and overlapping time windows.
- Edit size analysis and aggregations.
- Event filtering by Wikipedia language.

## How to Run
1. Start the environment: `docker compose up -d`
2. Create the Kafka topic: `py -3.12 admin.py`
3. Run the producer: `py -3.12 wikistream_producer.py`
4. Open JupyterLab at `http://localhost:8888/lab`.
5. Execute `notebooks/wikistream_pyspark.ipynb` and explore the streaming results.

## Results
- Processed 14,117 Wikimedia events.
- Identified 10,503 non-bot edits.
- Implemented tumbling and overlapping window aggregations.
- Tested English Wikipedia event filtering.

##  Structure
- `compose.yaml` — Docker services configuration.
- `admin.py` — Kafka topic management.
- `wikistream_producer.py` — Wikimedia event producer.
- `wikistream_producer_test.py` — English Wikipedia filter test.
- `notebooks/wikistream_pyspark.ipynb` — Spark streaming analysis.
