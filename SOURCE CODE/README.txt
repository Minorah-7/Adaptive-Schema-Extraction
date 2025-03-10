Source Code Documentation
This folder contains the implementation of the Adaptive Schema Extraction project, organized by development stages. Below are instructions to set up dependencies, execute the code, and customize the extraction process.

Directory Structure
Copy
source_code/
├── stage1_text_extraction/      # Code for Stage 1 (Basic OCR + ROI)
├── stage2_full_image_processing/ # Code for Stage 2 (Full-Image Extraction)
├── stage3_adaptive_roi/         # Code for Stage 3 (Priority-Based ROI Extraction)
├── utils/                       # Helper scripts and configurations
├── app.py                       # Streamlit web application
└── requirements.txt             # Dependency list
Installation
Prerequisites:

Python 3.8+

Tesseract OCR Engine (Installation Guide)

Install Dependencies:

bash
Copy
pip install -r requirements.txt
Key dependencies:

OpenCV (opencv-python)

PyTesseract (pytesseract)

Pandas (pandas)

Streamlit (streamlit)

Configure Tesseract Path (if not in system PATH):

python
Copy
# In your Python script:
pytesseract.pytesseract.tesseract_cmd = r'<your_tesseract_installation_path>'
Execution Steps
Stage 1: Basic Text Extraction
Place input images in /dataset/stage1_samples/

Run:

bash
Copy
python stage1_text_extraction/stage1_aadhar_extraction.py --input <image_path> --output <output_csv_path>
Stage 2: Full-Image Processing
bash
Copy
python stage2_full_image_processing/stage2_engineering_drawing_extractor.py --input <drawing_image_path> --excel_output <output.xlsx>
Stage 3: Adaptive ROI Extraction
Configure ROIs in stage3_adaptive_roi/roi_config.json:

json
Copy
{
  "roi_1": {
    "coordinates": [x1, y1, x2, y2],
    "priority": 1,
    "label": "material_spec"
  }
}
Execute:

bash
Copy
python stage3_adaptive_roi/adaptive_extraction.py --input <drawing_path> --config roi_config.json --output <data.xlsx>
Streamlit Web Interface
bash
Copy
streamlit run app.py
Access via http://localhost:8501 after execution.

Customization Guide
ROI Adjustment: Modify coordinates in roi_config.json for different drawing formats

Output Formatting: Edit utils/excel_writer.py to change Excel column structure

OCR Tuning: Adjust PyTesseract parameters in utils/ocr_processor.py:

python
Copy
config = '--psm 6 --oem 3 -c tessedit_char_whitelist=0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ'
Testing
Sample images are provided in /dataset/test_images/. Run:

bash
Copy
python -m pytest tests/
Troubleshooting
Tesseract Path Errors: Verify installation path in pytesseract.pytesseract.tesseract_cmd

Dependency Conflicts: Use a virtual environment

Image Format Issues: Convert images to PNG/JPG before processing

For detailed project rationale and methodology, refer to the main README.

This inner README provides technical execution details while linking to the high-level documentation in the main README. It includes actionable commands and configuration examples for developers working directly with the codebase.