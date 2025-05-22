 
Cyberclan Real-Time Threat Assessment via IP Camera Feed

This project, developed by Cyberclan, is a first working prototype of a real-time cybersecurity assistant. It captures live video from an IP camera, detects and extracts on-screen text using OCR, identifies cybersecurity-related questions, and answers them using a local LLM (Mistral 7B in GGUF format).

> Final Vision: The end product will use smart lenses with an integrated camera, streaming video in real time to our software for hands-free, real-world cybersecurity assistance in dynamic environments such as conferences, SOC rooms, or security training simulations.



Features

Real-time video capture from an IP camera

Optical Character Recognition (OCR) with Tesseract

Automatic detection of cybersecurity-related questions in video feeds (e.g., from training sessions, posters, or whiteboards)

Offline local LLM-based answering (no internet required)

Visual feedback using OpenCV with potential to highlight threat-related queries


Requirements

Python 3.8+

OpenCV

pytesseract

llama-cpp-python

A GGUF LLM model like mistral-7b-instruct-v0.1.Q4_K_M.gguf

Tesseract OCR installed and accessible in PATH


Installation

git clone https://github.com/psycho237-prog/Quizbox-AI-
cd Quizbox-AI-
pip install -r requirements.txt

Install Tesseract OCR (Linux)

sudo apt update
sudo apt install tesseract-ocr

Usage

1. Update the IP camera URL in main.py:



ip_camera_url = 'http://your-camera-ip:port/video'

2. Set the path to your local .gguf LLM model:



llm = Llama(model_path="path/to/your-model.gguf")

3. Run the application:



python main.py

Press q to exit the video window.

Model Download

Download the Mistral GGUF model from HuggingFace:

https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF


Place it in your project directory or update the model path accordingly.

Example Output

QUESTION: What is phishing?
ANSWER : Phishing is a type of cyber attack where attackers trick users into revealing sensitive information by pretending to be a trusted entity...

License

MIT License — open for use, contributions, and enhancements by the cybersecurity community.

Author

Cyberclan — developed by Onana Gregoire Legrand

Community

Join our Cyberclan community on LinkedIn:
https://www.linkedin.com/groups/13252179

