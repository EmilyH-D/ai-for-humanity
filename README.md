AI for Humanity: ASL Recognition & Visual Assistant

An accessible, AI-powered web platform designed to bridge communication gaps for the Deaf and Hard of Hearing community while assisting visually impaired users. Built using MediaPipe, TensorFlow.js, and browser-native APIs, this platform runs directly in the browser via static web hosting without requiring complex backend servers.

Live Demo

Check out the deployed version of this project on GitHub Pages:
https://emilyh-d.github.io/ai-for-humanity/

Features

Real-Time ASL Recognition: Analyzes hand movements via live webcam feeds using MediaPipe HandLandmarker and classifies ASL alphabet signs using custom TensorFlow.js models.

Dynamic Message Builder: Allows users to build full words and sentences letter-by-letter with instant delete, space, and clear functionalities.

ASL Text-to-Fingerspelling Visualizer: Converts typed text into individual ASL hand signs for educational display.

Audio Speech Synthesis: Includes speech engine integration (window.speechSynthesis) for pronouncing spelled words or providing auditory feedback for visual assistance.

100% Client-Side Execution: Runs securely and privately over HTTPS inside the user's web browser—no external Python servers or backend pipelines needed for web deployment.

Built With

HTML5 / CSS3 / JavaScript (ES6 Modules)

TensorFlow.js: Client-side neural network execution

MediaPipe Tasks Vision: High-precision 21-point 3D hand tracking

Web APIs: navigator.mediaDevices.getUserMedia (Camera access) & SpeechSynthesis

Python (Supplemental): OpenCV, PyTorch, YOLOv8, and Google Gemini API setup for local development experiments

Project Structure

ai-for-humanity/
│
├── index.html                  # Main real-time ASL camera recognition interface
├── avatar.html                 # Text-to-ASL fingerspelling animation visualizer
├── capture.html                # Camera capture & snapshot analysis interface
├── README.md                   # Project documentation
│
└── python-tools/               # Supplemental backend scripts (Local testing)
    ├── agent_detection.py      # Python backend sign detection prototype
    └── yolo_trainer.py         # YOLO/OpenCV object detection experiment


Getting Started Locally

Option A: Web Browser (Recommended)

Because the core application is built with static web technologies:

Clone or download this repository:

git clone https://github.com/EmilyH-D/ai-for-humanity.git
cd ai-for-humanity


Open index.html using a local web server (such as VS Code Live Server or Python's HTTP server):

python -m http.server 8000


Open your browser and navigate to http://localhost:8000.

Note: Browsers require a secure context (http://localhost or https://) to enable webcam permissions via getUserMedia. Double-clicking index.html directly as a local file:// may block camera access.

Option B: Python Environment (For backend/local tools)

If you are running or developing supplemental Python scripts in tools like Eclipse PyDev:

# Upgrade installation dependencies
python -m pip install --upgrade pip setuptools wheel

# Install required packages
python -m pip install opencv-python google-genai cryptography ultralytics


Deploying to GitHub Pages

If you fork or clone this project, deploying your own version on GitHub Pages takes less than a minute:

Push your repository to GitHub.

Go to Settings > Pages on your repository menu.

Under Build and deployment, select Deploy from a branch.

Choose main (or master) as the branch and / (root) as the folder, then click Save.

Your live site will automatically deploy over secure HTTPS!

Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

License

Distributed under the MIT License. See LICENSE for more details.
