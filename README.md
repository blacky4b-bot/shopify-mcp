# Shopify MCP Server

MCP server for Shopify Admin API — products, orders, customers, collections, inventory, fulfillments, and webhooks.

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `SHOPIFY_STORE` | Yes | Your store name (e.g. `my-store`) |
| `SHOPIFY_CLIENT_ID` | Recommended | App client ID (enables auto-refresh) |
| `SHOPIFY_CLIENT_SECRET` | Recommended | App client secret (enables auto-refresh) |
| `SHOPIFY_ACCESS_TOKEN` | Fallback | Static Admin API access token (used if client credentials not set) |
| `SHOPIFY_API_VERSION` | No | API version (default: `2024-10`) |
| `TOKEN_REFRESH_BUFFER` | No | Seconds before expiry to refresh token (default: `1800`) |
| `MCP_TRANSPORT` | No | `streamable-http` (default) or `stdio` |
| `PORT` | No | HTTP port (default: `8000`) |

## Deploy to Render

1. Push this repo to GitHub
2. Create a new **Web Service** on Render
3. Connect your GitHub repo
4. Set environment to **Docker**
5. Add your environment variables
6. Deploy

## Run Locally

```bash
pip install -r requirements.txt
export SHOPIFY_STORE=my-store
export SHOPIFY_ACCESS_TOKEN=shpat_xxxxx
python server.py
```
