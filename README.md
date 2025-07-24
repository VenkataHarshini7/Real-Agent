# 🏡 Real Agent – The DealMakers

An intelligent real estate assistant platform built for the CBRE Hackathon 2025 — combining AI, automation, compliance tracking, and CRM to redefine the broker-client real estate experience.

---

## 🚀 Overview

**Real Agent** is a full-stack property management assistant for brokers and clients. Designed with enterprise-level automation and decision intelligence, it supports every stage of the real estate journey — from shortlisting to site visits, investment analysis to document compliance — with seamless UI/UX across both dashboards.

---

## 🧩 Key Features

### 🔷 Broker & Client Dashboards
- Personalized dashboards for brokers and clients.
- Track visits, deals, properties, and activity.

### 📅 Scheduler for Site Visits & Meetings
- Smart scheduling UI for brokers and clients.
- Visual calendar integration.
- Backend support for visit tracking and conflict handling.

### 📍 Property Location Integration
- Integrated property maps.
- View pins and surrounding details within property pages.

### ✅ Bookmarking Properties
- Clients can bookmark favorites.
- Status visible to brokers.
- Used by Smart Recommendation Engine.

### 🔁 Property Comparison Tool
- Compare 2–3 properties side-by-side in a modal.
- Details shown: location, price, amenities, potential ROI, etc.

### 💡 Smart Recommendation Engine
- Suggests properties based on user behavior and preferences.
- Reactivity based on bookmarks, filters, and visit history.

### 🧠 AI-Powered Chatbot (LLM-based)
- In-built chatbot powered by LLM (Python backend).
- Assist with queries like “Best investment under 80L in Gachibowli?”
- Real-time property lookup & info retrieval.

### 📈 Investment Analyzer (Broker & Client Views)
- Analyze property potential: ROI, location trend, past value.
- Visual graphs and charts in a modal.
- Different metrics for brokers vs clients.

### 🟢 Green Score & Sustainability Metrics
- Evaluate properties based on eco-friendliness and infrastructure.
- Green Score shown on cards and details view.

### 💬 Sentiment Analysis of Client Messages
- Detects sentiment from client feedback, chat, and reviews.
- Helps brokers identify concerns or high-interest leads.

### 🔄 Status Approval by Broker
- Property status changes require broker approval.
- Workflow control for actions like publishing, booking, or document submission.

### 📁 Document Upload & Compliance Tracking
- Upload lease files, agreements (client-side only).
- Compliance checklist with localStorage persistence (no backend mutation).

### 🧩 In-Dashboard CRM: HubSpot-Style
- Add, view, update, delete contacts.
- View visit history and engagement per contact.
- Broker-only access to CRM features.

### 🔐 Security Measures
- Middleware for auth, input validation.
- Rate limiting, secure local storage, and file type checks.
- No sensitive operations on MongoDB after initial load.

### 📊 Automated Sync with Google Sheets
- Property visit data auto-synced to a connected Google Sheet.
- Useful for brokers to export and maintain offline logs.

---

## 🛠️ Tech Stack

| Layer       | Technologies |
|-------------|--------------|
| **Frontend** | React (Vite), Tailwind CSS, Chart.js, React Router |
| **Backend**  | Node.js, Express, Express Validator, Python (chatbot) |
| **Database** | MongoDB (Read-Only), Google Sheets API |
| **Tools & APIs** | HubSpot API, LocalStorage, Google Maps/Location, OpenAI LLM |
| **Security** | Express-rate-limit, JWT/Auth Middleware (for protected routes) |

---

## 🧪 How to Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/VenkataHarshini7/Real-Agent.git
cd Real-Agent/finalcbre

# 2. Install frontend and backend dependencies
npm install
cd backend && npm install
cd ../hubspot-proxy && npm install

# 3. Start backend servers
cd ../backend
node server.js

# 4. Start frontend
cd ../
npm run dev
