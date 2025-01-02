# Calendar-Application-for-Communication-Tracking
Calendar Application for Communication Tracking

Open (https://gleaming-praline-34152b.netlify.app/) to view it in your browser.

## Overview
This Calendar Application is designed to help organizations efficiently track and manage communication with external companies. The application provides a centralized platform for logging past interactions, scheduling future communications, and maintaining consistent engagement.

## Features

### Admin Module
- **Company Management**:
  - Add, edit, and delete companies.
  - Include details such as:
    - Name
    - Location
    - LinkedIn Profile
    - Emails
    - Phone Numbers
    - Comments
    - Communication Periodicity

- **Communication Method Management**:
  - Define available communication methods with details:
    - Name
    - Description
    - Sequence
    - Mandatory Flag
  - Default communication methods:
    1. LinkedIn Post
    2. LinkedIn Message
    3. Email
    4. Phone Call
    5. Other

### User Module
- **Dashboard**:
  - Grid view of companies with columns for:
    - Company Name
    - Last Five Communications
    - Next Scheduled Communication
  - Color-coded highlights for overdue (red) and due-today (yellow) communications.
  - Hover tooltips for communication notes.

- **Communication Action**:
  - Log a new communication with options for:
    - Communication Type
    - Date
    - Notes
  - Reset highlights upon submission.

- **Notifications**:
  - Overdue and today’s communications grids.
  - Badge icon for overdue/due communication count.

- **Calendar View**:
  - Visualize past communications and manage upcoming ones.

### Optional Module: Reporting and Analytics
- Actionable insights into communication frequency and engagement trends.

## Setup Instructions

### Prerequisites
- Node.js (v16 or above)
- npm or yarn
- A database (PostgreSQL or MySQL recommended)

### Installation
1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:
   Create a `.env` file in the project root with the following variables:
   ```env
   DATABASE_URL=<database_connection_string>
   PORT=3000
   REACT_APP_API_URL=http://localhost:3000
   ```

4. **Setup the Database**:
   - Run migrations to set up the database schema:
     ```bash
     npm run migrate
     ```

5. **Start the Application**:
   - For development:
     ```bash
     npm start
     ```
   - For production:
     ```bash
     npm run build
     npm run start:prod
     ```

### Deployment
1. **Build the Application**:
   ```bash
   npm run build
   ```

2. **Deploy to a Hosting Service** (e.g., AWS, Heroku):
   - Ensure the database and environment variables are correctly configured on the hosting platform.

## Application Functionality

### Admin Module
- Add and manage company details.
- Configure communication methods.

### User Module
- View communication dashboards and calendars.
- Log new communications and track overdue tasks.

### Notifications
- Overdue and due-today communication highlights.

### Calendar
- Comprehensive view of past and upcoming communications.

## Known Limitations
- **Scalability**: Performance might degrade with a large number of companies or communications.
- **Time Zones**: Communication scheduling is currently not optimized for different time zones.
- **Offline Mode**: Application requires a stable internet connection for data syncing.

---
