# PDF Information Extraction Script

## Overview

This Python script extracts text, image presence, and metadata from each page of a PDF file. It categorizes pages based on their content and type and then compiles this information into a pandas DataFrame. The DataFrame is displayed in the console and saved as a CSV file for further analysis.

## Requirements

- Python 3.x
- PyMuPDF (`fitz`)
- pandas

You can install the required packages using pip:

```bash
pip install PyMuPDF pandas

## Script Functionality

### Extract Information:

- Opens the specified PDF file using PyMuPDF.
- Iterates through each page to extract:
  - Text content
  - Image presence
  - Metadata (as a dictionary)
- Categorizes each page into one of several types based on its content:
  - **Banner Page**: Contains the text "banner page".
  - **Bad Blank**: Contains the text "bad blank" or follows a blank page.
  - **Blank Page**: Contains the text "good blank" or is blank.
  - **Not Blank**: Contains the text "not blank".
  - **Non Blank**: Has visible content and is not categorized as blank or special.

### Compile Data:

- Constructs a DataFrame with columns for:
  - Document ID (derived from the PDF filename)
  - Page Number
  - Page Type
  - Text Content
  - Image Content (Yes/No)
  - Metadata (as a string)

### Output:

- Displays the DataFrame in a tabular format in the console.
- Saves the DataFrame as a CSV file for easy sharing and analysis.

## Usage

### Set the PDF Path:

- Modify the `pdf_path` variable to point to the location of your PDF file.

### Run the Script:

- Execute the script using Python:
  ```bash
  python script_name.py

