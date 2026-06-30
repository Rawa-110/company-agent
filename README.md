# AI Agent System

## Project Overview

AI Agent System is an internal help desk system that receives employee requests, analyzes them, and automatically routes them to the appropriate department.

Examples:
- Technical issues → IT Department
- Leave requests → HR Department
- Financial issues → Finance Department

---

## Features

- Receive employee requests through API.
- Automatically classify requests.
- Route requests to the correct department.
- REST API built with FastAPI.
- Interactive API documentation using Swagger UI.

---

## Technologies Used

- Python
- FastAPI
- Uvicorn
- Pydantic

---

## Project Structure

```text
ai-agent-system/
│
├── app/
│   ├── main.py
│   │
│   ├── api/
│   │   └── routes.py
│   │
│   ├── agents/
│   │   └── classifier.py
│   │
│   ├── services/
│   │   ├── ticket_service.py
│   │   └── department_service.py
│   │
│   └── schemas/
│       └── ticket.py
│
├── requirements.txt
└── README.md
```

---

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install fastapi uvicorn pydantic
```

---

## Running the Project

Run the server:

```bash
py -m uvicorn app.main:app --reload
```

The application will run on:

```text
http://127.0.0.1:8000
```

---

## API Documentation

Swagger UI:

```text
http://127.0.0.1:8000/docs
```

---

## Example Request

Endpoint:

```http
POST /ticket
```

Request Body:

```json
{
  "message": "The internet is not working"
}
```

Response:

```json
{
  "message": "The internet is not working",
  "department": "IT"
}
```

---

## Departments

| Department | Type of Requests |
|------------|------------------|
| IT | Technical issues |
| HR | Leave, salary, employee services |
| Finance | Payments, invoices |
| General | Other requests |

---

## Future Enhancements

- Integrate OpenAI for intelligent classification.
- Add PostgreSQL database support.
- Create a web dashboard.
- Add email notifications.
- Add ticket tracking system.

---

## Author

Developed as an AI-based internal company service desk project.
