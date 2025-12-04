# Normalization Justification

## 1NF (First Normal Form)
- All tables have atomic values
- No repeating groups
- Each table has a primary key
- Example: FARMER table has single Contact_Number column

## 2NF (Second Normal Form)
- All non-key attributes fully dependent on entire primary key
- Example: In RENTAL table, all attributes depend on Rental_ID

## 3NF (Third Normal Form)
- No transitive dependencies
- Example: Equipment owner details in OWNER table, not in EQUIPMENT
