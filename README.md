# AI Order Automation Tool (Wine Distribution)

## Overview
This project is an AI-powered order parsing tool designed to convert unstructured customer orders (text, email, or notes) into clean, structured data for faster and more accurate entry into business systems like Sage.

## Problem
In many distribution environments, customer orders are received in inconsistent formats (calls, texts, emails), requiring manual entry into inventory systems. This leads to:
- Data entry errors  
- Time inefficiencies  
- Inventory mismatches  
- Financial discrepancies over time  

## Solution
This tool uses AI to automatically extract and structure order data, reducing manual work and improving accuracy.

## Features
- Parses raw customer orders into structured JSON
- Identifies customer name, product, quantity, and unit
- Normalizes common product names (e.g., “cab” → “cabernet”)
- Designed to integrate with inventory systems like Sage
- Optional logging system for tracking discrepancies (future feature)

## Example

### Input
"Need 2 cases Modelo, 1 cab, 3 pinot for Aspen Grill"

### Output
{
  "customer_name": "Aspen Grill",
  "items": [
    {"product_name": "Modelo", "quantity": 2, "unit": "case"},
    {"product_name": "Cabernet", "quantity": 1, "unit": "case"},
    {"product_name": "Pinot", "quantity": 3, "unit": "case"}
  ]
}

## Tech Stack
- Python
- AI API (Claude / OpenAI)
- JSON processing
- Google Sheets (for output integration)

## Why I Built This
I currently work in a wine distribution environment where order entry is done manually using outdated systems. I identified an opportunity to reduce errors, save time, and improve operational efficiency by automating the order parsing process.

## Future Improvements
- Direct integration with Sage ERP
- Email and SMS auto-processing
- Inventory validation and mismatch detection
- Dashboard for order tracking and analytics

## Status
In progress — actively testing with real-world order examples and improving parsing accuracy.

## Author
Seth Soto
