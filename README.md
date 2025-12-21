course: INSY 8311 - Database Development with PL/SQL

Student: Teta kevine 

ID: 27973

Lecturer: Eric Maniraquha

University: Adventist University of Central Africa (AUCA)

Date: 20 December 2025

A comprehensive Oracle PL/SQL database solution for managing farm equipment rentals in Rwanda.
This production-ready system automates the entire rental process from booking to return, with built-in analytics and security features.


🎯 Problem Statement

Farmers and agricultural cooperatives struggle with manual equipment rental systems that cause scheduling conflicts, revenue loss, 
and poor maintenance tracking. Our solution provides real-time availability, automated bookings, and business intelligence for better decision-making.


🎯 Key Objectives

✅ Automate rental booking and payment processing

✅ Track equipment maintenance and utilization

✅ Implement advanced auditing and security rules

✅ Provide business intelligence dashboards

✅ Ensure data integrity with PL/SQL constraints

1. SETUP  THE  DATABASE

Run these scripts in SQL Developer in order:

@01_create_tables.sql    -- Creates all 8 database tables

@02_insert_data.sql      -- Inserts sample data

@03_procedures_functions.sql -- Creates PL/SQL programs

@04_triggers_audit.sql   -- Sets up security and auditing


2. TEST THE  SYSTEM

-- Book a tractor for 7 days

DECLARE
    v_rental_id NUMBER;
    v_status VARCHAR2(200);
    
BEGIN
    rental_management_pkg.book_rental(
        p_cust_id => 101,      -- Customer ID
        p_eq_id => 1,          -- Tractor ID  
        p_days => 7,           -- 7 days rental
        p_rental_id => v_rental_id,
        p_status => v_status
    );
    DBMS_OUTPUT.PUT_LINE('Result: ' || v_status);
END;
/

3. CHECK AUDIT LOG (Security Feature)

SELECT * FROM Audit_Log 

WHERE attempt_date >= SYSDATE - 1

ORDER BY attempt_date DESC;

Phase I: Problem Identification 🔍

Why it mattered: We identified real pain points - not just technical requirements. 
This ensured our solution would actually help people, not just be a "database for database's sake."

Phase II: Business Process Modeling 📈

Why it mattered: We mapped out how farmers actually work - from inquiry to return. 
This human-centered design made our system intuitive and practical.

Phase III: Logical Database Design 🏗️

Why it mattered: Clean, organized structure means fast queries, easy maintenance, and scalability. 
Proper normalization prevents data errors as the business grows.

Phase IV: Database Creation ⚙️

Why it mattered: Setting up the technical foundation correctly ensures reliability,
security, and performance from day one.

Phase V: Table Implementation 📋

Why it mattered: Realistic sample data allowed thorough testing before real users depend on the system.

Phase VI: PL/SQL Programming 💻

Why it mattered: This is the "brain" of the system - automated logic that handles complex business rules, calculations, and validations automatically.

Phase VII: Advanced Features & Security 🔒

Why it mattered: The audit system and business rules ensure trust. Companies know who did what, when, and why. The weekday/holiday restriction prevents costly human errors.
