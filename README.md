# AI Engineer Coding Challenge

## Overview

Build a Python-based service that extracts structured invoice data from both **scanned** and **digital** PDF invoices, using a mix of OCR and AI models.

---

## Task

Create a RESTful API with the following capabilities:

- Accept one or more PDF invoices via an API.
- Detect whether each PDF is scanned (image-based) or digital (text-based).
- Extract these fields from each invoice:
  - `invoice_number`
  - `invoice_date`
  - `vendor_name`
  - `total_amount`
- Return structured JSON output for each processed file.

---

## API Specification (suggested)

- `POST /extract`  
  Accepts one or more PDF files (`multipart/form-data`).  
  Returns JSON array of extraction results per invoice.

- `GET /health`  
  Simple health check endpoint returning `{ "status": "ok" }`.

---

## Example Output

```json
{
  "invoice_number": "INV-12345",
  "invoice_date": "2024-07-10",
  "vendor_name": "Acme Corp",
  "total_amount": 1025.75
}
```

## Things We Value

- Clean, well-structured, and maintainable code.
- Automated tests covering core functionality.
- Thoughtful error handling and edge case coverage.

## Stretch Goals

- Containerise the application
- Extract line items in the invoice (list with description, qty, unit_price, line_total)
- What are the challenges/limitations and possible improvements
- Be creative! Try to extend or implement interesting functionalities using LLMs in the accounting/finance space (you can take inspiration from some use cases at [Attelas.ai](https://attelas.ai)).

## Submission

Please submit a link to a GitHub repository with your solution, including a brief `README.md` file explaining how to run the project.
Good luck! We look forward to seeing your solution.
