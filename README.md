# Al-Azhar I-Pass System

**Sekolah Menengah Al-Azhar (SMAZ)**  
*"Komited Melahirkan Insan Rabbani"*  
مركز الأزهر التعليمي

---

## Overview

Al-Azhar I-Pass System is a modern, Islamic-themed Smart Dormitory Monitoring System built for Sekolah Menengah Al-Azhar (SMAZ). The system provides role-based access control for students, parents, wardens, and administrators to manage and monitor student outing requests efficiently.

## Features

### 🎨 Design
- **Modern Islamic Aesthetic** with SMAZ logo color palette
- **Split-Screen Login Page** with auto-sliding carousel
- **Glassmorphism UI** with smooth animations
- **Dark/Light Mode** toggle
- **Fully Responsive** design for all devices
- **Islamic Geometric Pattern** watermark backgrounds

### 👨‍🎓 Student Features
- View personal biodata and information
- Create outing requests with date/time selection
- Track request status (Pending, Approved, Rejected)
- View request history
- Real-time status updates

### 👨‍👩‍👦 Parent Features
- View children's information
- Submit outing requests on behalf of children
- Monitor request status and history
- Track all children's activities in one place

### 🏫 Warden Features
- Approve/Reject outing requests
- Quick "Call Parent" button
- View students currently out
- Real-time pending requests list
- Generate reports

### 🖥 Admin Features
- Full system access and management
- Add/Edit/Delete students, parents, wardens
- View all outing requests
- Generate comprehensive reports
- System statistics and analytics
- Activity logs

## Technology Stack

- **Backend**: Core PHP 7.4+
- **Database**: MySQL 5.7+
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Styling**: Custom CSS with CSS Variables
- **Fonts**: Poppins (English), Cairo (Arabic)
- **Icons**: SVG Icons

## Color Palette (SMAZ Logo)

| Color | Hex Code | Usage |
|-------|----------|-------|
| Teal Blue | `#2FA7B1` | Primary brand color |
| Red | `#D62828` | Alerts, reject actions |
| Gold | `#F4C430` | Accents, highlights |
| White | `#FFFFFF` | Backgrounds, text |
| Black | `#000000` | Text, borders |

## Installation

### Prerequisites
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Web server (Apache/Nginx)

### Setup Steps

1. **Clone/Extract** the project to your web server directory:
   ```
   /var/www/html/al-azhar-ipass/
   ```

2. **Create Database**:
   - Open phpMyAdmin or MySQL CLI
   - The setup script will create the database automatically

3. **Run Setup**:
   - Navigate to `http://your-domain.com/al-azhar-ipass/setup.php`
   - The script will create all necessary tables

4. **Default Login Credentials**:
   - **Admin**: admin@alazhar.edu / password
   - **Warden**: warden@alazhar.edu / password

5. **Configure Database** (if needed):
   - Edit `includes/config.php`
   - Update database credentials:
     ```php
     define('DB_HOST', 'localhost');
     define('DB_USER', 'root');
     define('DB_PASS', 'your_password');
     define('DB_NAME', 'alazhar_ipass');
     ```

## Database Structure

### Tables

- **users** - Base user accounts with role-based access
- **students** - Student information and dormitory details
- **parents** - Parent/Guardian information
- **wardens** - Warden/Staff information
- **admins** - Administrator accounts
- **outing_requests** - Outing request records
- **activity_logs** - System activity tracking

## File Structure

```
al-azhar-ipass/
├── assets/
│   ├── css/
│   │   └── style.css          # Main stylesheet
│   ├── js/
│   │   └── main.js            # Main JavaScript
│   └── images/                # Image assets
├── database/
│   └── schema.sql             # Database schema
├── includes/
│   ├── config.php             # Configuration & functions
│   └── dashboard-header.php   # Dashboard template
├── pages/
│   ├── student/               # Student dashboard pages
│   ├── parent/                # Parent dashboard pages
│   ├── warden/                # Warden dashboard pages
│   └── admin/                 # Admin dashboard pages
├── index.php                  # Login page
├── setup.php                  # Installation script
├── logout.php                 # Logout handler
├── redirect.php               # Role-based redirect
└── README.md                  # This file
```

## Security Features

- Password hashing with `password_hash()` / `password_verify()`
- CSRF token protection
- Session management
- SQL injection prevention with prepared statements
- XSS protection with output escaping
- Role-based access control (RBAC)

## Customization

### Changing Colors
Edit CSS variables in `assets/css/style.css`:
```css
:root {
    --color-teal: #2FA7B1;
    --color-red: #D62828;
    --color-gold: #F4C430;
    /* ... */
}
```

### Adding New Roles
1. Update the `role` ENUM in `users` table
2. Add navigation items in `includes/dashboard-header.php`
3. Create role-specific pages in `pages/{role}/`

### Modifying Carousel Slides
Edit the carousel section in `index.php`:
```php
<div class="carousel-slide" data-slide="X">
    <!-- Your content -->
</div>
```

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+
- Opera 67+

## License

This project is proprietary software developed for Sekolah Menengah Al-Azhar (SMAZ).

## Support

For technical support or feature requests, please contact the system administrator.

---

**Al-Azhar I-Pass System**  
*Smart Dormitory Monitoring System*  
Sekolah Menengah Al-Azhar (SMAZ)

"Komited Melahirkan Insan Rabbani"
