REAL-TIME-DATA-PROCESSING-WITH-AZURE-DATABRICKS — (STREAM PROCESSING)
PROJECT OVERVIEW

This project demonstrates an end-to-end real-time data streaming pipeline using Azure Event Hub and Azure Databricks.
It follows a STREAM PROCESSING approach to capture, process, and analyze live weather data in motion, leveraging the Medallion Architecture (Bronze → Silver → Gold) for structured, incremental refinement.

ARCHITECTURE WORKFLOW

The solution implements a modern data lakehouse streaming pattern with Azure services and PySpark Structured Streaming.

Data Source — Simulated Weather Data

JSON weather data containing temperature, humidity, wind speed, and other attributes.

Data Ingestion — Azure Event Hub

Streams real-time weather data from producers (IoT or apps).
Acts as the message broker for high-throughput ingestion.

Raw Data Store — Delta Lake (Bronze Layer)

Stores unprocessed streaming data from Event Hub for traceability.
Ensures fault tolerance and reliability.

Stream Processing — Azure Databricks (PySpark Structured Streaming)

Parses JSON payloads from Event Hub in real time.
Cleans, enriches, and transforms data into structured Delta tables.
Writes results to Silver and Gold tables for analytics.

Data Visualization — Power BI

Connects to Gold tables in Databricks for real-time insights on temperature, humidity, and weather trends.

TECH STACK

Ingestion: Azure Event Hub – Real-time data streaming

Processing: Azure Databricks – Stream processing with PySpark

Storage: Delta Lake – Bronze, Silver, and Gold architecture

Visualization: Power BI – Real-time reporting and dashboards

Language: Python (PySpark Structured Streaming)
