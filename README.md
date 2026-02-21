# TOPSIS - Technique for Order Preference by Similarity to Ideal Solution

A practical toolkit for performing TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) based multi-criteria decision analysis. This project is available both as a Python command-line utility and a modern browser-based web application.

---

## Description

TOPSIS is a widely used multi-criteria decision-making (MCDM) technique that helps determine the most suitable alternative by comparing how close each option is to the ideal best and ideal worst solutions.

This repository provides two implementations:

1. **Command-Line Tool** (`topsis.py`) – suitable for batch processing and scripting  
2. **Web Service** (`index.html`) – interactive browser application with a modern UI  

---

## 🖥️ Command-Line Tool

### Requirements

- Python 3.x  
- pandas  
- numpy  
- openpyxl (for Excel file support)

### Installation

Install the required dependencies using pip:

```bash
pip install pandas numpy openpyxl
Usage
python topsis.py <InputDataFile> <Weights> <Impacts> <OutputResultFileName>
Parameters

InputDataFile: Path to the decision matrix file (CSV or XLSX format)

Weights: Comma-separated weights for each criterion (e.g., "1,1,1,1")

Impacts: Comma-separated impact symbols. Use + for beneficial criteria and - for non-beneficial criteria (e.g., "+,+,-,+")

OutputResultFileName: Path where the output file will be saved (CSV or XLSX)

Input File Format

The input file must be in CSV or XLSX format with the following structure:

First column: Alternative names/identifiers

Remaining columns: Numeric values for each criterion

Example
Alternative	Criterion1	Criterion2	Criterion3	Criterion4
A1	0.5	0.3	0.2	0.4
A2	0.6	0.4	0.3	0.5
A3	0.4	0.5	0.4	0.3

Note: The input file must contain at least three columns (one for alternatives and at least two criteria).

Example
python topsis.py data.xlsx "1,1,1,1" "+,+,-,+" output.xlsx

This command will:

Read the decision matrix from data.xlsx

Apply equal weights to all criteria

Treat the third criterion as non-beneficial

Calculate TOPSIS scores and rankings

Save the results to output.xlsx

Output

The output file will contain:

All original columns from the input file

Topsis Score – calculated relative closeness (higher is better)

Rank – ranking of alternatives (1 indicates the best option)

How TOPSIS Works

Normalization – removes unit differences between criteria

Weighted Normalization – multiplies normalized values by weights

Ideal Solutions – identifies ideal best and worst values

Distance Calculation – computes Euclidean distance from ideals

TOPSIS Score – calculates relative closeness

Ranking – orders alternatives by score

Error Handling

The tool will display errors and exit if:

Input file is not found

Unsupported file format is used

Input file has fewer than three columns

Non-numeric values appear in criteria columns

Number of weights/impacts does not match criteria count

Invalid impact values are provided

Incorrect number of command-line arguments

🌐 Web Service

A pure client-side web application for TOPSIS analysis. All computations run directly in the browser using JavaScript — no backend required.

Web Service Features

✅ Pure frontend implementation

✅ Drag & drop file upload

✅ Real-time data preview

✅ Interactive results visualization

✅ JavaScript-based TOPSIS computation

✅ Automatic file download

✅ Email integration via EmailJS

✅ Responsive modern UI

✅ Robust XLSX support

Web Service Usage

Open index.html in a modern web browser

Upload your CSV or XLSX file

Enter weights (comma-separated)

Enter impacts (+ or -)

Provide your email address

Click Process TOPSIS Analysis

View and download the results

📄 License

This project is open source and available for use.


---

✅ This will render like your **2nd screenshot**  
✅ Proper heading hierarchy  
✅ Clean GitHub styling  
✅ Humanized text  

---

If you want 🔥 I can next:

- add badges  
- add screenshots section  
- make it resume-level professional  
- add PyPI packaging section  

Just say the word.
