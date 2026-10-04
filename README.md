# 🎓 NANDHA LOST & FOUND

> **College:** Nandha Engineering College  
> **Location:** Erode, Tamil Nadu, India  
> **Affiliation:** Autonomous Institution | Approved by AICTE, New Delhi | Affiliated to Anna University, Chennai  
> **Project Type:** Modern Responsive Frontend-Only Web Application (College Project Prototype)

---

## 🌟 Project Overview

**Nandha Lost & Found** is a modern, responsive, SaaS-style campus web platform tailored specifically for Nandha Engineering College students, faculty, and administrative staff. It enables anyone across the 19 campus blocks and facilities to report lost items, report found items, perform instant filtered searches, review match suggestions, and manage report lifecycles through a live admin dashboard.

---

## 🎯 Key Project Features

### 1. Modern Sticky Navigation & Brand Identity
- **Header:** Nandha College crest badge, autonomous institution marker, desktop links with micro-interactions, and a responsive mobile drawer menu.
- **Quick Action Trigger:** "Report Item" quick launcher and "How It Works" interactive modal.
- **Campus Help Assistant:** Floating "Need Help?" button with 24/7 campus security phone numbers, emergency extensions, and custodian desks.

### 2. Home Page & Campus Directory
- **Hero Section:** High-impact SaaS headline, call-to-action buttons for *"I Lost Something"* (Red accent) and *"I Found Something"* (Purple accent), and an interactive Live Campus Registry Radar card.
- **Real-Time Dynamic Metrics:**
  - 🔴 **24 Lost Items**
  - 🟣 **18 Found Items**
  - 🔵 **9 Possible Matches**
  - 🟢 **7 Items Returned**
- **Interactive Campus Locations Directory (19 Spots):**
  - Block 1 (ECE & Science Labs)
  - Block 2 (Mechanical & Civil Depts)
  - Block 3 (CSE & IT Blocks)
  - Block 4 (AI&DS & Management Block)
  - Block 5 (EEE Dept & High Voltage Lab)
  - Block 6 (First Year Foundation Block)
  - Block 7 (Central Computing Center & Server Room)
  - Block 8 (Central Library & Reference Center)
  - Block 9 (Placement & Training Cell)
  - Auditorium, Cafeteria, Basketball Court, Volleyball Court, Boys Hostel, Girls Hostel, College Entrance, Yoga Hall, Car Parking, Bike Parking.
  - *Clicking any location chip automatically opens the Search Registry filtered to that spot!*

### 3. Module 1: Report Lost Item
- Form fields: Item Name, Category (12 standard campus categories), Nandha Location dropdown, Date Lost, Approximate Time, Drag-and-drop Photo Upload with local preview, Detailed Description, Optional Identifying Marks (for private verification), and Student Contact details.
- Quick Preset Photo picker for instant demonstration without searching local files.
- Animated submission with loading state.
- Modal confirmation with unique, generated report ID (e.g. `NLF-2026-043`) and 1-click clipboard copy.
- Persistent save to browser `localStorage`.

### 4. Module 2: Report Found Item
- Visually distinct purple/violet aesthetic for good campus Samaritan reporting.
- Form fields: Item Name, Category, Location, Date & Time, Photo Upload, Safe-Custody Location (where the item is currently held, e.g. Main Gate Security, HOD Office, Library Counter), and Finder details.
- Modal confirmation with generated report ID (e.g. `NFF-2026-044`).
- Updates the campus activity feed and triggers automatic match calculations.

### 5. Module 3: Search & Match
- **Real-Time Instant Search:** Filters live across item title, category, description, location, and report ID.
- **Multi-Filter Console:**
  - Item Type tabs: *All (42)*, *Lost (24)*, *Found (18)*
  - Category dropdown
  - Campus Location dropdown
  - Lifecycle Status dropdown
  - Date sorting (Newest / Oldest)
- **Rich Item Cards:** Badges for item type (Red for Lost, Purple for Found), status badges, thumbnail with zoom hover, location, date, and quick action buttons.
- Preloaded with the exact sample items required:
  1. *Black Wallet* (Lost · Cafeteria · 02 Oct 2026)
  2. *Student ID Card* (Found · Block 4 · 01 Oct 2026)
  3. *Black Backpack* (Lost · Auditorium · 30 Sep 2026)
  4. *Blue Water Bottle* (Found · Basketball Court · 29 Sep 2026)
  5. *Wireless Earphones* (Lost · Block 7 · 28 Sep 2026)
  + 37 additional realistic campus items.

### 6. Heuristic Match Comparison Feature
- Opens the **"Possible Match Found"** modal.
- Side-by-side comparison of the Lost item and Found item with high-resolution photos.
- **Match Factors Checklist:**
  - [x] Same category
  - [x] Similar description keywords
  - [x] Same campus location
  - [x] Similar date interval
- Dynamic match confidence score (e.g., **87%**, **92%**, **94%**) with animated gradient progress bar.
- Action to confirm match and transition item into *Under Review* or *Matched*.

### 7. Module 4: Admin & Status Dashboard
- **Executive Metrics:** Live statistics synchronized with `localStorage`.
- **Visual Analytics:** Interactive horizontal bar & progress chart showing Lost vs Found breakdown across top categories.
- **Campus Activity Feed:** Timestamped log of reports, status updates, and match detections.
- **Reports Management Table:**
  - Desktop table layout and mobile card layout.
  - Interactive status dropdown directly inside each row (*Searching*, *Under Review*, *Possible Match*, *Matched*, *Returned*). Status changes update persistence immediately.
  - Quick action buttons to view item details or open match comparison.
  - **"Reset Demo Data"** button to instantly restore pristine initial state during presentations.

### 8. Claim Verification & Handover Flow
- Clicking *"I Think This Is Mine"* opens a student claim form requesting Roll Number, Contact Info, and Private Identifying Proof.
- Submitting generates a claim ticket (e.g. `CLM-849201`) and sets the item to *Under Review*.
- Instructions provided to visit the Block 1 Ground Floor Security Control Room with Student ID card.

---

## 💻 Tech Stack & Design Architecture

- **HTML5:** Semantic, accessible layout with modular view panels.
- **Tailwind CSS:** Modern utility classes, smooth hover states, and responsive breakpoints.
- **Custom CSS (`css/styles.css`):** Glassmorphism navigation, soft shadows, rounded 16–24px SaaS cards, and custom scrollbars.
- **Vanilla JavaScript (ES6+):** Pure frontend architecture requiring no Node.js runtime, no backend build step, and zero npm dependencies.
- **Browser `localStorage` (`js/storage.js`):** Handles persistence, CRUD operations, dynamic metric counting, activity log generation, and heuristic similarity matching.
- **Lucide Icons:** Modern feather-style SVG icon system with retry mechanism for zero-glitch loading.

---

## 🚀 How to Run the Application

This is a **frontend-only** web application. It runs directly in any modern browser without installing servers or running terminal commands.

### Option A: Direct Browser Launch (Easiest)
1. Navigate to the project directory: `c:\Users\HP\Documents\Project`
2. Double-click on `index.html` (or right-click -> *Open with* -> Google Chrome / Microsoft Edge / Firefox).

### Option B: Local Web Server (Optional)
If you prefer running via a local development server:
```bash
# Using Python (if installed)
python -m http.server 8000

# Using Node.js npx (if installed)
npx serve .
```
Then open `http://localhost:8000` in your web browser.

---

## 📋 Live Demonstration Script for Review Committee

1. **Introduction:**
   - Open `index.html` to showcase the **Home View**.
   - Point out the Nandha Engineering College branding, Autonomous status badge, and the 4 statistics cards (24 Lost, 18 Found, 9 Matches, 7 Returned).
2. **Interactive Location Filtering:**
   - Scroll down to the *Campus Locations Directory*.
   - Click on **"Cafeteria"** or **"Block 7"**.
   - Show how the app smoothly switches to the **Search Registry** and filters items strictly to that location.
3. **Report a Lost Item (Module 1):**
   - Click **"Report Lost"** in the navigation bar.
   - Enter *"Titan Octane Watch"*, select Category *"Accessories"*, choose Location *"Basketball Court"*.
   - Click one of the quick photo presets (e.g. *"Wallet"* or *"Earphones"*) to demonstrate instant photo preview.
   - Click **"Submit Lost Report"**; observe the loading spinner and the celebratory modal with the newly generated ID (e.g. `NLF-2026-043`).
4. **Search & Heuristic Match (Module 3):**
   - Switch to **Search Items**.
   - Type *"Wallet"* into the search box.
   - Show the *"Black Leather Wallet"* card and click the **"Match"** button.
   - Walk through the **Possible Match Found** modal: 92% confidence score, checklist of match factors, and side-by-side photo comparison.
   - Click **"Confirm Match & Mark for Review"**.
5. **Dashboard & Status Lifecycle (Module 4):**
   - Navigate to the **Dashboard**.
   - Observe how the total count and activity log immediately updated with the new item and the confirmed match.
   - In the Reports Table, change the status of an item from *"Searching"* to *"Returned"* via the dropdown.
   - Show the dynamic category chart updating automatically.
6. **Student Claim Workflow:**
   - Open any item by clicking *"View"*, then click *"I Think This Is Mine"*.
   - Fill in student Roll Number `24CS108` and submit.
   - Show the generated verification ticket `CLM-xxxxxx` and the campus security instructions.

---

## 📂 File Structure

```
Project/
├── index.html           # Main single-page application markup & modals
├── css/
│   └── styles.css       # SaaS styling, animations, glassmorphism & badges
├── js/
│   ├── data.js          # 19 Nandha locations, 12 categories, initial sample dataset
│   ├── storage.js       # LocalStorage state manager, stats counter & match heuristic
│   └── app.js           # Navigation controller, form handlers, search & modal logic
└── README.md            # Comprehensive college project documentation
```

---

*Designed & Developed for Nandha Engineering College, Erode, Tamil Nadu, India.*
