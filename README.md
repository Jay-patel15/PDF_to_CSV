PDF to CSV Converter for University Results
This project is a Python-based solution for extracting, processing, and converting Mumbai University result PDFs into a structured CSV format. The tool uses regex patterns, named tuples, and pandas for data extraction, manipulation, and storage, providing an efficient way to parse unstructured PDF data into a tabular format.

Features
PDF Parsing: Utilizes pdfplumber to extract text from the result PDF.
Regex-based Data Extraction:
Extracts student details, including seat numbers and names.
Captures subject-wise marks, totals, remarks, and categories.
Fetches computed fields like C, G, GP, C*G, and totals.
Data Organization:
Assigns extracted values to specific columns.
Creates structured data using named tuples and DataFrames.
Data Merging: Combines multiple DataFrames to produce a comprehensive dataset.
Output: Saves the final processed data into a CSV file for further analysis.
Requirements
Install the necessary libraries before running the script:

bash
Copy code
pip install pdfplumber pandas
Project Workflow
PDF Input:
Provide the input PDF file containing Mumbai University results.

Text Extraction:
Extracts text from a specified page of the PDF for processing.

Data Extraction:

Regex patterns identify and extract:
Seat numbers and student names.
Subject-wise marks for theory and labs.
Remarks, totals, and computed grades.
Data Structuring:
Organizes extracted data into multiple DataFrames.

Data Merging:
Combines the structured DataFrames into a single, comprehensive DataFrame.

CSV Export:
Exports the final dataset to a CSV file (data.csv).

Usage
Place the result PDF in the project directory and update the file name in the script:

python
Copy code
ap = "data.pdf"  # Update this with your file name
Run the script:

bash
Copy code
python script_name.py
Find the generated CSV file (data.csv) in the project directory.

Output Example
The output CSV contains the following columns:

Student Details: Seat Number, Name.
Marks: Subject-wise marks for theory and lab exams.
Remarks: Remarks like Pass/Fail, Reappear categories, etc.
Total Scores: Computed totals and grades.
Dependencies
The project depends on the following libraries:

pdfplumber: For parsing and extracting text from PDFs.
pandas: For data manipulation and storage.
re: For regex-based data extraction.
Customization
To modify the script for other types of result PDFs:

Update the regular expressions for data extraction.
Adjust the DataFrame schema to match the new data structure.
Contributing
Contributions are welcome! If you encounter any issues or have suggestions for improvements, feel free to create a pull request or open an issue.

