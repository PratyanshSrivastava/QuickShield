# QuickShield & QuickShield Helper

QuickShield is a gesture‑based personal safety app that turns your Android phone’s power button into a silent SOS trigger.  
QuickShield Helper is the companion app for guardians and volunteers, delivering live alerts, location, and context when someone nearby needs help.

---

## 🌐 System Overview

- **QuickShield (User app)** – installed on the person who wants protection.  
- **QuickShield Helper (Guardian / Volunteer app)** – installed on trusted contacts and volunteers.  
Together they create a safety mesh that calls 112, notifies your guardians, and activates nearby helpers within a 0.5 km radius.

---

## 📱 QuickShield – User App

**Purpose:** Let a user trigger an SOS with just the power button and automatically notify everyone who can help.

### Key Functions

- **Login & profile**
  - Simple registration and login.
  - Stores basic details needed by guardians in an emergency.

- **Power‑button SOS gesture**
  - Detects **5 quick presses** of the power button.
  - Gives a **short vibration** as feedback.
  - Waits for **2 more presses** to confirm the SOS and prevent accidental triggers.

- **112 emergency call**
  - After confirmation, the phone automatically dials **112** (India’s official emergency number).
  - The call is made directly from the user’s device using the normal dialer.

- **Live location tracking**
  - Captures GPS location when SOS starts.
  - Periodically updates location while the SOS is active.
  - Shares the live position with all paired guardians.

- **Microphone audio streaming**
  - Turns on the microphone during an active SOS.
  - Streams audio to guardians in QuickShield Helper so they can understand the situation.

- **QR‑based pairing**
  - Generates a unique **QR code** for the user.
  - Guardians scan this QR in QuickShield Helper to link their phone to the user.
  - Supports multiple guardians for one user.

---

## 📲 QuickShield Helper – Guardian & Volunteer App

**Purpose:** Receive SOS alerts, see live location, hear audio (for guardians), and optionally help nearby users as a volunteer.

### Guardian Mode

- **Login & role selection**
  - Guardian chooses their role (guardian / volunteer / both).
- **Pairing with users**
  - Scans the QR code from QuickShield to pair.
  - Shows a list of all paired users and their status.
- **Incoming SOS alerts**
  - Phone rings and shows which user is in danger.
  - Displays **live map** with current location.
  - Plays **live microphone audio** from the user’s phone (guardians only).
- **Follow‑up actions**
  - Call the user back.
  - Coordinate with other guardians or local authorities.

### Volunteer Mode

- **Opt‑in volunteering**
  - Any QuickShield Helper user can enable “Volunteer Mode”.
- **Proximity‑based alerts**
  - Backend checks which volunteers are within **0.5 km** of an active SOS.
  - Eligible volunteers get a loud alert on their phone.
- **Privacy‑preserving view**
  - Volunteers see **only the incident location** and basic status.
  - No audio and no detailed personal identity by default.
- **Response options**
  - Volunteer can choose to help, navigate to the location, or ignore the alert.

---

## 🔗 How the Two Apps Work Together

- QuickShield detects the power‑button gesture, confirms it, and calls 112.  
- At the same time, it sends SOS data (user ID, location, audio info) to the backend.  
- The backend:
  - Notifies all paired guardians in **QuickShield Helper** with full context.  
  - Finds nearby volunteers within **0.5 km** and sends them a location‑only alert.  

This creates a layered safety net: **official 112 responders + trusted guardians + nearby volunteers**, all activated from one quick gesture on the power button.
