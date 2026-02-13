# QuickShield & QuickShield Helper

QuickShield is a gesture‑based personal safety app that turns your Android phone’s power button and voice into a silent SOS trigger.  
QuickShield Helper is the companion app for guardians and volunteers, delivering live alerts, location, and context when someone nearby needs help.

---

## 🌐 System Overview

- **QuickShield (User app)** – installed on the person who wants protection.  
- **QuickShield Helper (Guardian / Volunteer app)** – installed on trusted contacts and volunteers.  

Together they create an intelligent safety mesh that:

- Calls **112** (India’s emergency number) when needed.  
- Notifies trusted guardians with **live location and audio**.  
- Activates nearby volunteers within a **0.5 km radius**.  
- Uses **AI features** to detect voice SOS, predict risks, and help the user escape unsafe situations.

---

## 📱 QuickShield – User App

**Purpose:** Let a user trigger an SOS with just the power button or their voice and automatically notify everyone who can help.

### 🔐 Login & Profile

- Simple registration and login flow.  
- Stores basic personal and medical details needed by guardians in an emergency.  
- Allows managing trusted guardians and emergency preferences.

---

### 🔘 Power‑Button SOS Gesture

- Detects **5 quick presses** of the power button.  
- Gives a **short vibration** as feedback to show the gesture was recognized.  
- Waits for **2 more presses** to confirm the SOS and prevent accidental triggers.  
- Once confirmed, the SOS workflow starts and guardians are notified.

---

### 🗣️ AI Voice “Help” Detection

- Always‑listening, on‑device AI detects the keyword **“Help”** in the user’s voice.  
- When the word is detected, QuickShield triggers a **family‑only SOS** (no automatic 112 call).  
- Guardians receive an alert and **decide whether to escalate** by calling 112 or the user.  
- Designed to be discreet and usable even when the user cannot reach the phone’s buttons.

---

### ☎️ 112 Emergency Call

- After power‑button confirmation, the phone automatically dials **112** (India’s official emergency number).  
- The call is made directly from the user’s device using the normal dialer.  
- Works in parallel with alerts sent to guardians and volunteers.

---

### 📍 Live Location Tracking

- Captures GPS location the moment an SOS starts.  
- Periodically updates the location while the SOS is active.  
- Shares the **live position** with all paired guardians in QuickShield Helper.  
- Shows clear “SOS Active” status to avoid confusion.

---

### 🌃 AI High‑Risk Area Alerts

- Uses location, time of day, and external data sources to calculate a **safety score** for the user’s surroundings.  
- **Night‑time awareness**: Warns the user if they are entering or moving in a higher‑risk area at night.  
- Can prompt the user to **share live location** with guardians when risk is high.  
- Future‑ready to support **safer route suggestions** that avoid flagged hotspots.

---

### 📞 Fake Call Escape (AI‑Assisted)

- During setup, the user records a **custom audio clip** that sounds like a real call or conversation.  
- In suspicious or uncomfortable situations, QuickShield can trigger a **fake incoming call screen**.  
- Plays the recorded audio loudly on speaker (for example, a family member saying they are nearby).  
- Can be linked to:
  - The **voice “Help”** detection, or  
  - A subtle in‑app button or gesture.  
- Gives the user a socially acceptable reason to leave or de‑escalate the situation.

---

### 🎙️ Microphone Audio Streaming

- During an active SOS, QuickShield can enable the microphone.  
- Streams **live audio** to guardians using QuickShield Helper (guardian mode only).  
- Helps guardians understand what is happening around the user in real time.  
- Can be combined with AI analysis in future versions (for example, detecting stress in voice).

---

### 🔗 QR‑Based Pairing

- Generates a unique **QR code** for each user.  
- Guardians scan this QR in QuickShield Helper to safely link their device to the user’s profile.  
- Supports **multiple guardians** for one user.  
- Allows revoking or updating guardian access from the user app.

---

## 📲 QuickShield Helper – Guardian & Volunteer App

**Purpose:** Receive SOS alerts, see live location, hear audio (for guardians), and optionally help nearby users as a volunteer.

---

### 👨‍👩‍👧 Guardian Mode

- **Login & role selection**
  - Guardian logs in and chooses their role: **Guardian**, **Volunteer**, or **Both**.

- **Pairing with users**
  - Scans the user’s **QuickShield QR code** to pair.  
  - Shows a **list of all paired users**, their online status, and last known location.

- **Incoming SOS alerts**
  - Phone rings or vibrates and shows **which user is in danger**.  
  - Displays a **live map** with the user’s current or last location.  
  - Plays **live microphone audio** from the user’s phone (guardians only).

- **Voice “Help” escalation**
  - When an SOS was triggered by voice only, guardians see that context.  
  - Guardians can **vote or decide** whether to:
    - Call the user directly.  
    - Call **112** and share the situation.  
    - Coordinate with other guardians.

- **Follow‑up actions**
  - One‑tap call back to the user.  
  - Share location and details with **local authorities** if needed.  
  - In‑app notes or chat to coordinate response among guardians.

---

### 🧭 Volunteer Mode

- **Opt‑in volunteering**
  - Any QuickShield Helper user can enable **“Volunteer Mode”**.  
  - Volunteers can specify preferences (e.g., time slots, areas).

- **Proximity‑based alerts**
  - The backend identifies volunteers within **0.5 km** of an active SOS.  
  - Eligible volunteers receive a **distinct loud alert** on their phone.  

- **Privacy‑preserving view**
  - Volunteers see **only the incident location** and basic severity/status.  
  - No live audio and no detailed personal identity by default.  

- **Response options**
  - Volunteer can:
    - Mark **“I am coming”**.  
    - Navigate to the location via maps.  
    - Politely ignore the alert if they cannot assist.

---

## 🔗 How the Two Apps Work Together

1. **Trigger**  
   - The user activates QuickShield via:
     - **Power‑button SOS gesture**, or  
     - **Voice “Help” detection**, or  
     - In‑app SOS controls.  

2. **Immediate Actions on the User Device**  
   - Power‑button flow: confirm gesture → **auto‑call 112**.  
   - Voice “Help” flow: **family‑only SOS** without auto‑calling 112.  
   - Optional **Fake Call Escape** is triggered in situations where a distraction is safer.  

3. **Data Sent to the Backend**  
   - User ID and profile key.  
   - Current GPS location (and live updates while active).  
   - Context flags (power‑button, voice‑only, high‑risk area, etc.).  
   - Audio streaming metadata for guardians.

4. **Backend Processing**  
   - Notifies all paired **guardians in QuickShield Helper** with full context.  
   - Finds nearby **volunteers within 0.5 km** and sends them a privacy‑preserving, location‑only alert.  
   - Applies AI logic (for example, risk scoring and escalation hints) to assist guardians.

5. **Response & Resolution**  
   - Guardians and volunteers coordinate to help the user in real time.  
   - When the user is safe, they or a guardian can mark the SOS as **resolved**, stopping alerts and live tracking.

---

## 🧠 Why QuickShield Stands Out

- **Multi‑trigger safety**: Power button, voice, and in‑app controls.  
- **AI‑enhanced protection**: Voice keyword detection, high‑risk area awareness, and smart escape tools.  
- **Layered response**: Official **112 responders + trusted guardians + nearby volunteers**.  
- **Privacy‑first**: Guardians get context, volunteers see only what they need.  
- **Built for India, open‑source friendly**: Uses common Android hardware, FOSS‑friendly tools, and is ideal for hackathons like **FOSSHACK 2026**.

