# IOT-BASED-ATTENDANCE-SYSTEM-USING-FINGERPRINT-SENSOR

This project aims to automate attendance recording using an ESP32 microcontroller and an R307S fingerprint sensor. It provides an accurate, secure, and efficient solution for recording attendance data directly to a Google Sheet. This reduces manual effort and increases data accuracy.

## Project Objective

Develop an ESP32-based system that uses a fingerprint module (R307S) to automate the recording of attendance. The system automatically saves attendance data—including the person's name, time, and date—in a Google Sheet for easy access, management, and analysis.

## Features

- **Automated Attendance Logging**: Attendance is recorded with the scan of a fingerprint.
- **Secure and Accurate**: Only registered fingerprints are recognized.
- **Real-Time Data Storage**: Attendance data (name, date, and time) is logged in real-time to a Google Sheet.
- **Easy Access**: Attendance records are saved in a centralized Google Sheet for easy access and management.


## Components Required

- **ESP32 Microcontroller**
- **R307S Fingerprint Sensor**
- **Internet Connection (for Google Sheets API integration)**

## How It Works

1. **Initialize System**: The ESP32 microcontroller powers up, and the fingerprint sensor (R307S) is initialized to ensure readiness.

2. **Scan Fingerprint**: The user places a finger on the fingerprint sensor, which scans the fingerprint.

3. **Match Fingerprint**:
    - The system checks the fingerprint against its database.
    - If a match is found, it identifies the user; if not, the user is prompted to try again.

4. **Retrieve Name**: Upon a successful match, the system retrieves the user's name from the database.

5. **Get Date and Time**: The ESP32 fetches the current date and time.

6. **Log to Google Sheets**:
    - The system uses the Google Sheets API to open the specified sheet.
    - It logs the user's name, date, and time, creating a new attendance record.

7. **Confirmation**: A confirmation message is displayed, indicating successful logging of attendance.

## Setup and Installation

1. **Hardware Setup**:
   - Connect the R307S fingerprint sensor to the ESP32 microcontroller.
   - Ensure the ESP32 has a stable internet connection for API access.

2. **Software Setup**:
   - Install the **Arduino IDE** and necessary libraries for ESP32 and fingerprint sensor.
   - Set up the **Google Sheets API** and obtain API credentials. Refer to [Google Sheets API Documentation](https://developers.google.com/sheets/api) for steps.
   - Modify the provided code to include your Google Sheets API credentials and ESP32 setup.

3. **Fingerprint Enrollment**:
   - Enroll fingerprints by following the fingerprint sensor library's instructions.
   - Store the fingerprint data in the ESP32’s database.
