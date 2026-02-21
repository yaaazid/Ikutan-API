# QR Scanner Event API (API Logic Only)

## 📌 Project Description
QR Scanner Event API is a RESTful backend system built to manage event ticket reservations and QR-based check-in processes.  
This API is designed for an Event Management System where attendees can reserve tickets and use QR codes for entry, while admins can validate and check-in attendees through a QR scanner.

The system ensures secure ticket validation, prevents duplicate check-ins, and manages ticket quotas efficiently per event.

This project is suitable for:
- Mobile Apps (Flutter / React Native)
- Web Admin Dashboard
- QR Scanner Entry Systems
- Event Management Platforms

---

# 🎯 Project Purpose
The main purpose of this API is to:
- Manage event ticket reservations
- Generate unique QR codes for tickets
- Validate tickets using QR scanning
- Prevent duplicate event entry
- Provide admin control over events and attendees
- Maintain real-time ticket tracking and quota system

---

# 👥 User Roles

## 1. Attendee
Attendee is a normal user who can:
- View active events
- Reserve a ticket
- Generate and view QR code
- Check ticket status
- Cancel ticket

## 2. Admin
Admin is responsible for:
- Creating events
- Managing events
- Viewing attendees list
- Scanning QR codes
- Validating tickets
- Checking in attendees
- Deactivating events

---

# 🧱 System Architecture (API Logic)
Client (Mobile/Web) → REST API (Laravel) → Database (MySQL/PostgreSQL)

Core Modules:
- Authentication Module
- Event Module
- Ticket Module
- QR Code Module
- Admin Scanner Module

---

# 🔐 Authentication Endpoints

## Register User
**POST** `/api/auth/register`

Description:  
Register a new attendee account.

Request Body:
```json
{
  "name": "John Doe",
  "email": "john@email.com",
  "password": "password"
}