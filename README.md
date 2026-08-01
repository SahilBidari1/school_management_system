# School Management System

A comprehensive web-based school management system built with Django (Python) for the backend and HTML, CSS, and JavaScript for the frontend.

## Features

### 🎓 Student Management
- Add, edit, and delete student records
- Student profile management with photos
- Search and filter students
- Student enrollment tracking
- Student attendance history

### 👨‍🏫 Teacher Management
- Teacher profile management
- Teacher assignment to subjects
- Teacher qualification tracking
- Experience and credentials management

### 📚 Class & Subject Management
- Class creation and management
- Subject assignment to classes
- Teacher-subject assignments
- Class capacity management

### 📊 Attendance Management
- Daily attendance tracking
- Multiple attendance statuses (Present, Absent, Late, Excused)
- Bulk attendance recording
- Attendance reports and analytics

### 📈 Grade Management
- Assignment and exam grading
- Grade calculation and tracking
- Grade reports and analytics
- Student performance monitoring

### 📋 Dashboard & Analytics
- Real-time statistics
- Recent activities overview
- Quick action buttons
- Visual data representation

## Technology Stack

### Backend
- **Django 5.1.1** - Python web framework
- **SQLite** - Database (can be easily changed to PostgreSQL/MySQL)
- **Pillow** - Image processing for profile pictures

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with custom design
- **JavaScript (ES6+)** - Interactive functionality
- **Bootstrap 5** - Responsive UI framework
- **Font Awesome** - Icons

### Additional Libraries
- **jQuery** - DOM manipulation and AJAX
- **Django Crispy Forms** - Better form rendering
- **Django Filter** - Advanced filtering capabilities

## Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd school_management_system
```

### Step 2: Create Virtual Environment
```bash
# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Database Setup
```bash
python manage.py makemigrations
python manage.py migrate
```

### Step 5: Create Superuser
```bash
python manage.py createsuperuser
```

### Step 6: Run the Development Server
```bash
python manage.py runserver
```

### Step 7: Access the Application
- Main Application: http://127.0.0.1:8000/
- Django Admin: http://127.0.0.1:8000/admin/

## Project Structure

```
school_management_system/
├── core/                          # Main Django app
│   ├── models.py                  # Database models
│   ├── views.py                   # View functions
│   ├── urls.py                    # URL patterns
│   └── admin.py                   # Admin interface
├── templates/                     # HTML templates
│   ├── base.html                  # Base template
│   └── core/                      # App-specific templates
│       ├── dashboard.html         # Dashboard page
│       ├── student_list.html      # Student listing
│       ├── student_form.html      # Student form
│       └── ...
├── static/                        # Static files
│   ├── css/
│   │   └── style.css              # Custom CSS
│   ├── js/
│   │   └── main.js                # Main JavaScript
│   └── images/                    # Images
├── media/                         # User-uploaded files
├── manage.py                      # Django management script
├── requirements.txt               # Python dependencies
└── README.md                      # This file
```

## Database Models

### Student
- Personal information (name, email, phone, address)
- Academic information (student ID, enrollment date)
- Profile picture support
- Gender and date of birth

### Teacher
- Personal and professional information
- Qualifications and experience
- Profile picture support
- Teaching assignments

### Class
- Class name and description
- Academic year and capacity
- Active/inactive status

### Subject
- Subject name and code
- Credits and description
- Active/inactive status

### ClassSubject
- Links classes with subjects
- Teacher assignments
- Schedule information

### StudentClass
- Student enrollment in classes
- Enrollment date tracking

### Attendance
- Daily attendance records
- Multiple status options
- Remarks and recording information

### Grade
- Assignment and exam grades
- Score and grade tracking
- Grading history

## Usage Guide

### 1. Dashboard
- View system statistics
- Access quick actions
- Monitor recent activities

### 2. Student Management
- Navigate to Students → All Students
- Use search functionality to find students
- Click "Add Student" to create new records
- Use action buttons to view, edit, or delete students

### 3. Teacher Management
- Navigate to Teachers → All Teachers
- Add new teachers with qualifications
- Assign teachers to subjects

### 4. Class Management
- Create and manage classes
- Assign subjects to classes
- Set class capacity and academic year

### 5. Attendance Recording
- Navigate to Attendance → Record Attendance
- Select class and subject
- Mark attendance for each student
- Save attendance records

### 6. Grade Recording
- Navigate to Grades → Record Grades
- Select class, subject, and assignment
- Enter scores and grades for students
- Add remarks if needed

## API Endpoints

### Students API
- `GET /api/students-by-class/?class_id=<id>` - Get students by class

### Subjects API
- `GET /api/class-subjects/?class_id=<id>` - Get subjects by class

## Customization

### Adding New Features
1. Create new models in `core/models.py`
2. Add views in `core/views.py`
3. Create templates in `templates/core/`
4. Update URLs in `core/urls.py`
5. Register models in `core/admin.py`

### Styling Customization
- Modify `static/css/style.css` for custom styles
- Update Bootstrap classes in templates
- Add custom JavaScript in `static/js/main.js`

### Database Configuration
- Edit `settings.py` to change database settings
- For production, use PostgreSQL or MySQL
- Configure environment variables for sensitive data

## Deployment

### Production Settings
1. Set `DEBUG = False` in settings.py
2. Configure `ALLOWED_HOSTS`
3. Set up a production database
4. Configure static file serving
5. Set up environment variables

### Environment Variables
Create a `.env` file:
```
SECRET_KEY=your-secret-key
DEBUG=False
DATABASE_URL=your-database-url
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## Future Enhancements

- [ ] User authentication and authorization
- [ ] Role-based access control
- [ ] Advanced reporting and analytics
- [ ] Email notifications
- [ ] Mobile app integration
- [ ] API for third-party integrations
- [ ] Advanced search and filtering
- [ ] Export functionality (PDF, Excel)
- [ ] Calendar integration
- [ ] Fee management system

## Screenshots

*Add screenshots of the application here*

---

**Note**: This is a development version. For production use, ensure proper security measures, data backup, and testing are implemented.
