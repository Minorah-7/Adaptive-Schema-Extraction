# Adaptive Schema Extraction: A Multi-Stage Learning Approach for Manufacturing Drawing Interpretation.
Research project focusing on automated extraction of data from engineering drawings. Implemented a progressive ROI refinement methodology.

**This project was a collaborative effort by Team Matrix, consisting of three team members:**
1. Owais Hussain: [GitHub](https://github.com/owais-syed) , [LinkedIn](https://www.linkedin.com/feed/)
2. Jyothindra Pallikonda: [Git Hub](https://github.com/jyothindrapallikonda)  , [Linkedin](https://www.linkedin.com/in/jyothindrapallikonda/) 
3. Minorah Palli: [GitHub](https://github.com/Minorah-7)  , [Linkedin](https://www.linkedin.com/in/minorah-palli-01b286266?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)

**Project Overview:**  
In manufacturing industries, extracting data from engineering drawings plays a vital role in automating machine processes and ensuring production accuracy. Traditionally, this process is done manually, which can be both time-consuming and error-prone. Our project aims to automate this task, using image recognition and text extraction techniques to pull relevant data directly from engineering drawings, reducing the chance for mistakes and speeding up the workflow.
The project is divided into three key stages, each focusing on progressively improving the accuracy and adaptability of the extraction process. Below is a brief overview of each stage:

**Stage 1: Text Extraction from Images**  
In the first stage, we focused on extracting text from basic images using PyTesseract (OCR) and Region of Interest (ROI) techniques. For this, we used Aadhar card images and bills to practice text extraction, identifying key sections of the image for data retrieval. The process involved selecting specific regions where text appeared and running OCR on these sections.

**Approach**: PyTesseract for OCR, ROI-based extraction.  
**Outcome**: We successfully extracted text from selected image regions (like Aadhar cards and bills).


**Stage 2: Engineering Drawing Text Extraction without ROI**  
In the second stage, we moved on to engineering drawings, attempting to extract text from the entire image without manually defining regions of interest. The extracted content was then pushed into an Excel file for further analysis.  

**Approach**: Full image text extraction without predefined ROIs.
**Drawback**: This approach was limited to similar types of images. It only worked well on a specific type of engineering drawing, and its performance varied with different drawings.

![output_drawing_with_stamps_3_png rf 04e7dfa668137fe2426cdc454faeddf4](https://github.com/user-attachments/assets/db69c764-2f5d-42f4-9d7e-698e4c405f4d)

**Stage 3: ROI-based Text Extraction for Engineering Drawings**  
In the final stage, we introduced a more refined approach using Region of Interest (ROI) with both vertical and horizontal parameters. By manually fixing the coordinates of the ROIs, we ensured consistent and reliable data extraction from engineering drawings. Each ROI had a specific priority, which allowed us to extract relevant data (such as dimensions, tolerances, materials, etc.) and store it in an organized Excel format.  

**Approach**: Custom ROI setup for each engineering drawing, extracting labeled data to Excel.  
**Outcome:** The extraction became more adaptable to different kinds of engineering drawings because of the ability to adjust ROIs and prioritize areas of the image.

![Capture](https://github.com/user-attachments/assets/e622fa4e-d0fc-47b8-86af-eaa0ac46e8e7)

**Try it out** @ https://adaptiveschemaextraction-4qf2ry7zxvpisblv3zdiqd.streamlit.app/


https://github.com/user-attachments/assets/022fc860-daea-4211-97bd-22a4c2e1a37a



**Key Benefits:**  
**Stage 1**: Demonstrated basic OCR text extraction capabilities.  
**Stage 2:** Enabled full-image extraction, though with limitations regarding adaptability.  
**Stage 3:** Achieved scalable, accurate extraction with ROI prioritization, adaptable to various engineering drawings.
This multi-stage approach provides a comprehensive solution for automating the extraction of key data from engineering drawings, making it adaptable across different industries and machine types. As we continue to refine this process, our solution aims to reduce manual input, eliminate errors, and significantly improve the efficiency of manufacturing operations.
"


![Capture56](https://github.com/user-attachments/assets/0304c0ce-aeeb-47d6-a9c6-c8f41b2a695f)

