# README for Source Code Folders (Stage 1, Stage 2, Stage 3)

This README provides an overview of the source code in the `Stage 1`, `Stage 2`, and `Stage 3` folders. Each stage corresponds to a specific part of the project, focusing on different tasks such as data extraction, preprocessing, and analysis.

---

## **Stage 1: Data Extraction from Aadhaar**
### **Overview**
This stage focuses on extracting specific information from Aadhaar card images, such as the Aadhaar number and name. The code uses predefined ROIs to crop relevant sections of the image and applies OCR to extract text.

### **How It Works**
1. **Image Loading**:
   - Aadhaar card images are loaded using OpenCV and PIL.

2. **ROI Cropping**:
   - Predefined ROIs are used to crop sections of the image containing the Aadhaar number and name.

3. **Text Extraction**:
   - The `pytesseract` library extracts text from the cropped regions.
   - Extracted text is cleaned and stored in a DataFrame.

4. **Data Storage**:
   - The extracted data is saved to an Excel file (`aadhaar_details.xlsx`).

### **Key Features**
- Predefined ROIs for accurate cropping.
- Handles variations in Aadhaar card layouts.
- Saves extracted data in a structured format.

### **Usage**
1. Place Aadhaar card images in the specified folder.
2. Run the script to extract Aadhaar numbers and names.
3. The extracted data is saved in `aadhaar_details.xlsx`.

## **Stage 1: Data Extraction from Recipts**


### **Overview**
This stage focuses on extracting structured data from receipt images using Optical Character Recognition (OCR). The code processes images, identifies key regions of interest (ROIs), and extracts text such as store names, dates, and total amounts.

### **How It Works**
1. **Image Preprocessing**: 
   - Images are loaded and converted to grayscale for better OCR accuracy.
   - Adaptive thresholding is applied to enhance text visibility.

2. **Text Extraction**:
   - The `pytesseract` library is used to extract text from predefined ROIs.
   - Regular expressions are applied to identify store names, dates, and total amounts.

3. **Data Storage**:
   - Extracted data is stored in a Pandas DataFrame and saved to an Excel file (`receipt_data.xlsx`).

### **Key Features**
- Supports multiple receipt formats.
- Handles noisy images with preprocessing techniques.
- Extracts structured data for further analysis.

### **Usage**
1. Place receipt images in the `receipts_img` folder.
2. Run the script to process all images and extract data.
3. The extracted data is saved in `receipt_data.xlsx`.


## **Stage 2&3: Engineering Drawing Data Extraction**

### **Overview**
This stage focuses on extracting text from engineering drawings. The code processes images, identifies horizontal and vertical ROIs, and extracts text using OCR.

### **How It Works**
1. **Image Cropping**:
   - Images are cropped to focus on specific regions of interest (ROIs).

2. **ROI Definition**:
   - Horizontal and vertical ROIs are defined to capture text from different parts of the drawing.

3. **Text Extraction**:
   - The `pytesseract` library extracts text from the defined ROIs.
   - Extracted text is stored in a DataFrame.

4. **Data Storage**:
   - The extracted data is saved to an Excel file (`extracted_ed.xlsx`).

### **Key Features**
- Supports multiple ROIs for comprehensive text extraction.
- Handles complex engineering drawings.
- Saves extracted data in a structured format.

### **Usage**
1. Place engineering drawing images in the specified folder.
2. Run the script to extract text from the drawings.
3. The extracted data is saved in `extracted_ed.xlsx`.

---

## **Installation and Dependencies**
To run the code in all stages, install the required libraries using the following commands:

```bash
pip install opencv-python numpy pytesseract openpyxl pandas keras-ocr
```

Additionally, ensure Tesseract OCR is installed on your system and update the `pytesseract.pytesseract.tesseract_cmd` path in the code.

---

## **Output Files**
- **Stage 1**: `receipt_data.xlsx` (Extracted receipt data).
- **Stage 2**: `aadhaar_details.xlsx` (Extracted Aadhaar card data).
- **Stage 3**: `extracted_ed.xlsx` (Extracted engineering drawing data).

---

## **Notes**
- Modify the input and output folder paths in the code as needed.
- Ensure images are clear and properly aligned for accurate text extraction.
- For best results, use high-quality images with minimal noise.

---

This README provides a high-level overview of the code in each stage. For detailed implementation, refer to the source code in the respective folders.
