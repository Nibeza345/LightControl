# MQTT-Based Light Control

This project is a web-based application that allows users to switch a light ON/OFF over MQTT. It simulates an IoT device (ESP8266) using Python to listen for MQTT messages and print the status of the light (ON/OFF).

## Task Objective

The goal of the assignment is to create a simple web interface that uses MQTT to control the state of a simulated light via MQTT. The web interface provides two buttons, "Turn ON" and "Turn OFF", which send MQTT messages. A Python script simulates the IoT device, which subscribes to the MQTT topic and prints the light status.

## Project Structure

- **index.html**: Web Interface that lets users turn the light ON or OFF via MQTT.
- **light_simulation.py**: Python script that simulates the IoT device (ESP8266) and listens for MQTT messages.
- **README.md**: Documentation for the project.

## Instructions

### Step 1: Web Interface (index.html)
- Created a simple webpage with two buttons: "Turn ON" and "Turn OFF".
- Displays a status message indicating the last sent command.
- Uses MQTT.js to publish "ON" or "OFF" to the `/student_group/light_control` topic via WebSockets.

### Step 2: Simulated IoT Device (Python)
- The Python script subscribes to the `/student_group/light_control` topic using MQTT.
- If it receives "ON", it prints: `🟢 Light is TURNED ON`.
- If it receives "OFF", it prints: `🔴 Light is TURNED OFF`.

### Step 3: Hosting & Testing
- The Python script is run on the local machine to simulate the IoT device (ESP8266).
- The `index.html` is opened in a browser, and users can test switching the light ON and OFF.
- The Python script prints the correct status when the buttons are clicked.

### Step 4: Push to GitHub
This repository contains the following files:
- `index.html` (Web Interface)
- `light_simulation.py` (Simulated IoT Device)
- `README.md` (Project Documentation)

### Step 5: Submit Your Work
After completing the project, the GitHub repository link is submitted via the provided Google Form.

## Requirements

- Python 3.x
- MQTT broker (e.g., Mosquitto)
- MQTT.js library for the web interface

## Running the Project Locally

1. **Start the MQTT broker** (e.g., Mosquitto) on your machine.
2. **Run the Python script** (`light_simulation.py`):
   ```bash
   python light_simulation.py
