# Nightscout Docker Setup

A simple Docker Compose setup for running Nightscout (CGM Remote Monitor) with MongoDB.

## What is Nightscout?

Nightscout is an open-source web application that allows you to view your continuous glucose monitor (CGM) data from anywhere. It's particularly popular in the diabetes community.

## Quick Start

1. **Start the services:**

   ```bash
   docker-compose up -d
   ```

2. **Access Nightscout:**
   Open your browser and go to `http://localhost:1337`

3. **Stop the services:**
   ```bash
   docker-compose down
   ```

## Configuration

- **Port:** 1337 (accessible at `http://localhost:1337`)
- **Database:** MongoDB 5.x with persistent storage
- **API Secret:** Pre-configured (change in production)
- **Timezone:** Europe/Paris (modify as needed)

## Data Persistence

Your glucose data is stored in a Docker volume (`mongo-data`) and will persist between container restarts.

## Security Note

This setup uses HTTP for simplicity. For production use, consider:

- Using HTTPS
- Changing the default API secret
- Setting up proper authentication
