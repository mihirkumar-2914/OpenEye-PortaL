PROJECT NAME: OpenEye 


ABOUT:The track we have chosen is open innovation. Citizens often face difficulties such as government negligence, police misconduct, or everyday civic issues (like broken roads, sanitation, or corruption). However, fear of retaliation, social stigma, or lack of trust prevents many from voicing their concerns openly. As a result, countless problems remain unreported and unresolved, reducing accountability and weakening public trust in the system.
There is a need for a secure and anonymous complaint platform where individuals can freely report issues without fear of exposure, while ensuring authenticity and enabling authorities or communities to take action. And hence our team Techspire has innovated OpenEye which helps the people in reporting their concerns to the government without revealing their true identity which is the main crux of our portal . It acts as a bridge between the government and public . Public can report their concerns and the government authorities active can take action accordingly .


TEAM NAME: TECHSPIRE


TEAM LEADER: MIHIR KUMAR


TEAM MEMBERS: CHIRAG SHARMA,SHRI RAM AZAD and SHASHANK RAI


OpenEye - Anonymous Complaint Portal
A comprehensive web application for anonymous complaint submission and tracking, built with Python Flask backend and modern HTML/CSS frontend.

Features
Anonymous Complaint Submission: Submit complaints without revealing identity
User Management: Separate registration for Government and Public users
Complaint Tracking: Monitor complaint status and progress
Authority Management: View active government authorities
Area Coverage: Display active service areas
Responsive Design: Modern, mobile-friendly interface
Project Structure
OpenEye/
├── backend/
│   ├── __init__.py
│   └── app.py              # Main Flask application
├── templates/              # HTML templates
│   ├── index.html         # Home page
│   ├── login_register.html # User authentication
│   ├── areas.html         # Active areas page
│   ├── file_complaint.html # Complaint submission
│   ├── pending_problems.html # Complaint tracking
│   └── active_authorities.html # Government authorities
├── static/                # Static assets (CSS, JS, images)
├── requirements.txt       # Python dependencies
└── README.md             # Project documentation
Installation
Clone or navigate to the project directory

cd OpenEye
Install Python dependencies

python -m pip install -r requirements.txt
Run the application

cd backend
python app.py
Access the application

Local access: http://127.0.0.1:5000
Network access: http://192.168.0.3:5000 (for devices on same network)
Public access: Use ngrok for internet access (see Network Access section)
Usage
For Public Users
Visit the homepage to see available features
Click "File a Complaint" to submit anonymous complaints
Use "Complaint Tracker" to monitor submitted complaints
View "Active Areas" to see service coverage
Check "Active Authorities" for government contacts
For Government Users
Register or login with Government user type
Access complaint management features
View and respond to submitted complaints
Upload solutions and updates
API Endpoints
Authentication
POST /api/register - User registration
POST /api/login - User login
Complaints
GET /api/complaints - Get all complaints
POST /api/complaints - Submit new complaint
Authorities
GET /api/authorities - Get active authorities
Statistics
GET /api/stats - Get system statistics
GET /api/problems-solved - Get solved problems data
Database Models
User
User authentication and role management
Supports Government and Public user types
Complaint
Anonymous complaint storage
Unique complaint ID generation
Status tracking (pending, in_review, resolved)
Authority
Government authority information
Contact details and jurisdiction
Area
Service area definitions
Coverage information
Technology Stack
Backend
Python 3.x
Flask - Web framework
SQLAlchemy - Database ORM
Flask-Migrate - Database migrations
Flask-CORS - Cross-origin resource sharing
Frontend
HTML5 - Structure
CSS3 - Styling with modern features
JavaScript - Interactive functionality
Font Awesome - Icons
Responsive Design - Mobile-friendly layouts
Development
Adding New Features
Update database models in backend/app.py
Add new routes for API endpoints
Create corresponding HTML templates
Update frontend JavaScript for new functionality
Database Management
The application uses SQLite by default. For production, consider:

PostgreSQL or MySQL for better performance
Update SQLALCHEMY_DATABASE_URI in configuration
Use environment variables for sensitive data
Network Access
Local Network Access
The application is configured to run on all network interfaces (0.0.0.0:5000), making it accessible to other devices on the same network.

Access URLs:

Local: http://127.0.0.1:5000
Network: http://192.168.0.3:5000 (replace with your actual IP)
Public Internet Access (ngrok)
To share the application with users on different networks:

Download ngrok: https://ngrok.com/download
Create free account: https://dashboard.ngrok.com/signup
Get authtoken from dashboard
Configure ngrok:
ngrok config add-authtoken YOUR_AUTHTOKEN
Start ngrok tunnel:
ngrok http 5000
Share the public URL (e.g., https://abc123.ngrok.io)
Windows Firewall Configuration
If others can't access your app, add a firewall rule:

netsh advfirewall firewall add rule name="Python Flask" dir=in action=allow protocol=TCP localport=5000
Security Features
Password hashing using Werkzeug
CORS protection
Input validation
Anonymous complaint submission
Secure session management
Contributing
Follow the existing code structure
Maintain responsive design principles
Add proper error handling
Include user feedback for all actions
Test on multiple browsers and devices
License
This project is developed for educational and demonstration purposes.

Quick Start Guide
For Local Development
cd OpenEye/backend
python app.py
# Access at: http://127.0.0.1:5000
For Network Sharing
# Same as above, then share: http://192.168.0.3:5000
# (Replace 192.168.0.3 with your actual IP address)
For Internet Sharing
# 1. Start Flask app
cd OpenEye/backend
python app.py

# 2. In another terminal, start ngrok
ngrok http 5000

# 3. Share the ngrok URL (e.g., https://abc123.ngrok.io)
Support
For questions or issues, please contact the development team.
