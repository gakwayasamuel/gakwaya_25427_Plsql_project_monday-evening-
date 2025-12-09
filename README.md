# gakwaya_25427_Plsql_project_monday-evening-
🌾 Crop Disease Alert System — PL/SQL Capstone Project
Student: Gakwaya Samuel — ID 25427

A Smart Database-Driven Early Disease Detection System for Farmers

📖 Project Overview

The Crop Disease Alert System is a PL/SQL-powered solution that helps farmers detect crop diseases early.
Most farmers rely on manual inspection, which often leads to late detection and major crop losses.

This system stores information about farms, crops, observations, and disease patterns.
When a new observation is added, a PL/SQL trigger automatically checks symptoms and generates a real-time alert.

✔ Works entirely inside Oracle Database
✔ Offline-friendly (suitable for rural areas)
✔ Simple rule-based detection
✔ Fast, expandable, and practical

🏗 System Architecture Diagram

(Insert your ERD or architecture image here)

📸 ERD_Diagram.png

🗃 Database Schema
1️⃣ FARM
Column	Description
farm_id (PK)	Unique farm identifier
farm_name	Farm name
location	Location of farm
owner_name	Owner of the farm
2️⃣ CROP
Column	Description
crop_id (PK)	Unique crop ID
farm_id (FK)	Links to FARM
crop_type	Example: Beans, Maize, etc
planting_date	Date crop was planted
3️⃣ OBSERVATION
Column	Description
obs_id (PK)	Unique observation ID
crop_id (FK)	Crop being observed
obs_date	Observation date
symptoms	Visible symptoms
severity	Scale 1–10
4️⃣ DISEASE_PATTERN
Column	Description
pattern_id (PK)	Unique disease pattern
disease_name	Name of disease
symptom_keywords	Keyword matches for symptoms
recommended_action	Suggested action
5️⃣ ALERT
Column	Description
alert_id (PK)	Unique alert ID
obs_id (FK)	Observation that triggered the alert
disease_name	Detected disease
action	Recommended action
alert_date	Alert creation date
⚙️ PL/SQL Features Implemented
✔ Trigger: Auto Disease Alert

Checks new observations and creates alerts instantly.

✔ Stored Procedures

Used for adding farms, adding crops, updating diseases, etc.

✔ Functions

Calculate risk levels or symptom matches.

✔ Packages

A package (farm_management_pkg) for cleaner, organized logic.

✔ Exception Handling

Prevents invalid insertions and runtime errors.

🖼 Screenshots (Attach Here)
1. Database Tables
📸 screenshot_tables.png

2. Trigger Auto-Alert Output
📸 screenshot_trigger_output.png

3. Package Execution Output
📸 screenshot_package_test.png

4. SQL*Plus PDB Creation
📸 screenshot_sqlplus_pdb.png

▶️ Running the System
1. Create Tables
@sql/tables.sql

2. Insert Sample Data
@sql/sample_data.sql

3. Compile Functions
@sql/functions.sql

4. Compile Procedures & Packages
@sql/procedures.sql

5. Compile Trigger
@sql/triggers.sql

6. Run All Tests
@sql/tests.sql

🚀 How the System Works (Workflow)

1️⃣ User adds an observation
2️⃣ Trigger checks disease patterns
3️⃣ Symptoms match keywords
4️⃣ System automatically creates an alert
5️⃣ User sees disease name + recommended action

🌱 Innovation & Advantages
✔ Automatic disease alerts

No human checking needed — alerts appear instantly.

✔ Keyword-based detection

Simple, fast, and easy to expand.

✔ Action recommendations

Farmers immediately know what to do.

✔ Works offline

Ideal for small farmers and cooperatives.

✔ Fully database-driven

No web app needed — everything runs in Oracle.

🧑‍💻 Developer

Gakwaya Samuel
Student ID: 25427
Course: Oracle Database — PL/SQL Final Capstone Project
