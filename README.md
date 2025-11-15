  # project name:
  Automated Invoice Reconciliation Using OCR & Machine Learning
  
## Project Overview

This project automates the process of invoice reconciliation by extracting text from invoice images using OCR (Optical Character Recognition) and applying machine learning and rule-based logic to detect mismatches in:
             1.Invoice numbers
             2.Vendor names
             3.Invoice dates
             4.Total invoice amounts
It removes the need for manual checking and speeds up the reconciliation workflow.

## Key Features

:-OCR extraction using Tesseract + OpenCV
:-Preprocessing (grayscale, thresholding, noise removal, dilation/erosion)
:-Text → structured fields using Regex
:-Rule-based comparisons
:-Machine Learning mismatch detection 

## Current Status

The project report is uploaded as required.
The full source code will be uploaded soon once execution and testing are completed.

## Planned Folder Structure

📁 Automated-Invoice-Reconciliation
│── 📁 raw_invoices/                 # Folder containing invoice images
│── 📁 src/
│     ├── preprocess.py              # OCR preprocessing
│     ├── ocr_extract.py             # Text extraction
│     ├── field_extraction.py        # Regex field extraction
│     └── reconciliation.py          # ML + rule-based reconciliation
│── invoice_texts.csv                # OCR text output
│── clean_invoice_data.csv           # Extracted structured data
│── requirements.txt                 # Required Python libraries
│── Report.pdf                       # Project report
│── README.md                        # This file

## OCR Preprocessing Techniques Used

These steps significantly improve OCR accuracy on invoice images:
Grayscale Conversion – simplifies image & removes color noise
Gaussian Blur – removes random pixel noise
Adaptive Thresholding – handles non-uniform lighting
Dilation – thickens text so OCR reads faint characters
Erosion – removes extra noise & lines
Opening (Erosion → Dilation) – cleans small spots
Binarization – converts image to pure black & white
Skew Correction – fixes tilted invoice scans
Edge Detection – improves text isolation
Image Resizing (Upscaling) – makes small text readable

## Machine Learning Models Used

As part of the automated invoice reconciliation system, multiple machine learning models were trained and evaluated to classify invoices as:
     i.Matched
     ii.Mismatched

To build the invoice reconciliation classifier, I am going to experiment with the following machine learning models:
1.Logistic Regression:
I will first try Logistic Regression as a baseline model.
It is simple, easy to implement, and useful for binary classification.
This helps me understand how well the basic features perform before moving to advanced models.

2.Random Forest Classifier
After that, I will try a Random Forest, which usually performs well when data is noisy or contains imperfect OCR outputs.
Since it is an ensemble model, it can capture non-linear relationships and is often more accurate.
I expect this model to give the best results.

3️.Support Vector Machine (SVM)
Finally, I will test SVM, which is good for small datasets and works well when the boundary between classes is not linear.
This model may also perform well depending on how clean and structured the extracted invoice features are.

## Summary

I will try all three models — Logistic Regression, Random Forest, and SVM — and then compare their performance.
Whichever model gives the highest accuracy and stability will be selected as the final model for invoice reconciliation.

## Project Report

The full project report is included as:

📘 MACHINE LEARNING PROJECT REPORT.pdf

## Conclusion

In this project, I worked on building an Automated Invoice Reconciliation System using OCR techniques and machine learning. The aim was to extract text from invoice images, clean the data, and automatically match invoice information for reconciliation.
Although the full execution and model training are pending, I planned to test the following machine learning algorithms for classification and decision-making in the system:
     Logistic Regression – to build a simple baseline model.
     Support Vector Machine (SVM) – to capture non-linear patterns in the extracted text features.
     Random Forest Classifier – expected to give the best performance due to its robustness, ability to handle messy real-world data, and strong accuracy in previous OCR-based tasks.
Based on how these models typically perform on similar datasets, Random Forest is expected to achieve the highest accuracy for this project. It handles noise, missing values, and complex patterns better than the other models.
Overall, the project establishes a complete workflow for invoice reconciliation using OCR preprocessing (grayscale, thresholding, denoising), text extraction using Tesseract, and planned machine learning models for final matching. The system can be further improved once the models are executed and evaluated with actual dataset results.
