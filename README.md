# ChainShield

ChainShield is a security-focused web application designed to analyze URLs and provide a foundation for detecting potentially suspicious or malicious links.

## Current Project Status

The backend foundation has been developed using **FastAPI**. The current backend can:

* Receive URL scan requests
* Validate URLs using Pydantic
* Process scan requests through a dedicated API route
* Provide API documentation using Swagger UI
* Support frontend-backend communication through CORS

## Technology Stack

* Python
* FastAPI
* Uvicorn
* Pydantic
* REST API

## API Endpoints

### 1. Home

**Method:** `GET`

**Endpoint:**

```text
/
```

Returns a message confirming that the ChainShield backend is running.

### 2. Scan URL

**Method:** `POST`

**Endpoint:**

```text
/scan
```

**Request:**

```json
{
  "url": "https://example.com"
}
```

**Response:**

```json
{
  "url": "https://example.com/",
  "status": "received",
  "message": "URL received successfully"
}
```

The API validates that the submitted value is a valid URL before processing the request.

## API Documentation

After starting the backend, Swagger UI is available at:

```text
http://127.0.0.1:8000/docs
```

Swagger UI can be used to test the available API endpoints directly from the browser.

## Project Structure

```text
Chainshield/
│
├── app/
│   ├── __init__.py
│   ├── routes/
│   │   ├── __init__.py
│   │   └── scan.py
│   │
│   ├── schemas/
│   │   ├── __init__.py
│   │   └── scan.py
│   │
│   ├── services/
│   └── utils/
│
├── main.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Running the Backend Locally

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
uvicorn main:app --reload
```

The backend will run locally at:

```text
http://127.0.0.1:8000
```

## Planned Modules

The following modules are planned for later stages of ChainShield development:

* Machine Learning based URL analysis
* SHAP-based prediction explanations
* Blockchain service integration
* React dashboard
* Chrome extension
* Integration and performance testing
* Final system validation

These modules are part of the planned development roadmap and are not yet implemented in the current backend version.
