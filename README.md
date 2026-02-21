# QR Scanner API

## 📌 Project Purpose
QR Scanner API is a RESTful backend system designed for event ticketing using QR codes.  
This API allows attendees to reserve tickets, generate QR codes, and check their entry status, while admins can manage events, scan QR codes, validate tickets, and perform check-ins.

Key Objectives:
- Manage events and attendees
- Provide QR-based ticket validation
- Prevent duplicate check-ins
- Support admin scanning system
- Track ticket counts per event

---

## 🚀 Available Endpoints

### 🔐 Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/register | Register new user |
| POST | /api/auth/login | Login and get token |
| POST | /api/auth/logout | Logout authenticated user |

Authentication uses Bearer Token (Sanctum/JWT).

---

## 🎟️ Attendee Endpoints

### 1. Get Active Events (Dashboard)
**GET /api/events**

Description:
- Retrieve list of active events
- Includes ticket count and remaining quota

---

### 2. Reserve Ticket
**POST /api/tickets/reserve**

Request Body:
```json
{
  "event_id": 1
}