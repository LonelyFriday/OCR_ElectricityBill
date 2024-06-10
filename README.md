# Thai OCR with Preprocessing and Text Correction
This Python script demonstrates how to perform Optical Character Recognition (OCR) on Thai and English text using the Tesseract OCR engine and the ThaiNLP library for text correction in Google Colab.

## Prerequisites
- Python 3.x
- OpenCV (cv2)
- Tesseract OCR Engine (pytesseract)
- ThaiNLP (pythainlp) 
- Google Colab Patches (cv2_imshow) [optional]

## Preprocessing
The preprocess_image() method applies the following preprocessing steps to improve OCR accuracy:
1. Converts the image to grayscale.
2. Adjusts the brightness and contrast of the image.
3. Applies thresholding to the image.

## Text Extraction
The extract_text_eng() and extract_text_thai() methods use the Tesseract OCR engine to extract text from the preprocessed image. The --oem 3 --psm 6 configuration is used for English text, while "-l that" is added for Thai text.

## Text Correction
The correct_text() method uses the ThaiNLP library to correct the extracted text. It tokenizes the text using the word_tokenize() function with the newmm engine and then joins the corrected tokens back into a single string.

## Conclusion
This script demonstrates how to perform OCR on Thai and English text with preprocessing and text correction using Python. By combining OpenCV, Tesseract OCR, and ThaiNLP, you can achieve accurate text extraction and correction from images.
