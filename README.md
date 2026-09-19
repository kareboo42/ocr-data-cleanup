# OCR Data Cleanup Tool

A Python project that extracts text from an image using OCR, then cleans and structures the messy output into validated, usable tabular data.

## What it does

1. Generates/loads a receipt-style image
2. Uses Tesseract OCR (via pytesseract) to extract raw text from the image
3. Parses the unstructured OCR output using regex to identify item/price pairs
4. Applies a correction step to fix common OCR misreads
5. Loads the cleaned data into a pandas DataFrame and exports it to CSV
6. Runs a validation check, summing extracted item prices and comparing against the receipt's stated subtotal to catch potential OCR errors

## Skills demonstrated

- OCR (Optical Character Recognition) - converting image-based text into machine-readable text
- Regex pattern matching - extracting structured fields from unstructured text
- Data cleaning - correcting known OCR misreads, fixing malformed numeric data
- Data validation - cross-checking extracted totals against source data
- pandas - structuring and exporting tabular data

## Tech stack

- Python
- pytesseract + Tesseract OCR - text extraction from images
- Pillow (PIL) - image handling
- pandas - data structuring
- re (regex) - text pattern matching

## How to run it

1. Install Tesseract OCR: https://github.com/UB-Mannheim/tesseract/wiki
2. Install Python dependencies:
   pip install pytesseract pillow pandas
3. Update the tesseract_cmd path in the notebook to match your install location
4. Open the notebook in Jupyter and run all cells

## Output

- receipt_data.csv - structured, cleaned item/price data extracted from the receipt image

## Note on accuracy

OCR is not perfectly accurate. This project intentionally demonstrates handling real-world OCR imperfections (misread characters, missing decimal points) rather than using a flawless source image, since that reflects realistic data-cleaning work.
