# test_automation_ui

This project contains a Playwright-based automated test for the image preview functionality of the Image Resizing feature on [pixelssuite.com](https://www.pixelssuite.com).

---

## Project Structure

```
test_automation_ui/
├── image_preview_test.py   → Main Playwright test script
├── execution_results.csv   → Auto-generated test results
├── sample.png              → Sample PNG image used in the test
├── Commands.txt            → All commands in one place
├── README.md               → Project documentation
└── results/
    └── preview_pass.png    → Screenshot taken during test execution
```

---

## Prerequisites

- Python 3.11 or 3.12
- Google Chrome browser
- Internet connection

---

## Installation

Open Command Prompt and navigate to the project folder:

```
cd C:\path\to\test_automation_ui
```

Then run the following commands one by one:

```
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## Running the Test

```
python3 image_preview_test.py --url "https://www.pixelssuite.com/convert-to-png" --slow-mo-ms 200
```

---

## What the Test Does

1. Opens a Chrome browser automatically
2. Navigates to the Image Resizing page on pixelssuite.com
3. Uploads the sample PNG file
4. Checks whether a preview image is displayed after upload
5. Takes a screenshot of the result
6. Saves the result to execution_results.csv

---

## Test Scenario Details

| Field | Details |
|---|---|
| TC ID | Pos_0009 |
| Feature | Image Resizing |
| Type | Positive Test Case |
| Input | Valid PNG image file |
| Expected Output | Uploaded image is displayed in the preview section |

---

## Checking Results

After the test runs:

- Open `execution_results.csv` — should contain one data row
- Open `results/preview_pass.png` — should show a screenshot of the page

---

## Notes

- Do not close the browser manually while the test is running
- If the test times out, increase the timeout: `--timeout-ms 90000`
- Make sure `sample.png` exists in the project folder before running
