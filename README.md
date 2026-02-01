# Poker MDA

## Project Overview
This project implements a Medallion Architecture (MDA) for poker data, structuring data into Bronze, Silver, and Gold layers to ensure data quality, consistency, and usability for analytics and machine learning.

## Architecture
The architecture follows a Medallion pattern, organized into three distinct layers:

### Bronze Layer
This layer contains raw, immutable data ingested directly from source systems. Data here is stored as-is, preserving the original format and history.

### Silver Layer
The Silver layer processes and refines the data from the Bronze layer. It involves data cleaning, standardization, filtering, and combining disparate datasets. This layer provides a "single source of truth" for core business entities.

### Gold Layer
The Gold layer delivers highly aggregated and denormalized data optimized for specific business use cases, reporting, and machine learning models. This layer focuses on performance and ease of consumption for end-users.

## Data Architecture
<img src="docs/poker-erd.drawio.svg" width="100%" alt="Poker Data Architecture ERD">

[View Full Diagram](./docs/poker-erd.drawio.svg)

## Tech Stack
*   **dbt (data build tool):** Used for transforming data in our data warehouse.
*   **BigQuery:** Our scalable and serverless data warehouse.
*   **uv:** A fast Python package installer and resolver, ensuring efficient dependency management.

## How to Run
[//]: # (TODO: Add detailed instructions on how to set up and run the project)