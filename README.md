 SafeGuard — Women Safety & Emergency Assistance Platform

A safety-focused web platform that helps women instantly request emergency assistance, share live alerts with trusted contacts and verified volunteers, and access safety resources — built as a fully responsive, no-backend, client-side web application.

Live Demo: add your Netlify URL here after deployment
Video Walkthrough: add your feedback video link here


 Problem Statement

Women often face unsafe situations while traveling, working late hours, or living alone. Existing safety mechanisms suffer from delayed access to help, lack of nearby responder coordination, dependence on manual phone calls, no centralized assistance platform, and limited real-time location tracking.

SafeGuard addresses this by providing a single platform where users can trigger an SOS alert, notify trusted contacts, get matched with nearby verified volunteers, and access a directory of emergency services and safety resources — all from one dashboard.


Objectives

Primary


Provide immediate emergency assistance to women
Connect users with nearby verified support resources (volunteers)
Enable simulated real-time location sharing during emergencies
Improve response time and safety outcomes


Secondary


Build a trusted network of volunteers and responders
Increase awareness of safety resources and tips
Demonstrate a design that is scalable to multi-city deployment



Features

User Module


Registration, login, forgot password with form validation
Personal dashboard with safety status indicator and quick actions
One-click SOS emergency button with confirmation modal, 60-second countdown timer, and simulated SMS dispatch to trusted contacts
Trusted Contacts — full CRUD (add/edit/delete/call)
Emergency Services Directory — Police, Ambulance, Fire, Women's Helpline, and more (real Indian helpline numbers)
Nearby Help Centers — police stations, hospitals, and women's protection centers with map links
Safety Zones — community safety ratings (Safe / Caution / Unsafe) for known areas
Safety Tips — personal, travel, online, and emergency-preparedness guidance
Alert History — full log of all SOS alerts with date, time, type, and status
Profile management — photo upload, edit details, change password, delete account


Volunteer Module


Volunteer registration with skills, service area, and ID verification fields
Pending-verification gate (volunteers can't log in until admin-approved)
Live dashboard showing active emergency requests in their area
Accept / Decline / Resolve workflow with response history and rating
Status toggle: Available / Busy / Offline


Admin Module


Manage registered users (search, view, delete)
Verify or reject volunteer applications
Monitor all emergency alerts platform-wide (status, responder, location)
Manage Safety Zones (add/edit/delete)
KPI dashboard: resolution rate, response rate, volunteer verification %, active alert rate
Export all platform data as JSON


UI/UX


Fully responsive (desktop, tablet, mobile) with collapsible sidebar navigation
Dark mode toggle (persisted via localStorage)
Toast notifications, modal confirmations, loading animation, live clock
Custom design system (no Bootstrap) using CSS variables, Google Fonts, and Font Awesome icons



Tech Stack

LayerTechnologyMarkupHTML5StylingCustom CSS3 (CSS Variables, Flexbox, Grid)LogicVanilla JavaScript (ES6+)PersistenceBrowser localStorage (no backend/server required)IconsFont Awesome 6FontsGoogle Fonts — Playfair Display, DM Sans

This is a fully static, client-side application — there is no backend server, database, or API. All data (users, alerts, contacts, zones) is stored in the browser's localStorage, making it instantly deployable to any static hosting provider with zero configuration.


📂 Project Structure

women-safety-platform/
│
├── index.html                  # Entry point → redirects to login
├── login.html                  # Login with role tabs (User / Volunteer / Admin)
├── register.html               # User registration
├── forgot-password.html        # Simulated password reset
├── dashboard.html               # User dashboard
├── sos.html                     # SOS emergency button + countdown
├── contacts.html                # Trusted contacts CRUD
├── services.html                 # Emergency services directory
├── helpcenters.html             # Nearby help centers
├── zones.html                   # Safety zone ratings
├── tips.html                    # Safety tips module
├── alerts.html                  # Alert history log
├── profile.html                 # User profile management
├── volunteer-register.html      # Volunteer application form
├── volunteer-dashboard.html     # Volunteer response dashboard
├── admin.html                   # Admin control panel
│
├── css/
│   └── style.css                # Complete design system
│
├── js/
│   └── script.js                # All application logic
│
└── assets/
    └── images/                  # Image assets


Getting Started Locally

No build tools, no dependencies, no installation required.


Clone the repository:


bash   git clone https://github.com/<your-username>/safeguard-women-safety-platform.git
   cd safeguard-women-safety-platform


Open index.html directly in your browser, or serve it locally:


bash   # Python 3
   python3 -m http.server 8000
   # then visit http://localhost:8000


Demo Credentials

RoleEmailPasswordAdminadmin@wsp.comadmin123Volunteervolunteer@wsp.comvol123UserRegister a new account—


Demo accounts are seeded automatically into localStorage on first load.




 Deployment

This project is deployed as a static site. To deploy your own copy:

Netlify (Drag & Drop)


Go to app.netlify.com/drop
Drag the project folder onto the page
Netlify gives you a live URL instantly


GitHub Pages


Push this repo to GitHub
Go to Settings → Pages → Source: main branch, / (root)
Your site will be live at https://<username>.github.io/<repo-name>/



📈 Key Performance Indicators (Tracked in Admin Panel)


Number of registered users
Emergency alerts triggered
Average response time
Successful assistance / resolution rate
Volunteer response and verification rate
Monthly active users



 Future Enhancements


Native mobile application with SOS widget
Real backend integration (Node.js/Express + MongoDB) for true multi-device sync
Direct integration with police/ambulance dispatch systems
Voice-activated SOS alerts
Wearable device (smartwatch) support
AI-based risk detection and predictive safety zone mapping
Real GPS-based live location sharing (current version simulates location)



 Scope Notes


This is a Phase 1 / prototype build intended for academic and portfolio demonstration.
All data is stored in browser localStorage — it is not synced across devices and will be cleared if browser storage is cleared.
SMS notifications, location sharing, and emergency service calls are simulated for demonstration purposes; no real SMS or live GPS APIs are integrated in this phase.
No direct law-enforcement system integration in this phase (per project scope).



Author

Built as part of an internship project submission — Frontend Development track, Housing & Community Platforms domain (Co-Living Space Platform track), adapted to the Women Safety & Emergency Assistance Platform brief.

License

This project is released under the MIT License — see LICENSE for details.
