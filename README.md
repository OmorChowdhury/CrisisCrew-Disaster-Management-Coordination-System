# 🚨 CrisisCrew - Disaster Management & Coordination System

A comprehensive web-based disaster management platform designed to streamline disaster response operations. CrisisCrew enables administrators, clients, and volunteers to efficiently manage disaster events, resources, and tasks through a centralized, role-based platform.

---

## 📋 Project Overview

**CrisisCrew** is a full-stack web application built to address the critical need for coordinated disaster response. In times of crisis, effective communication and resource management are essential. This system provides a unified platform where:

- **Administrators** can create and manage disaster events, assign resources, and oversee operations
- **Clients** can request assistance, track resources, and communicate with volunteers
- **Volunteers** can view active disasters, accept task assignments, and contribute to relief efforts

The platform uses role-based access control to ensure data security and streamlined workflows for different user types. Built with PHP backend and MySQL database, it's designed for rapid deployment and easy maintenance.

---

## ✨ Key Features

| Feature | Description | User Role |
|---------|-------------|-----------|
| **Role-Based Login** | Secure authentication system with Admin and Client roles | All Users |
| **Disaster Event Management** | Create, update, and manage active disaster events with details and severity levels | Admin |
| **Volunteer Task Assignment** | Assign specific tasks to volunteers and track task completion status | Admin/Volunteer |
| **Resource Tracking** | Monitor and manage available resources (medical, supplies, equipment) in real-time | Admin/Client |
| **User Profile Management** | Edit personal information, update contact details, and manage profile settings | All Users |
| **Password Recovery** | Secure password reset mechanism with email verification | All Users |
| **Dashboard Analytics** | View statistics, active events, pending tasks, and resource utilization | Admin |
| **Real-Time Notifications** | Receive updates on new tasks, event changes, and resource availability | All Users |
| **Event History & Reports** | Access historical data and generate reports for past disasters | Admin |
| **Search & Filter** | Quickly find events, tasks, volunteers, and resources | All Users |

---

## 🛠️ Tech Stack

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### Backend & Database
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

### Development Environment
![XAMPP](https://img.shields.io/badge/XAMPP-FB7185?style=for-the-badge&logo=xampp&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D42020?style=for-the-badge&logo=apache&logoColor=white)

---

## 📁 Project Folder Structure

```
CrisisCrew-Disaster-Management-Coordination-System/
│
├── README.md                           # Project documentation
├── index.php                           # Home/Landing page
├── login.php                           # User login page
├── register.php                        # User registration page
│
├── admin/                              # Admin dashboard & functions
│   ├── dashboard.php                   # Admin main dashboard
│   ├── manage_events.php               # Create/edit disaster events
│   ├── assign_tasks.php                # Assign tasks to volunteers
│   ├── manage_resources.php            # Track and manage resources
│   ├── manage_users.php                # Manage admin, client, volunteer accounts
│   ├── reports.php                     # Generate disaster reports
│   └── logout.php                      # Admin logout
│
├── client/                             # Client portal functions
│   ├── dashboard.php                   # Client main dashboard
│   ├── view_events.php                 # View active disasters
│   ├── request_assistance.php          # Submit assistance requests
│   ├── track_resources.php             # Track assigned resources
│   ├── profile.php                     # Client profile management
│   └── logout.php                      # Client logout
│
├── volunteer/                          # Volunteer portal functions
│   ├── dashboard.php                   # Volunteer main dashboard
│   ├── available_tasks.php             # View available task assignments
│   ├── my_tasks.php                    # Track assigned tasks
│   ├── profile.php                     # Volunteer profile management
│   └── logout.php                      # Volunteer logout
│
├── includes/                           # Shared PHP includes
│   ├── db_config.php                   # Database configuration
│   ├── functions.php                   # Common functions
│   ├── header.php                      # Page header template
│   ├── footer.php                      # Page footer template
│   ├── auth.php                        # Authentication functions
│   └── validation.php                  # Input validation functions
│
├── assets/                             # Static assets
│   ├── css/
│   │   ├── style.css                   # Main stylesheet
│   │   ├── dashboard.css               # Dashboard styles
│   │   └── responsive.css              # Mobile responsive styles
│   ├── js/
│   │   ├── script.js                   # Main JavaScript
│   │   ├── form_validation.js          # Client-side validation
│   │   └── ajax.js                     # AJAX functions
│   ├── images/
│   │   ├── logo.png                    # CrisisCrew logo
│   │   ├── banner.jpg                  # Hero banner
│   │   └── icons/                      # UI icons
│   └── uploads/                        # User uploads (images, documents)
│
├── database/                           # Database files
│   ├── crisiscrew_db.sql               # Database schema & initial data
│   └── backup/                         # Database backups
│
└── config/                             # Configuration files
    ├── settings.php                    # Application settings
    └── constants.php                   # Application constants
```

---

## 🚀 XAMPP Setup Instructions

### Prerequisites:
- XAMPP (Apache, PHP, MySQL) installed on your system
- [Download XAMPP](https://www.apachefriends.org/)
- PHP 7.4 or higher
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Step-by-Step Setup:

#### 1. **Start XAMPP Services**

On **Windows**:
```
1. Open XAMPP Control Panel
2. Click "Start" button next to Apache
3. Click "Start" button next to MySQL
4. Verify both are running (green indicators)
```

On **Mac/Linux**:
```bash
sudo /Applications/XAMPP/xamppfiles/bin/apache2ctl start
sudo /Applications/XAMPP/xamppfiles/bin/mysql.server start
```

#### 2. **Clone the Repository**

```bash
# Navigate to XAMPP htdocs directory
cd /xampp/htdocs  # Windows: C:\xampp\htdocs

# Clone the repository
git clone https://github.com/OmorChowdhury/CrisisCrew-Disaster-Management-Coordination-System.git

cd CrisisCrew-Disaster-Management-Coordination-System
```

#### 3. **Create Database**

```bash
# Open MySQL Command Line or phpMyAdmin

# Using MySQL Command Line:
mysql -u root -p

# Create database
CREATE DATABASE crisiscrew_db;
USE crisiscrew_db;
SOURCE database/crisiscrew_db.sql;
EXIT;
```

**Or using phpMyAdmin** (recommended):
```
1. Open http://localhost/phpmyadmin
2. Click "New" to create new database
3. Database name: crisiscrew_db
4. Click "Create"
5. Go to "Import" tab
6. Import database/crisiscrew_db.sql file
7. Click "Import"
```

#### 4. **Configure Database Connection**

Edit `includes/db_config.php`:

```php
<?php
define('DB_HOST', 'localhost');      // Database host
define('DB_USER', 'root');           // Database username
define('DB_PASS', '');               // Database password (leave empty if no password)
define('DB_NAME', 'crisiscrew_db');  // Database name
define('DB_PORT', 3306);             // MySQL port

// Connection
$conn = new mysqli(DB_HOST, DB_USER, DB_PASS, DB_NAME, DB_PORT);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

#### 5. **Access the Application**

Open your web browser and navigate to:

```
http://localhost/CrisisCrew-Disaster-Management-Coordination-System/
```

or

```
http://localhost/CrisisCrew-Disaster-Management-Coordination-System/index.php
```

#### 6. **Default Test Credentials**

After importing the database, use these credentials to test:

**Admin Account:**
```
Email: admin@crisiscrew.com
Password: admin123
```

**Client Account:**
```
Email: client@crisiscrew.com
Password: client123
```

**Volunteer Account:**
```
Email: volunteer@crisiscrew.com
Password: volunteer123
```

⚠️ **Security Note**: Change these passwords immediately in production!

#### 7. **Troubleshooting**

| Issue | Solution |
|-------|----------|
| **Port 80 already in use** | Change Apache port in httpd.conf or stop other services |
| **MySQL connection error** | Verify MySQL is running and credentials are correct in db_config.php |
| **Database import fails** | Ensure crisiscrew_db.sql file exists and is valid |
| **Blank pages/errors** | Check PHP error logs in XAMPP/php/logs/ |
| **Permission denied** | Ensure htdocs folder has proper read/write permissions |

---

## 👥 User Roles & Permissions

### 1️⃣ **Administrator**
- **Access**: Admin Dashboard
- **Permissions**:
  - Create and manage disaster events
  - Assign volunteers to tasks
  - Manage system users (add/remove/edit)
  - Allocate and track resources
  - Generate reports and analytics
  - View all activities and logs
  - Manage system settings

### 2️⃣ **Client**
- **Access**: Client Portal
- **Permissions**:
  - View active disaster events
  - Submit assistance requests
  - Track assigned resources
  - View task progress
  - Manage personal profile
  - Receive notifications

### 3️⃣ **Volunteer**
- **Access**: Volunteer Portal
- **Permissions**:
  - View available tasks
  - Accept/decline task assignments
  - Update task status
  - View assigned disasters
  - Manage personal profile
  - Receive task notifications

---

## 📊 Database Schema Overview

### Key Tables:

```sql
-- Users table
users (id, name, email, password, role, phone, address, status)

-- Disaster events
disasters (id, name, location, severity, status, description, start_date, end_date)

-- Tasks
tasks (id, disaster_id, description, priority, assigned_to, status, deadline)

-- Resources
resources (id, disaster_id, resource_type, quantity, location, status)

-- Volunteer assignments
assignments (id, volunteer_id, task_id, status, assigned_date, completed_date)

-- Requests
assistance_requests (id, client_id, disaster_id, description, status, created_at)
```

---

## 🔒 Security Features

- ✅ **Password Hashing**: Passwords encrypted using bcrypt
- ✅ **SQL Injection Prevention**: Parameterized queries with prepared statements
- ✅ **XSS Protection**: Input validation and output escaping
- ✅ **Session Management**: Secure session handling with timeouts
- ✅ **CSRF Protection**: Token-based protection on forms
- ✅ **Role-Based Access Control**: Granular permission system
- ✅ **Password Recovery**: Secure email-based password reset

---

## 🔄 How to Use

### For Administrators:

1. **Login** with admin credentials
2. **Create Disaster Event**: Go to Manage Events → New Event
3. **Add Resources**: Allocate supplies, medical equipment, personnel
4. **Assign Volunteers**: Select volunteers and assign specific tasks
5. **Monitor Progress**: Track task completion and resource utilization
6. **Generate Reports**: View analytics and historical data

### For Clients:

1. **Login** with client credentials
2. **View Active Disasters**: Check ongoing events in your area
3. **Request Assistance**: Submit aid requests with details
4. **Track Resources**: Monitor assigned aid and delivery status
5. **Update Profile**: Maintain current contact information

### For Volunteers:

1. **Login** with volunteer credentials
2. **View Available Tasks**: See all active task assignments
3. **Accept Tasks**: Choose tasks to contribute to
4. **Update Status**: Mark tasks as in-progress or completed
5. **Manage Profile**: Keep volunteer information current

---

## 🔬 Future Improvements

- [ ] **SMS Notifications**: Real-time SMS alerts for critical updates
- [ ] **Mobile App**: Native iOS and Android applications
- [ ] **GPS Tracking**: Real-time location tracking for volunteers and resources
- [ ] **API Integration**: RESTful API for third-party integrations
- [ ] **Advanced Analytics**: Machine learning for disaster prediction
- [ ] **Multi-language Support**: Support for multiple languages
- [ ] **Weather Integration**: Real-time weather data and forecasting
- [ ] **Video Conferencing**: Integrated communication for coordination
- [ ] **Blockchain Logging**: Immutable activity logs for transparency
- [ ] **Cloud Deployment**: AWS/Azure/GCP deployment options
- [ ] **Two-Factor Authentication**: Enhanced security with 2FA
- [ ] **Social Media Integration**: Share updates on social platforms
- [ ] **Accessibility**: WCAG 2.1 AA compliance
- [ ] **Performance Optimization**: Caching and database optimization

---

## 📝 Installation Checklist

- [ ] XAMPP installed and running
- [ ] Repository cloned to htdocs
- [ ] Database created (crisiscrew_db)
- [ ] Database schema imported
- [ ] db_config.php configured with correct credentials
- [ ] Folder permissions set correctly
- [ ] Application accessible at localhost URL
- [ ] Test login with default credentials
- [ ] Changed default passwords
- [ ] All features tested and working

---

## 📞 Support & Contact

For questions, bug reports, or feature requests:

- 📧 **Email**: [omorchowdhury01@gmail.com](mailto:omorchowdhury01@gmail.com)
- 💼 **LinkedIn**: [omor-chowdhury-87b4673a7](https://www.linkedin.com/in/omor-chowdhury-87b4673a7/)
- 🐙 **GitHub**: [@OmorChowdhury](https://github.com/OmorChowdhury)

---

## 📄 License

This project is open source and available under the MIT License. Feel free to use, modify, and distribute as needed for educational and commercial purposes.

---

## 🙏 Acknowledgments

- **BRAC University**: Academic support and infrastructure
- **Community Contributors**: Feedback and suggestions
- **Open Source Community**: Libraries and tools used in this project

---

<div align="center">

**⭐ If you found this project helpful, please consider starring it! ⭐**

*Helping communities respond to disasters faster, better, and stronger. 🚨*

</div>
