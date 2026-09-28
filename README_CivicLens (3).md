# CivicLens AI

> **From Citizen Reports to Verified Civic Action**

CivicLens AI is an AI-powered civic issue reporting and municipal intelligence platform that helps citizens report local infrastructure and sanitation problems using photos while helping municipal teams organize, prioritize, track, and verify those issues.

The platform is designed to turn a simple citizen photo into a structured civic case with AI-assisted issue detection, severity analysis, location/ward mapping, duplicate detection, complaint tracking, repair verification, and municipal analytics.

---

## 🚀 Overview

Citizens regularly encounter problems such as:

- Potholes and damaged roads
- Garbage dumping and overflowing bins
- Blocked drains
- Open manholes
- Broken streetlights
- Water leakage
- Sewage overflow
- Fallen trees
- Damaged public infrastructure

Traditional complaint workflows can require manual categorization, detailed descriptions, and finding the right authority. CivicLens simplifies the reporting process and creates a complete lifecycle from **reporting → routing → resolution → verification**.

### Core Workflow

```text
Citizen
   ↓
Capture / Upload Photo
   ↓
AI Issue Analysis
   ↓
Severity Detection
   ↓
Location + Ward Identification
   ↓
Duplicate Detection
   ↓
Complaint Creation
   ↓
Municipal Officer Dashboard
   ↓
Assignment & Repair
   ↓
Before / After Verification
   ↓
Citizen Verification
   ↓
Verified / Reopened
```

---

## ✨ Key Features

### 👤 Citizen Features

- Secure registration and login
- Photo-based civic issue reporting
- Camera/image upload support
- AI-assisted issue identification
- AI-assisted severity estimation
- Automatic location capture when permission is available
- Ward and department mapping
- Duplicate complaint detection
- Support existing complaints instead of creating unnecessary duplicates
- Complaint ID generation
- Complaint history
- Complaint status timeline
- Nearby civic issue map
- Notifications
- Citizen verification after resolution
- Ability to reopen an issue when it is not actually fixed

### 🤖 AI Features

- Civic issue image analysis
- Issue category prediction
- Severity estimation
- Suggested municipal department
- AI-generated issue description
- Duplicate issue assistance
- Before/after repair image comparison

AI results are intended to assist users and officials and can be reviewed or corrected where appropriate.

### 🏛️ Municipal Officer Features

- Department-specific complaint dashboard
- Ward-specific filtering
- Complaint search and sorting
- Severity-based prioritization
- Complaint assignment
- Status management
- SLA tracking
- Repair/update comments
- Before/after repair image upload
- Resolution workflow
- Reopened complaint handling
- Department analytics

### 📊 Civic Intelligence

- Live civic issue map
- Issue heatmaps
- Ward-level issue distribution
- Department workload analytics
- Resolution time analytics
- SLA compliance monitoring
- Repeated problem/hotspot analysis
- Road health indicators
- Historical issue trends

---

## 🧠 Why CivicLens?

CivicLens is designed to go beyond a basic complaint portal.

Instead of only collecting complaints, it creates an intelligent workflow:

```text
Report
  ↓
Understand
  ↓
Prioritize
  ↓
Route
  ↓
Resolve
  ↓
Verify
  ↓
Analyze
```

### Differentiators

| Capability | CivicLens |
|---|---|
| Photo-based reporting | ✅ |
| AI issue detection | ✅ |
| AI severity assistance | ✅ |
| Department suggestion | ✅ |
| Location / ward mapping | ✅ |
| Duplicate detection | ✅ |
| Existing issue support | ✅ |
| Complaint timeline | ✅ |
| SLA tracking | ✅ |
| Civic issue map | ✅ |
| Before/after verification | ✅ |
| Citizen resolution verification | ✅ |
| Municipal analytics | ✅ |
| Road health indicators | ✅ |

---

## 🏗️ System Architecture

```text
┌─────────────────────────────┐
│       Citizen Interface     │
│     React + Tailwind CSS    │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│        Backend API          │
│     REST / Authentication   │
└──────────────┬──────────────┘
               │
       ┌───────┴────────┐
       ▼                ▼
┌─────────────┐   ┌─────────────┐
│ PostgreSQL  │   │ AI Services │
│  + PostGIS  │   │ Vision / NLP│
└─────────────┘   └─────────────┘
       │
       ▼
┌─────────────────────────────┐
│   Municipal Officer Panel   │
│ Dashboard + Maps + Analytics│
└─────────────────────────────┘
```

---

## 🛠️ Technology Stack

> Update this section to match the exact technologies used in your implementation.

### Frontend
- React
- Tailwind CSS
- TypeScript / JavaScript
- Recharts
- Leaflet / Mapbox / OpenStreetMap

### Backend
- Spring Boot or Node.js
- REST APIs
- Role-based authentication and authorization

### Database
- PostgreSQL
- PostGIS for geospatial queries where enabled

### AI
- Computer vision / multimodal AI
- Image classification
- Severity analysis
- Text generation
- Duplicate detection

### Storage & Services
- Image/file storage
- Authentication
- Notifications
- Environment-based configuration

---

## 📱 Main Application Areas

### Citizen Portal

- Dashboard
- Report Issue
- My Complaints
- Complaint Details
- Nearby Issues
- Civic Map
- Notifications
- Profile

### Municipal Officer Portal

- Dashboard
- Complaint Queue
- Complaint Details
- Assigned Tasks
- Map
- Analytics

### Admin Portal

- Dashboard
- User Management
- Officer Management
- Departments
- Wards
- Issue Categories
- SLA Configuration
- Analytics
- System Settings

---

## 🔄 Complaint Lifecycle

Every complaint follows a controlled lifecycle:

```text
Submitted
   ↓
AI Analyzed
   ↓
Assigned
   ↓
Acknowledged
   ↓
In Progress
   ↓
Resolved
   ↓
Citizen Verification
   ├── Verified
   └── Reopened
```

Each status transition can be recorded with timestamps and associated actions.

---

## 🔎 Duplicate Detection

CivicLens is designed to reduce repeated complaints for the same physical issue.

Before creating a new complaint, the system can compare:

- Geographic proximity
- Issue category
- Time
- Description similarity
- Image similarity where implemented

Example:

```text
Possible existing issue found

Issue: Large pothole
Distance: 80 meters
Existing reports: 14
Status: In Progress

[Support Existing Issue]
[Submit New Complaint]
```

This allows multiple citizens to signal the same civic problem without creating unnecessary duplicate tickets.

---

## 🛠️ Repair Verification

CivicLens includes a two-stage resolution verification concept.

### 1. AI-assisted verification

The officer uploads an after-repair photo.

The system compares the before/after images and produces an analysis such as:

```text
Repair Verification
Issue: Pothole
Detected change: Road surface appears repaired
Confidence: 92%
```

### 2. Citizen verification

The citizen can confirm:

```text
✅ Yes, fixed
❌ No, still exists
```

A citizen rejection can reopen the complaint for further action.

> AI verification is an assistive feature and should not be treated as a guarantee that physical work was completed.

---

## 🗺️ Civic Map & Heatmap

The CivicLens map can visualize civic problems by:

- Issue type
- Severity
- Status
- Ward
- Location
- Complaint density

Example:

```text
🔴 High severity
🟠 Medium severity
🟢 Resolved
```

The analytics layer can identify repeated problem locations and issue concentrations for planning and maintenance.

---

## ⏱️ SLA Tracking

CivicLens supports configurable target resolution times by category or severity.

Example configuration:

```text
High severity   → 24 hours
Medium severity → 72 hours
Low severity    → 7 days
```

When the configured time is exceeded, the complaint can be marked:

```text
⚠ SLA BREACHED
```

Actual SLA values should be configured by the deploying organization.

---

## 🔐 Security & Privacy

The application should follow secure development practices, including:

- Password hashing
- Role-based access control
- API authorization
- Input validation
- File type/size validation
- Secure environment variables
- Audit logging
- Restricted access to private citizen information
- No API keys committed to source control

### Environment Variables

Never commit secrets to GitHub.

Create a `.env` file locally and provide a safe template:

```env
# Example only
DATABASE_URL=
API_BASE_URL=
AI_API_KEY=
MAP_API_KEY=
AUTH_SECRET=
```

Commit only:

```text
.env.example
```

and keep:

```text
.env
```

in `.gitignore`.

---

## 📂 Suggested Project Structure

```text
civiclens-ai/
│
├── frontend/
│   ├── components/
│   ├── pages/
│   ├── layouts/
│   ├── services/
│   ├── hooks/
│   ├── utils/
│   └── types/
│
├── backend/
│   ├── controllers/
│   ├── services/
│   ├── repositories/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── utils/
│
├── ai/
│   ├── image-analysis/
│   ├── severity/
│   ├── duplicate-detection/
│   └── verification/
│
├── database/
│   ├── schema/
│   └── seed/
│
├── .env.example
├── .gitignore
└── README.md
```

Adjust this structure to match the actual repository.

---

## ⚙️ Installation

### Prerequisites

Install:

- Git
- Node.js
- npm
- PostgreSQL

If your version also uses Java/Spring Boot:

- JDK 17+ (or the version required by the backend)

### Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

### Install dependencies

Frontend:

```bash
cd frontend
npm install
```

Backend:

```bash
cd backend
# Use the package/build command required by your backend
```

### Configure environment variables

Copy:

```bash
cp .env.example .env
```

Then configure the required database, authentication, AI, map, and storage values.

### Run the application

Start the backend and frontend using the commands defined by the project.

Example:

```bash
npm run dev
```

> Replace the commands above with the exact commands used by your repository.

---

## 🧪 Demo Workflow

CivicLens can be demonstrated using the following end-to-end workflow:

### Citizen

1. Register or log in
2. Select **Report an Issue**
3. Capture/upload a photo
4. Run AI analysis
5. Review issue category and severity
6. Confirm location
7. Check for existing nearby complaints
8. Support an existing issue or submit a new complaint
9. Receive a complaint ID
10. Track the complaint

### Municipal Officer

11. Log in to the officer dashboard
12. View the complaint
13. Review image, AI analysis and location
14. Assign/acknowledge the complaint
15. Start work
16. Upload an after-repair image
17. Mark the complaint as resolved

### Verification

18. AI performs assistive before/after comparison
19. Citizen receives verification request
20. Citizen confirms the repair or reopens the issue
21. Analytics update based on the complaint lifecycle

---

## 🧩 Demo Mode

For development and hackathon demonstrations, CivicLens can use seeded/sample data.

The prototype may demonstrate a specific city or locality using sample data.

> Sample/demo locations and complaint data must not be presented as official municipal data unless an actual verified integration exists.

---

## 🌐 Future Scope

Potential future enhancements include:

- Official municipal/government API integrations
- WhatsApp-based reporting
- Multilingual voice reporting
- Telugu, Hindi and other regional language support
- Offline reporting with later synchronization
- Predictive infrastructure maintenance
- IoT/sensor integration
- Satellite/geospatial data integration
- Advanced computer vision models
- Automated work-order integration
- State-wide deployment
- National-scale civic intelligence

---

## ⚠️ Important Prototype Note

CivicLens is currently designed as a civic-tech platform/prototype.

For the prototype:

```text
Citizen
   ↓
CivicLens Backend
   ↓
CivicLens Database
   ↓
Municipal Officer Dashboard
```

It does **not** imply an existing official connection to a municipal corporation or government grievance system.

Government/municipal system integration can be added through approved APIs or other authorized mechanisms in a production deployment.

---

## 🎯 Project Goals

CivicLens aims to:

- Make civic issue reporting simpler
- Reduce duplicate complaints
- Improve issue prioritization
- Help route complaints to the right municipal team
- Increase resolution transparency
- Add verification to the resolution process
- Turn complaint data into useful civic intelligence

---

## 👥 Team

**Project:** CivicLens AI

**Team Members:**
- Your Name
- Team Member 2
- Team Member 3
- Team Member 4

**Institution:** Your College Name

**Hackathon:** Your Hackathon Name

---

## 📸 Screenshots

Add your project screenshots here:

```markdown
![Landing Page](screenshots/landing.png)

![Citizen Dashboard](screenshots/citizen-dashboard.png)

![Report Issue](screenshots/report-issue.png)

![AI Analysis](screenshots/ai-analysis.png)

![Officer Dashboard](screenshots/officer-dashboard.png)

![Civic Map](screenshots/civic-map.png)
```

---

## 📄 License

Add the license appropriate for your project.

Example:

```text
MIT License
```

---

## ⭐ Support

If you find CivicLens interesting, consider starring the repository and sharing feedback.

---

### CivicLens AI

**See it. Report it. Route it. Fix it. Verify it.**
