# SAP_PURCHASE_ORDER_PROJECT
SAP ABAP Mini Project – Purchase Order Management

📌 Project Overview

This project demonstrates end-to-end creation of a Custom Purchase Order Management System in SAP using:

Custom transparent tables

Foreign key relationships

Search help

Table Maintenance Generator (TMG)

ABAP report program (Insert, Update, Delete)

📂 Technical Objects Created

1️⃣ Tables

Table	Description

ZPURCHASE_HEAD	Purchase Order Header
ZPURCHASE_ITEMS	Purchase Order Item
ZBSART_DATA	Document Type Table

2️⃣ Search Help

Object	Description

ZBSART	Document Type Search Help

3️⃣ Foreign Keys

Child Table	Field	Check Table	Purpose

ZPURCHASE_ITEMS	ZEBELN	ZPURCHASE_HEAD	Validate PO Number
ZPURCHASE_ITEMS	MATNR	MARA	Validate Material Number
ZPURCHASE_HEAD	ZBSART	ZBSART_DATA	Validate Document Type

4️⃣ ABAP Report Program

Program: ZPURCHASE_ORDER1

Features:

Insert Purchase Order (Header + Item)

Delete Purchase Order

Modify Purchase Order Item

Field validations using SAP Data Dictionary

Dynamic screen handling using MODIFY SCREEN

---

🛠 Technologies Used

SAP ABAP

SE11 (Data Dictionary)

SE54 (TMG Generation)

SE38 (Report Program)

📸 Screenshots

Add the following inside /screenshots folder:

Table definitions

TMG screens

Search help

Foreign key settings

ABAP program

Test results (Insert/Delete/Modify)


✔ Example Insert Code (From report)

INSERT INTO zpurchase_head VALUES wa_head.
IF sy-subrc = 0.
  WRITE: 'Header inserted successfully'.
ELSE.
  WRITE: 'Header insert failed'.
ENDIF.

🚀 How to Run

1. Execute program ZPURCHASE_ORDER1


2. Select operation:

Insert PO

Delete PO

Modify PO Item

3. Enter required fields

4. Execute

📦 Project Folder Structure

/SAP_Purchase_Order_Project
    /tables
    /reports
    /screenshots
    /documentation
    README.md
