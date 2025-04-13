# Week 2 Day 3: 30 Day DevOps Challenge

## Project: Soccer Stats API

This project is an exercise from the 30 Day DevOps Challenge. It demonstrates the creation of a RESTful API that provides soccer player statistics and top scorers using the API-Football service, along with Docker for containerization.

## Project Overview

The project consists of a main Python script and a Dockerfile for containerization:

1. `soccer_stats.py`: Core API implementation for fetching and serving soccer statistics.
2. `Dockerfile`: Configuration for building a Docker image to run the API.

## Features

### Soccer Stats API (`soccer_stats.py`)

- Fetches player statistics from the API-Football service.
- Provides endpoints to retrieve player stats and top scorers for a specified league.
- Implements error handling for API requests.
- Health check endpoint to monitor the API status.

### Docker Integration (`Dockerfile`)

- Uses Python 3.9 slim base image for lightweight containerization.
- Installs dependencies from `requirements.txt`.
- Exposes port 8000 for API access.
- Runs the application using Uvicorn.

## API Endpoints

- `GET /`: Root endpoint showing available endpoints and basic info.
- `GET /player/{player_id}`: Get stats for a specific player.
- `GET /topscorers/{league_id}`: Get top scorers for a league.
- `GET /health`: Health check endpoint.

## Dependencies

The project requires the following Python packages:

- `fastapi`: For building the API.
- `uvicorn`: ASGI server for running the application.
- `requests`: For making HTTP requests to the API-Football service.
- `python-dotenv`: For loading environment variables.
- `pytest`: For testing the API.
- `httpx`: For making asynchronous HTTP requests.
- `python-multipart`: For handling multipart form data.

## Monitoring

The API includes a health check endpoint:

- Returns a JSON response indicating the status of the API.
- Useful for monitoring the health of the application in production.
