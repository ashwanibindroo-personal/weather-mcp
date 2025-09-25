# Weather MCP Server

A simple **Model Context Protocol (MCP) server** that connects Claude Desktop to the
[National Weather Service (NWS) API](https://www.weather.gov/documentation/services-web-api).
This server provides real-time **alerts** and **forecast data** as callable tools.

---

## ✨ Features

- **`get_alerts(state)`**  
  Get active weather alerts for a U.S. state (e.g. `"CA"`, `"NY"`).

- **`get_forecast(latitude, longitude)`**  
  Get a 5-period forecast for any latitude/longitude.

- **`ping()`**  
  Simple health check tool (`"weather-mcp: alive"`) to confirm the server is running.

---

## 📦 Requirements

- Python **3.10+**
- Dependencies:
  - [`httpx`](https://www.python-httpx.org/) for async HTTP requests
  - [`mcp-server`](https://github.com/anthropics/mcp) (provides `FastMCP`)

Install with [uv](https://github.com/astral-sh/uv) (recommended):

```bash
uv pip install httpx mcp-server
