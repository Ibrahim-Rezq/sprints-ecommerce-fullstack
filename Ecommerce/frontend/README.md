# E-commerce Frontend - React Application

## 📋 Overview

A modern, responsive e-commerce single-page application built with **React.js** and **Redux Toolkit**. This frontend application provides a complete shopping experience with product browsing, cart management, user authentication, and order tracking. Developed as part of the **Sprints Bootcamp Program** by a team of 5 frontend developers.

---

## 🛠️ Technology Stack

### Core Technologies
- **React.js v18** - UI library for building user interfaces
- **Redux Toolkit** - State management
- **React Router v6** - Client-side routing and navigation

### UI & Styling
- **Bootstrap v5** - Responsive UI framework
- **Styled Components** - CSS-in-JS for component styling
- **React Icons** - Icon library
- **React Responsive Carousel** - Image carousel component

### HTTP & Data Management
- **Axios** - Promise-based HTTP client
- **React Debounce Input** - Debounced input components

### Development Tools
- **Create React App** - Build tooling and configuration
- **ESLint** - Code linting
- **React Scripts** - Development and build scripts

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm (v6 or higher)
- Backend API running on `http://127.0.0.1:8000`

### Installation

1. **Navigate to frontend directory:**
```bash
cd Ecommerce/frontend
```

2. **Install dependencies:**
```bash
npm install
```

3. **Configure environment variables:**

Create a `.env` file in the frontend root directory:
```env
REACT_APP_API_KEY=http://127.0.0.1:8000/
```

**Important:** The `.env` file must be in `.gitignore` for security.

4. **Start development server:**
```bash
npm start
```

The application will open at `http://localhost:3000`

---

## 📜 Available Scripts

| Script | Command | Description |
|--------|---------|-------------|
| Start | `npm start` | Runs the app in development mode |
| Build | `npm run build` | Builds the app for production |
| Test | `npm test` | Launches the test runner |
| Lint | `npm run lint` | Runs ESLint on source files |
| Eject | `npm run eject` | Ejects from Create React App (one-way operation) |

### Development Mode
```bash
npm start
```
- Opens on `http://localhost:3000`
- Hot-reloads on code changes
- Shows lint errors in console

### Production Build
```bash
npm run build
```
- Creates optimized production build in `build/` folder
- Minifies and optimizes assets
- Includes content hashes for caching
- Ready for deployment

---

## 📁 Project Structure

```
frontend/
├── src/
│   ├── pages/                    # Page components (Views)
│   │   ├── Home.jsx             # Landing page
│   │   ├── About.jsx            # About page
│   │   ├── Products.jsx         # Product listing page
│   │   ├── SingleProduct.jsx   # Product detail page
│   │   ├── Cart.jsx             # Shopping cart page
│   │   ├── CheckOut.jsx         # Checkout page
│   │   ├── LoginRegister.jsx   # Authentication page
│   │   └── AccountInfo.jsx      # User account page
│   │
│   ├── components/              # Reusable UI components
│   │   ├── Navigation/          # Navigation components
│   │   │   ├── Navigation.jsx
│   │   │   ├── NavLinks.jsx
│   │   │   └── ProtectedLinks.jsx
│   │   │
│   │   ├── Home/               # Home page components
│   │   │   ├── Hero.jsx
│   │   │   ├── Featured.jsx
│   │   │   └── Contact.jsx
│   │   │
│   │   ├── Products/           # Product components
│   │   │   ├── ProductsView.jsx
│   │   │   ├── Filters.jsx
│   │   │   ├── ProductCard.jsx
│   │   │   └── ProductImagePreview.jsx
│   │   │
│   │   ├── ProductDetail/      # Single product components
│   │   │   ├── AddToCart.jsx
│   │   │   ├── AddToCartButton.jsx
│   │   │   ├── CartAmountButtons.jsx
│   │   │   ├── ProductReviews.jsx
│   │   │   ├── SingleProductReview.jsx
│   │   │   └── AddReview.jsx
│   │   │
│   │   ├── Cart/               # Cart components
│   │   │   ├── CartView.jsx
│   │   │   ├── CartItem.jsx
│   │   │   └── ProceedToCheckOut.jsx
│   │   │
│   │   ├── Orders/             # Order components
│   │   │   ├── OrdersView.jsx
│   │   │   └── SingleOrder.jsx
│   │   │
│   │   ├── Admin/              # Admin dashboard components
│   │   │   ├── AdminDashboard.jsx
│   │   │   ├── Sales.jsx
│   │   │   ├── SalesData.jsx
│   │   │   ├── Products.jsx
│   │   │   ├── ProductsData.jsx
│   │   │   ├── Customers.jsx
│   │   │   ├── CustomersData.jsx
│   │   │   └── Edits.jsx
│   │   │
│   │   └── Account/            # Account components
│   │       ├── AccountInfo.jsx
│   │       └── Profile.jsx
│   │
│   ├── redux/                   # State management
│   │   ├── store.js            # Redux store configuration
│   │   ├── slices/             # Redux slices
│   │   │   ├── authSlice.js
│   │   │   ├── productsSlice.js
│   │   │   ├── cartSlice.js
│   │   │   └── ordersSlice.js
│   │
│   ├── assets/                  # Static assets
│   │   ├── images/
│   │   └── icons/
│   │
│   ├── css/                     # Global styles
│   │   └── index.css
│   │
│   ├── utils/                   # Utility functions
│   │   ├── priceFormatting.js
│   │   ├── dataHelpers.js
│   │   └── validators.js
│   │
│   ├── App.js                   # Main App component
│   ├── index.js                 # Entry point
│   └── setupProxy.js            # Proxy configuration
│
├── public/                      # Public assets
│   ├── index.html
│   └── favicon.ico
│
├── .env                         # Environment variables
├── .gitignore
├── package.json
└── README.md
```

---

## 🏗️ Component Architecture

### Page Components
Each page includes **Navigation** and **Footer** components and serves as a container for specific features:

- **Home** - Landing page with hero section and featured products
- **About** - Company information and mission
- **Products** - Product catalog with filtering and search
- **SingleProduct** - Detailed product view with reviews
- **Cart** - Shopping cart management
- **CheckOut** - Order checkout process
- **Login/Register** - User authentication
- **AccountInfo** - User profile and settings

### Component Patterns

**Functional Components:**
- All components are functional components using React Hooks
- Components marked with `F->something` indicate functions passed from parent

**Static vs Dynamic:**
- Static components render without external data
- Dynamic components receive props and manage local state

**Reusable Components:**
- Small, focused components with single responsibility
- Prop-driven for maximum reusability

---

## 🔄 State Management with Redux Toolkit

### Store Structure

The application uses Redux Toolkit for centralized state management:

```javascript
// Store configuration
{
  auth: {
    user: {},
    token: '',
    isAuthenticated: false
  },
  products: {
    items: [],
    loading: false,
    filters: {}
  },
  cart: {
    items: [],
    totalAmount: 0,
    totalPrice: 0
  },
  orders: {
    items: [],
    currentOrder: {}
  }
}
```

### Redux Slices

**authSlice** - User authentication and session
- Login/logout actions
- Token management
- User profile

**productsSlice** - Product catalog
- Fetch all products
- Filter and search
- Product details

**cartSlice** - Shopping cart
- Add/remove items
- Update quantities
- Calculate totals

**ordersSlice** - Order management
- Create orders
- Track order status
- Order history

---

## 🎨 Styling Approach

### Styled Components
Used for component-level styling with the following benefits:
- Scoped CSS to avoid conflicts
- Dynamic styling based on props
- Better component encapsulation

```javascript
import styled from 'styled-components';

const Button = styled.button`
  background: ${props => props.primary ? 'blue' : 'white'};
  padding: 10px 20px;
  border-radius: 4px;
`;
```

### Bootstrap
Used for:
- Grid system and layout
- Responsive utilities
- Pre-built components (modals, forms, cards)

### Global Styles
`index.css` contains:
- CSS variables for theming
- Global resets
- Typography
- Utility classes

---

## 🔌 API Integration

### Axios Configuration

The app uses Axios for HTTP requests with a configured base URL:

```javascript
import axios from 'axios';

const API = axios.create({
  baseURL: process.env.REACT_APP_API_KEY,
  headers: {
    'Content-Type': 'application/json'
  }
});

// Request interceptor for auth token
API.interceptors.request.use((config) => {
  const token = localStorage.getItem('token');
  if (token) {
    config.headers.Authorization = `Bearer ${token}`;
  }
  return config;
});
```

### API Endpoints Used

- **Authentication**: `/users/login/`, `/users/register_user/`
- **Products**: `/products/`, `/products/{id}/`
- **Orders**: `/orders/`, `/orders/add_order/`, `/orders/my_orders/`
- **User**: `/users/get_user/`, `/users/update_user/`

---

## 🛡️ Protected Routes

Routes are protected using a custom `ProtectedRoute` component:

```javascript
<Route 
  path="/checkout" 
  element={
    <ProtectedRoute>
      <CheckOut />
    </ProtectedRoute>
  } 
/>
```

Redirects unauthenticated users to login page.

---

## 📚 What We Learned

### React Development
- Component composition and reusability
- React Hooks (useState, useEffect, useContext, custom hooks)
- React Router v6 navigation and protected routes
- Performance optimization techniques

### State Management
- Redux Toolkit setup and configuration
- Creating slices and reducers
- Async thunks for API calls
- Connecting components with useSelector and useDispatch

### Modern JavaScript
- ES6+ features (destructuring, spread operator, arrow functions)
- Async/await for asynchronous operations
- Array methods (map, filter, reduce)
- Module imports/exports

### UI/UX Development
- Responsive design principles
- Bootstrap grid system
- CSS-in-JS with Styled Components
- Form validation and error handling
- Loading states and user feedback

### Team Collaboration
- Git workflow and branching strategies
- Code reviews and pull requests
- Component documentation
- Consistent coding standards
- Task distribution and coordination

---

## 👥 Frontend Team

**Frontend Lead Developer:**
- **Ibrahim Rezq** - [@Ibrahim-Rezq](https://github.com/Ibrahim-Rezq)
  - Project architecture and component structure
  - Redux Toolkit implementation
  - Team coordination and code reviews
  - Core feature development
  - Technical decision-making

**Frontend Developers:**
- **Habiba Mohammad** - [@Habiba-Mohammad](https://github.com/Habiba-Mohammad)
  - UI component development
  - Product pages and filtering

- **Wespro** - [@Wespro](https://github.com/Wespro)
  - Cart and checkout functionality
  - Form components

- **Seif Omran** - [@seifomran132](https://github.com/seifomran132)
  - Authentication components
  - User profile features

- **Ebrahim** - [@Ebrahim15](https://github.com/Ebrahim15)
  - Admin dashboard components
  - Data visualization

---

## 🔧 Development Guidelines

### Code Style
- Use functional components with hooks
- Follow React best practices
- Keep components small and focused
- Use meaningful variable and function names
- Comment complex logic

### File Naming
- Components: PascalCase (e.g., `ProductCard.jsx`)
- Utilities: camelCase (e.g., `priceFormatting.js`)
- Styles: kebab-case (e.g., `main-header.css`)

### Git Workflow
- Create feature branches from main
- Write descriptive commit messages
- Review code before merging
- Keep commits focused and atomic

---

## 🐛 Troubleshooting

### Common Issues

**Issue: API connection errors**
```
Solution: Ensure backend is running on http://127.0.0.1:8000
Check .env file has correct REACT_APP_API_KEY
```

**Issue: Module not found errors**
```
Solution: Delete node_modules and package-lock.json
Run: npm install
```

**Issue: Port 3000 already in use**
```
Solution: Kill the process or run on different port
Run: PORT=3001 npm start
```

---

## 📝 Project Context

This frontend application was developed as part of the **Sprints Bootcamp Program** by a team of 5 developers. The project demonstrates:

- Modern React.js development practices
- Team collaboration on a large-scale application
- Redux Toolkit for state management
- Integration with RESTful APIs
- Responsive and accessible UI design

---

## 🙏 Acknowledgments

- Sprints Bootcamp Program for the learning opportunity
- Backend team for the robust API
- React community for excellent documentation and resources
- All frontend team members for their dedication and contributions

---

## 📄 License

This project was created as part of the Sprints Bootcamp Program.

---

## 🔗 Related Links

- **Main Repository**: [sprints-ecommerce-fullstack](https://github.com/Ibrahim-Rezq/sprints-ecommerce-fullstack)
- **Backend Repository**: [Sprints Online Store API Backend](https://github.com/Ahmed-Abdelgawad-Dev/Sprints_Online_Store_API_Backend)
- **Create React App Documentation**: [https://create-react-app.dev](https://create-react-app.dev)
- **Redux Toolkit Documentation**: [https://redux-toolkit.js.org](https://redux-toolkit.js.org)
