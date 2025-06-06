# Natural Language to SQL API

Convert natural language queries to SQL using AI. Built with FastAPI, Oracle Database, and Mistral AI.

## Quick Start

1. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Setup environment variables**
   Create `.env` file:
   ```env
   DB_HOST=your-oracle-host
   DB_PORT=1521
   DB_SERVICE_NAME=your-service
   DB_USER=your-username
   DB_PASSWORD=your-password
   DB_SCHEMA=your-schema
   MISTRAL_API_KEY=your-mistral-key
   ```

3. **Run the server**
   ```bash
   python main.py
   ```


## API Endpoints

- `POST /generate-sql` - Convert natural language to SQL
- `GET /status` - Check service health
- `GET /docs` - API documentation

## Features

- 🔍 Smart table detection using vector search
- 🤖 AI-powered SQL generation with Mistral
- ⚡ Local embeddings for fast performance  
- 🔄 Auto schema updates every 24 hours

## Requirements

- Python 3.8+
- Oracle Database access
- Mistral AI API key

## Example Response

```json
{
  "sql_query": "SELECT * FROM customers WHERE city = 'New York'",
  "relevant_tables": ["customers"],
  "execution_time": 1.2
}
```
