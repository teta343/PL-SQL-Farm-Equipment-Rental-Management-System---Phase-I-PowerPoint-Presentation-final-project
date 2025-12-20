Course: INSY 8311 - Database Development with PL/SQl

Institution: Adventist University of Central Africa (AUCA)

Academic Year: 2025-2026 | Semester I

Lecturer: Eric Maniraquha

Student: Teta kevine 

Student ID: 27973

This capstone project demonstrates mastery of Oracle database design, PL/SQL development, and Business Intelligence implementation through a comprehensive Farm Equipment Rental Management System.

🎯 Problem Statement

Farmers and agricultural cooperatives in Rwanda face significant challenges in managing equipment rentals:

Manual tracking leads to double bookings and scheduling conflicts

No real-time availability information for equipment

Inefficient maintenance scheduling causing equipment downtime

Revenue loss from poor inventory management

🚀 Solution

A production-ready Oracle PL/SQL database system featuring:

Core Features

✅ Automated Booking System - Real-time availability checking and reservation

✅ Payment Processing - Multiple payment methods with transaction tracking

✅ Maintenance Management - Scheduled and on-demand maintenance tracking

✅ Advanced Auditing - Comprehensive security and compliance logging

✅ Business Intelligence - Analytics and reporting capabilities

Lack of business intelligence for decision making
Database Schema
8 Normalized Tables (3NF):

Customer - Customer information and membership tracking

Equipment - Equipment inventory and status management

Rental - Rental transactions and scheduling

Payment - Payment processing and reconciliation

Maintenance - Equipment maintenance history

Holidays - Public holiday management for business rules

Audit_Log - Comprehensive security auditing

Employee_Access - Employee activity tracking

⚙️ Technical Implementation

PL/SQL Components Developed

Phase I-V: Foundation
Business Process Modeling (UML/BPMN diagrams)

Logical Database Design (ER diagrams, Data Dictionary)

Physical Database Creation (Oracle PDB configuration)

Table Implementation (CREATE scripts with constraints)

Data Population (100+ realistic records per main table)

Phase VI: PL/SQL Programming
Stored Procedures (5+ procedures including book_equipment, process_payment, return_equipment)

Functions (5+ functions including calculate_rental_cost, check_availability)

Cursors (Explicit and bulk collection cursors)

Window Functions (ROW_NUMBER, RANK, LAG/LEAD analytics)

Packages (rental_management_pkg with encapsulated logic)

Phase VII: Advanced Programming & Auditing
Triggers (4 triggers implementing critical business rules)

Business Rule: Employees cannot INSERT/UPDATE/DELETE on weekdays or public holidays

Audit System: Comprehensive logging of all database operations

Security Rules: Row-level and statement-level restrictions

Holiday Management: Dynamic public holiday tracking
