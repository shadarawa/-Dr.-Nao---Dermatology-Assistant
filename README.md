

# Dr. Nao - Dermatology Assistant

An educational robotics and AI demonstration project that combines the NAO humanoid robot, a web based dermatology interface, and a pre trained skin lesion classification model to create an interactive assistant for skin lesion image analysis.

This project was developed as a demonstration oriented academic prototype showing how robotics, computer vision, and medical AI can be integrated into a single interactive workflow.

---

## Overview

Dr. Nao - Dermatology Assistant allows a user to:

• upload a skin lesion image through a web interface  
• capture an image from a laptop camera  
• capture an image from a NAO connected camera pipeline  
• run image classification using a pre trained dermatology model  
• display the predicted lesion class with confidence scores  
• present the result visually in the interface  
• generate a spoken style explanation through the NAO interaction flow  

The system is designed for educational demonstration purposes only and is intended to showcase human robot interaction combined with AI based image analysis.

---

## Key Features

• interactive web based diagnosis interface  
• support for uploaded skin lesion images  
• laptop camera capture workflow  
• NAO camera capture workflow  
• skin lesion prediction with top ranked class probabilities  
• NAO oriented interaction and speech pipeline  
• clean demonstration flow for academic presentations and exhibitions  

---
## Project Screenshots

### Home Interface

<img width="1834" height="807" alt="image" src="https://github.com/user-attachments/assets/1c800a71-8c0a-41d7-9d0b-5bcb177133a7" />
<img width="1713" height="864" alt="image" src="https://github.com/user-attachments/assets/cfff461a-dcca-46b6-8ebc-777b18a2ad6b" />


### Upload and result View
<img width="1741" height="916" alt="image" src="https://github.com/user-attachments/assets/d4461d9a-cded-4dab-ad74-08c78572ff9e" />
<img width="1694" height="832" alt="image" src="https://github.com/user-attachments/assets/71c7e657-9d26-49fd-a7fa-d786a7e68c9f" />



### NAO Camera Capture View

<img width="1705" height="831" alt="image" src="https://github.com/user-attachments/assets/b8341234-2c37-4098-a84c-471e5a2c56a8" />
<img width="1609" height="789" alt="image" src="https://github.com/user-attachments/assets/778d7768-b041-4902-8d53-9345296d2bfa" />


### NAO Camera Result

<img width="1473" height="896" alt="image" src="https://github.com/user-attachments/assets/66aac2ed-bfcc-43ee-b1d9-7718b39ca2e5" />


### Diagnosis Result


###  admin page
<img width="1028" height="787" alt="image" src="https://github.com/user-attachments/assets/1c8eb673-46e3-4e12-ac8c-612cc0cf4a31" />



---
### video tutorial
https://drive.google.com/file/d/1IBy1_i3tBsj_oRGafgVte41f2RhrIHpW/view?usp=sharing

## System Workflow
The user opens the web interface.
The user either:
○ uploads a skin lesion image, or
○ captures an image from the laptop camera, or
○ captures an image from the NAO camera workflow.
The backend processes the image.
The image is passed to the pre trained skin lesion classification model.
The predicted class and confidence scores are returned.
The result is displayed on the web interface.
A NAO compatible explanation or speech output can be triggered as part of the demo flow.


## Technologies Used

• Python
• FastAPI / backend serving components
• HTML / CSS / JavaScript
• PyTorch
• NAOqi / NAO integration workflow
• computer vision and image preprocessing
• web based interaction interface

## Model Attribution

This project uses a pre trained skin lesion classification model from:

iamhmh / derm-cnn-ham10000
 https://huggingface.co/iamhmh/derm-cnn-ham10000

The project uses that model as part of an educational demonstration workflow for skin lesion image analysis. The original model page states that the model weights are licensed under CC BY-NC 4.0 and the code is licensed under MIT. Please review the original source and its license terms before reuse or redistribution.

## Important License and Usage Notice

This repository is shared in a clean academic and demo form.

• The pre trained model file is not included in this repository.
• Users should download the model from the original upstream source when needed.
• The upstream model weights are marked for non commercial use on the source page.

Accordingly, this project should be treated as:

• educational
• academic
• demonstration oriented
• non commercial


## Medical Disclaimer

This project is intended for educational and demonstration purposes only.

It is not a medical device and must not be used for:

• medical diagnosis
• treatment decisions
• clinical decision making
• professional dermatological judgment

The upstream model page also includes a diagnostic use disclaimer, so any use of this system should remain strictly within safe educational and demo boundaries.

 
## Setup Instructions
1. Clone the repository
git clone https://github.com/ghayda-njaafreh/skin_nao_demo.git
cd skin_nao_demo
2. Create and activate a virtual environment

# Windows

python -m venv .venv
.venv\Scripts\activate

# Linux / macOS

python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

## Download the model weights

Download the required trained model weights from the original source:

https://huggingface.co/iamhmh/derm-cnn-ham10000

Then place the downloaded model file in the local path expected by the prediction code, and update the path in the source code if needed for your environment.

Note: the model file is intentionally not included in this repository.


## Configure local paths and device specific settings

Before running the project, update local configuration values inside the code such as:

• NAO_IP
• PYTHON2_PATH
• NAO_CAMERA_SERVER_URL
• YOUR_BACKEND_IP
• any local SDK or runtime paths

Example placeholders:

NAO_IP = "YOUR_NAO_IP"
PYTHON2_PATH = r"C:\Path\To\Python27\python.exe"
NAO_CAMERA_SERVER_URL = "http://YOUR_NAO_CAMERA_SERVER_IP:5000/snapshot"


# Run the backend

From the project directory, run the backend server:

uvicorn skin_nao_demo.main:app --reload

# Open the web interface

Open the frontend file from the skinnaoweb folder in your browser, or serve it locally using a simple static server if needed.

## Notes for NAO Integration

This project includes a NAO oriented interaction pipeline. To use it correctly, you may need:

• a configured NAO robot or virtual environment
• compatible Python and SDK setup for NAO communication
• correct network IP configuration
• proper local runtime paths for robot communication scripts

Because NAO environments differ between machines, some paths and settings must be adjusted manually for your device.

What Is Included in This Repository

Included:

• source code
• frontend interface
• backend logic
• prediction pipeline code
• NAO interaction scripts
• screenshots
• documentation

Not included:

• pre trained model weights
• runtime logs
• temporary uploads
• captured user images
• private environment files

##  Contributors

This project was developed by:

• shadarawa
• ghayda-njaafreh


 ## Academic / Demonstration Context

This project was developed as an academic style prototype demonstrating how:

• humanoid robotics
• AI based image classification
• interactive web systems
• medical themed assistive interfaces

can be combined into one integrated demonstration platform.

It is especially suitable for:

• university demos
• academic exhibitions
• robotics presentations
• AI demonstration events

## Future Improvements

Possible future directions include:

• improved UI and UX design
• live NAO voice interaction enhancements
• better deployment packaging
• configurable model loading
• multi model comparison
• safer and more modular medical AI demo workflows
• stronger environment configuration handling

##  Citation / Acknowledgment

If you use or adapt this project for an academic demonstration, please also acknowledge the original upstream model source:

iamhmh / derm-cnn-ham10000 

https://huggingface.co/iamhmh/derm-cnn-ham10000

##  Contact

For academic or demo collaboration or project discussion, please use the repository issues section or your preferred GitHub contact method.


## Project Structure

```text
.
├── nao.py
├── nao_camera_server/
│   └── server.py
├── skin_nao_demo/
│   ├── inference.py
│   ├── labels.json
│   ├── main.py
│   ├── model.py
│   ├── nao_speaker.py
│   ├── predictor.py
│   └── test_predictor.py
├── skinnaoweb/
│   ├── index.html
│   └── other frontend assets
├── assets/
│   └── screenshots/
│       ├── home-interface.png
│       ├── upload-and-camera-view.png
│       ├── nao-camera-capture-view.jpeg
│       ├── nao-camera-result-nevus.jpeg
│       └── diagnosis-result-bcc.jpeg
├── requirements.txt
├── .gitignore
└── README.md
