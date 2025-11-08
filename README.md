# Browser Use Proxy

Simple FastAPI proxy service that enables n8n-nodes-browser-use to communicate with browser-use containers.

## Features

- Lightweight Python 3.11 proxy
- FastAPI for high performance
- Token-based authentication
- Health check endpoint
- Forwards requests to browser-use webui

## Environment Variables

- `BROWSER_USE_API_TOKEN` - API token for authentication
- `BROWSER_USE_HOST` - Hostname of browser-use service (default: n8n-browseruse-iulufe)
- `BROWSER_USE_PORT` - Port of browser-use service (default: 7788)

## Endpoints

- `GET /` - Service info
- `GET /health` - Health check (tests upstream connection)
- `POST /api/task` - Execute browser automation task

## Usage with n8n

In n8n browser-use node credentials:
- **URL**: `http://browser-use-proxy:8000`
- **API Token**: Your `BROWSER_USE_API_TOKEN` value

## Deployment

Deploy using Docker Compose in Dokploy or any Docker Swarm environment.