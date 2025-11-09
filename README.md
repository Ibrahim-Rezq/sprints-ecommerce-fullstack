# Sprints E-commerce Full Stack

## 📋 Project Overview

A full-stack e-commerce web application built with **Django REST API** backend and **React.js** frontend. This project was developed as part of the **Sprints Bootcamp Program** through a collaborative team effort, showcasing modern web development practices, RESTful API design, and single-page application architecture.

The application provides a complete online shopping experience with user authentication, product browsing, shopping cart functionality, order management, and an admin dashboard.

---

## 🏗️ Architecture

### Full Stack Architecture

This project demonstrates a **complete separation of concerns** between frontend and backend:

- **Backend (Django REST API)**: Handles business logic, data persistence, authentication, and serves RESTful endpoints
- **Frontend (React SPA)**: Provides an interactive user interface, manages client-side state with Redux Toolkit, and communicates with the backend via HTTP requests
- **Database (SQLite/PostgreSQL)**: Stores users, products, orders, and relationships

### Team Collaboration

The project was split between two specialized teams:
- **Backend Team**: Django REST API development
- **Frontend Team**: React.js SPA development

---

## 🛠️ Technology Stack

### Backend
- **Django** - Python web framework
- **Django REST Framework** - RESTful API toolkit
- **SQLite** - Development database (PostgreSQL ready for production)
- **python-dotenv** - Environment variable management

### Frontend
- **React.js** - UI library
- **Redux Toolkit** - State management
- **React Router v6** - Client-side routing
- **Axios** - HTTP client
- **Bootstrap** - UI framework
- **Styled Components** - CSS-in-JS styling
- **React Icons** - Icon library

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- Node.js 14 or higher
- npm or yarn
- pip (Python package manager)

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/Ibrahim-Rezq/sprints-ecommerce-fullstack.git
cd sprints-ecommerce-fullstack
```

#### 2. Backend Setup

**Create and activate virtual environment:**
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Or using conda
conda create -n ecommerce python=3.8
conda activate ecommerce
```

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Configure environment variables:**

Create a `.env` file in the backend root directory:
```env
SECRET_KEY=your-django-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```

**Run migrations:**
```bash
python manage.py migrate
```

**Create admin user:**
```bash
python manage.py createsuperuser
```

**Start backend server:**
```bash
python manage.py runserver
```
Backend will run on `http://127.0.0.1:8000`

#### 3. Frontend Setup

**Navigate to frontend directory:**
```bash
cd Ecommerce/frontend
```

**Install dependencies:**
```bash
npm install
```

**Configure environment variables:**

Create a `.env` file in the frontend directory:
```env
REACT_APP_API_KEY=http://127.0.0.1:8000/
```

**Start frontend development server:**
```bash
npm start
```
Frontend will run on `http://localhost:3000`

---

## 🔌 API Endpoints

### Authentication & Users

| Endpoint | Method | Parameters | Description |
|----------|--------|------------|-------------|
| `/users/register_user/` | POST | firstname, lastname, username, password | Register new user |
| `/users/login/` | POST | username, password | User login (returns token) |
| `/users/get_user/` | GET | - | Get current user details |
| `/users/get_users/` | GET | - | Get all users (admin) |
| `/users/update_user/` | PUT | user fields | Update user information |

### Products

| Endpoint | Method | Parameters | Description |
|----------|--------|------------|-------------|
| `/products/` | GET | - | Get all products |
| `/products/{id}/` | GET | id | Get single product details |

### Orders

| Endpoint | Method | Parameters | Description |
|----------|--------|------------|-------------|
| `/orders/` | GET | - | Get user's orders |
| `/orders/add_order/` | POST | order details | Create new order |
| `/orders/my_orders/` | GET | - | Get current user's orders |
| `/orders/{order_id}/` | GET | order_id | Get order by ID |
| `/orders/{order_id}/paid/` | POST | order_id | Mark order as paid |
| `/orders/{order_id}/Delivered/` | POST | order_id | Mark order as delivered |

---

## 📁 Project Structure

```
sprints-ecommerce-fullstack/
├── Ecommerce/
│   └── frontend/              # React frontend application
│       ├── src/
│       │   ├── pages/        # Page components (views)
│       │   ├── components/   # Reusable UI components
│       │   ├── assets/       # Images and static files
│       │   ├── css/          # Global styles
│       │   ├── utils/        # Utility functions
│       │   └── redux/        # Redux store and slices
│       ├── public/
│       └── package.json
├── backend/                   # Django backend (if included)
│   ├── users/                # User authentication app
│   ├── products/             # Products app
│   ├── orders/               # Orders app
│   ├── manage.py
│   └── requirements.txt
├── Schema.png                # Database schema diagram
└── README.md
```

---

## 🗄️ Database Schema

The database schema diagram (`Schema.png`) is located in the root folder, showing the relationships between:
- **Users** - Customer accounts and authentication
- **Products** - Product catalog
- **Orders** - Order management
- **Order Items** - Many-to-many relationship between orders and products

---

## 🎯 Key Features

### User Features
- User registration and authentication
- Browse product catalog
- Product search and filtering
- Shopping cart management
- Order creation and tracking
- User profile management

### Admin Features
- Product management (CRUD operations)
- Order management
- User management
- Sales dashboard
- Customer data analytics

---

## 📚 What We Learned

### Backend Development
- RESTful API design principles
- Django REST Framework best practices
- Database schema design and relationships
- Authentication and authorization
- API endpoint development and testing
- Environment configuration management

### Frontend Development
- React.js component architecture
- Redux Toolkit for state management
- React Router v6 for navigation
- API integration with Axios
- Responsive design with Bootstrap
- CSS-in-JS with Styled Components
- Reusable component patterns
- Team collaboration on large-scale React projects

### Full Stack Integration
- Frontend-backend communication
- CORS configuration
- API consumption best practices
- Environment variable management
- Full stack application deployment strategies

---

## 👥 Team & Contributors

### Frontend Team (React.js)

**Frontend Lead Developer:**
- **Ibrahim Rezq** - [@Ibrahim-Rezq](https://github.com/Ibrahim-Rezq) (37 commits)
  - Project architecture and component structure
  - Redux Toolkit state management
  - Team coordination and code reviews
  - Core feature implementation

**Frontend Developers:**
- **Habiba Mohammad** - [@Habiba-Mohammad](https://github.com/Habiba-Mohammad) (15 commits)
- **Wespro** - [@Wespro](https://github.com/Wespro) (10 commits)
- **Seif Omran** - [@seifomran132](https://github.com/seifomran132) (6 commits)
- **Ebrahim** - [@Ebrahim15](https://github.com/Ebrahim15) (2 commits)

### Backend Team (Django REST API)

**Backend Lead Developer:**
- **Ahmed Abdelgawad** - [@Ahmed-Abdelgawad-Dev](https://github.com/Ahmed-Abdelgawad-Dev)
  - Complete Django REST API implementation
  - Database design and migrations
  - Authentication system
  - All API endpoints

---

## 📝 Project Context

This project was developed as part of the **Sprints Bootcamp Program** to demonstrate full-stack web development skills through team collaboration. The project showcases:

- **Team Collaboration**: Coordinated development between frontend and backend teams
- **Modern Web Stack**: Industry-standard technologies (Django + React)
- **Professional Practices**: Git workflow, code reviews, and documentation
- **Real-world Application**: Complete e-commerce platform with authentication and payments

---

## 🔧 Development Tools

- **VS Code** - IDE
- **GitHub** - Source control and collaboration
- **Trello** - Task management
- **Slack** - Team communication
- **Postman** - API testing (backend)
- **React DevTools** - React debugging (frontend)

---

## 🙏 Acknowledgments

- Sprints Bootcamp Program for the project opportunity
- All team members for their contributions
- Django and React communities for excellent documentation

---

## 📄 License

This project was created as part of the Sprints Bootcamp Program.

---

## 🔗 Related Repositories

- **Backend Repository**: [Sprints Online Store API Backend](https://github.com/Ahmed-Abdelgawad-Dev/Sprints_Online_Store_API_Backend)
- **Main Repository**: [sprints-ecommerce-fullstack](https://github.com/Ibrahim-Rezq/sprints-ecommerce-fullstack)
