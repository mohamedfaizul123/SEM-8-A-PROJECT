# SEM-8-A-PROJECT
SECURE VOICE TRANSACTION USING MACHINE LEARNING AND IOT
Introduction
With the rise of digital transactions, security has become a significant concern. This project implements a secure voice transaction system that uses Machine Learning (ML) for voice-based identity verification and IoT components for added layers of biometric and RFID authentication.

Problem Statement
Traditional authentication systems are vulnerable to security breaches such as password leaks and card cloning. This project aims to address these challenges by implementing a multi-modal biometric authentication method that enhances both security and usability.

Objectives
Authenticate users using voice recognition

Add extra layers with RFID and fingerprint sensors

Use machine learning algorithms for real-time identity verification

Ensure secure transaction approval via IoT integration

System Architecture
text
Copy
Edit
User --> Voice Input --> Voice ML Model
     --> Fingerprint Sensor --> ML Classifier
     --> RFID Scanner --> ID Verification
     --> Microcontroller --> Transaction Approved/Denied
Technologies Used
Python

Arduino UNO / ESP32

Machine Learning (SVM, HMM, DTW)

SpeechRecognition, librosa, scikit-learn

RFID Module (RC522)

Fingerprint Sensor (R305)

Flask (for local server interface)

Modules
Module	Description
voice_auth.py	Processes and verifies user voice
fingerprint.py	Scans and matches fingerprint data
rfid_module.py	Reads RFID card and verifies ID
main.py	Coordinates all modules and processes flow

Hardware Requirements
ESP32 / Raspberry Pi / Arduino UNO

RC522 RFID Reader

R305 Fingerprint Sensor

Microphone / Sound Card

Speaker (optional for feedback)

Dataset
Voice Dataset: Collected via microphone or public datasets like Mozilla Common Voice.

Fingerprint Dataset: Pre-collected sensor data or local captures.

RFID Tags: Each user is assigned a unique RFID UID.

How it Works
User speaks a passphrase (e.g., "Confirm my transaction").

The voice is verified using an ML classifier (SVM or HMM).

The user scans their fingerprint, which is verified locally.

The RFID tag is read and matched with a known UID.

On successful verification from all three, transaction is approved.

Results
Accuracy:

Voice Recognition (SVM): 93%

Fingerprint Matching: 98%

RFID Verification: 100%

Latency: < 3 seconds end-to-end

Future Work
Add face recognition using OpenCV

Integrate with blockchain for tamper-proof logs

Real-time SMS/email alerts for failed authentications

Deploy over cloud with mobile app interface

