SAP RAP PO View App
Overview

SAP RAP PO View App is a sample SAP Fiori Elements application developed using the ABAP RESTful Application Programming Model (RAP). The application demonstrates how to build a Purchase Order reporting application using CDS View Entities, Service Definitions, Service Bindings, Associations, and Fiori Elements annotations.

The application provides:

Purchase Order Header Details
Purchase Order Item Details
Vendor Information
Object Page Navigation
CDS Associations
OData V4 Service Exposure
SAP Fiori Elements UI Generation

This project serves as a learning reference for developers who want to understand RAP-based read-only applications in SAP S/4HANA or SAP BTP ABAP Environment. RAP is SAP's recommended framework for building modern Fiori applications.

Application Architecture
Data Model
Purchase Order Header

CDS View: ZAB_I_PoDetails

Displays:

Purchase Order Number
Document Type
Vendor
Vendor Name
Purchasing Organization
Creation Date
Created By
Purchase Order Items

CDS View: ZAB_I_EKPO

Displays item-level information associated with a Purchase Order.

Vendor Details

CDS View: ZAB_I_LFA1

Displays vendor master information.

RAP Components
CDS View Entities
Object	Description
ZAB_I_PoDetails	Purchase Order Header View
ZAB_I_EKPO	Purchase Order Item View
ZAB_I_LFA1	Vendor Master View
Associations
Association	Description
_Item	Header → PO Items
_Vendor	Header → Vendor Details
Service Layer
Service Definition
define service Zsd_po_detail {
  expose ZAB_I_PoDetails;
  expose ZAB_I_EKPO      as POitems;
  expose ZAB_I_LFA1      as POVendor;
}
Service Binding
OData V4 UI Service
Fiori Elements Preview Supported
Fiori Features
List Report

The List Report provides:

Purchase Order Search
Filter Options
Sorting
Line Item Display
Object Page

The Object Page provides:

Header Information
PO Number
Vendor
Organization
Creation Information
Purchase Order Items Facet

Displays all related PO Items.

Vendor Information Facet

Displays Vendor Master Data.

Technologies Used
ABAP RESTful Application Programming Model (RAP)
CDS View Entities
OData V4
SAP Fiori Elements
Service Definition
Service Binding
Eclipse ADT
SAP S/4HANA

Project Structure

Folders/

│
├── CDS Views
│   ├── ZAB_I_PoDetails
│   ├── ZAB_I_EKPO
│   └── ZAB_I_LFA1
│
├── Service Definition
│   └── ZSD_PO_DETAIL
│
├── Service Binding
│   └── OData V4 UI Service
│
└── Fiori Elements UI
How to Run
Step 1: Import Objects

Import all repository objects into your SAP package using abapGit or manual transport.

Step 2: Activate Objects

Activate:

CDS Views
Service Definition
Service Binding
Step 3: Publish Service
Open Service Binding.
Click Publish.
Verify service activation.
Step 4: Launch Application
Open the published Service Binding.
Select entity ZAB_I_PoDetails.
Click Preview.

The Fiori Elements application will launch automatically. RAP-generated UIs can be previewed directly from the service binding in ADT.

Learning Objectives

This project demonstrates:

CDS View Entity Development
CDS Associations
UI Annotations
Fiori Elements Facets
Object Page Navigation
OData V4 Exposure
RAP Read-Only Applications


Author

Ajay Bishnoi

GitHub Repository:

GitHub: https://github.com/ajaybishnoi029/SAP_RAP_PO_VIEW_APP

License

This project is provided for educational and learning purposes.
