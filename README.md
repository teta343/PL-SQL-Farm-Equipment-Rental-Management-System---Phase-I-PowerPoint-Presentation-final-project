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


