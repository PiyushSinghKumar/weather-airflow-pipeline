# Weather ETL Pipeline with Airflow

This repository contains an ETL pipeline for fetching weather data from the Open-Meteo API, transforming it, and loading it into a PostgreSQL database. The pipeline is orchestrated using Apache Airflow.

## Overview

The pipeline performs the following steps:

1. **Extract**: Fetches current weather data from the Open-Meteo API for a specified location (London).
2. **Transform**: Extracts relevant fields from the API response and formats them for storage.
3. **Load**: Inserts the transformed data into a PostgreSQL database.

## Prerequisites

- Docker
- Docker Compose
- Apache Airflow

## Setup

1. Clone the repository.
2. Set up Airflow connections for the Open-Meteo API and PostgreSQL.
3. Start the services using Docker Compose.
4. Access the Airflow UI at `http://localhost:8080`.
5. Trigger the `weather_etl_pipeline` DAG.

## Project Structure

- `dags/`: Contains the Airflow DAG definition.
- `docker-compose.yml`: Docker Compose file for PostgreSQL and Airflow.
- `README.md`: This file.

## DAG Workflow

1. **extract_weather_data**: Fetches weather data.
2. **transform_weather_data**: Transforms the data.
3. **load_weather_data**: Loads data into PostgreSQL.

## Database Schema

The weather data is stored in a PostgreSQL table with columns for latitude, longitude, temperature, windspeed, winddirection, weathercode, and timestamp.

## Acknowledgments

- [Open-Meteo](https://open-meteo.com/)
- [Apache Airflow](https://airflow.apache.org/)
- [PostgreSQL](https://www.postgresql.org/)
