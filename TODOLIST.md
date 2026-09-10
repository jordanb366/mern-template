# MERN Template with Authentication - Todo List

## Phase 1: Project Setup

- [x] Create project root directory structure (`server/`, `client/`)
- [x] Initialize backend with `npm init -y` in `/server`
- [x] Create `.env.example` in `/server` (template for environment variables)
- [x] Initialize frontend with `npx create-react-app client` or `npm create vite@latest client`
- [x] Create `.env.example` in `/client`
- [x] Create `.gitignore` at project root
- [x] Initialize git repository

## Phase 2: Backend - Dependencies & Configuration

- [x] Install backend dependencies:
  - [x] `express`
  - [x] `mongoose`
  - [x] `jsonwebtoken`
  - [x] `bcryptjs`
  - [x] `dotenv`
  - [x] `cors`
  - [x] `express-validator`
  - [x] `nodemon` (dev dependency)
- [x] Create `server/config/db.js` for MongoDB connection
- [x] Create `server/config/env.js` to load environment variables
- [ ] Update `server/package.json` with start scripts

## Phase 3: Backend - User Model & Schema

- [ ] Create `server/models/User.js` with:
  - [ ] Email field (unique, validated)
  - [ ] Password field (hashed)
  - [ ] Name field
  - [ ] Timestamps
  - [ ] Any additional fields needed

## Phase 4: Backend - Authentication Utilities

- [ ] Create `server/utils/jwt.js` with functions to:
  - [ ] Generate access token
  - [ ] Generate refresh token
  - [ ] Verify tokens
- [ ] Create `server/utils/password.js` with:
  - [ ] Hash password function
  - [ ] Compare password function

## Phase 5: Backend - Authentication Middleware

- [ ] Create `server/middleware/auth.js` to:
  - [ ] Verify JWT tokens
  - [ ] Extract user info from token
  - [ ] Handle expired/invalid tokens

## Phase 6: Backend - Authentication Routes & Controllers

- [ ] Create `server/controllers/authController.js` with:
  - [ ] Register controller (validate input, hash password, create user)
  - [ ] Login controller (verify credentials, issue tokens)
  - [ ] Refresh token controller (issue new access token)
  - [ ] Logout controller (optional: token blacklist)
- [ ] Create `server/routes/auth.js` with endpoints:
  - [ ] `POST /auth/register`
  - [ ] `POST /auth/login`
  - [ ] `POST /auth/refresh`
  - [ ] `POST /auth/logout`

## Phase 7: Backend - User Routes & Controllers (Optional)

- [ ] Create `server/controllers/userController.js` with:
  - [ ] Get current user profile
  - [ ] Update user profile
  - [ ] Get all users (admin only, optional)
- [ ] Create `server/routes/users.js` with protected endpoints

## Phase 8: Backend - Server Setup

- [ ] Create `server/server.js` with:
  - [ ] Express app initialization
  - [ ] Middleware setup (cors, bodyParser, dotenv)
  - [ ] Database connection
  - [ ] Route registration
  - [ ] Error handling middleware
- [ ] Test backend endpoints with Postman/Insomnia

## Phase 9: Frontend - Dependencies

- [ ] Install frontend dependencies:
  - [ ] `axios`
  - [ ] `react-router-dom`
- [ ] Update `.env` with `REACT_APP_API_URL` (or `VITE_API_URL` for Vite)

## Phase 10: Frontend - Auth Context

- [ ] Create `src/context/AuthContext.jsx` with:
  - [ ] Auth state (user, isAuthenticated, loading, error)
  - [ ] Login action
  - [ ] Register action
  - [ ] Logout action
  - [ ] Refresh token on mount
- [ ] Create `src/context/AuthProvider.jsx` to wrap the app

## Phase 11: Frontend - Custom Hooks

- [ ] Create `src/hooks/useAuth.js` to access auth context
- [ ] Create `src/hooks/useFetch.js` for API calls with token injection
- [ ] Create `src/hooks/useLocalStorage.js` for token persistence (optional)

## Phase 12: Frontend - API Service

- [ ] Create `src/services/api.js` with:
  - [ ] Axios instance configuration
  - [ ] Request interceptor (attach JWT token)
  - [ ] Response interceptor (handle token refresh, errors)
  - [ ] Auth API functions (register, login, logout, refresh)

## Phase 13: Frontend - Protected Routes

- [ ] Create `src/components/PrivateRoute.jsx`:
  - [ ] Check if user is authenticated
  - [ ] Redirect to login if not authenticated
  - [ ] Render component if authenticated

## Phase 14: Frontend - Pages

- [ ] Create `src/pages/LoginPage.jsx` with:
  - [ ] Login form (email, password)
  - [ ] Error handling
  - [ ] Redirect to dashboard on success
- [ ] Create `src/pages/RegisterPage.jsx` with:
  - [ ] Registration form (name, email, password, confirm password)
  - [ ] Validation feedback
  - [ ] Redirect to login on success
- [ ] Create `src/pages/DashboardPage.jsx` (or HomePage.jsx) with:
  - [ ] Welcome message with user name
  - [ ] Logout button
  - [ ] Protected content example

## Phase 15: Frontend - Routing Setup

- [ ] Update `src/App.jsx` with:
  - [ ] BrowserRouter setup
  - [ ] Route definitions
  - [ ] PrivateRoute usage
  - [ ] Redirect logic

## Phase 16: Frontend - Token Persistence

- [ ] Implement localStorage/sessionStorage for tokens
- [ ] Restore auth state on app load
- [ ] Auto-refresh token before expiry (optional)

## Phase 17: Testing & Integration

- [ ] Test complete auth flow:
  - [ ] Register new user
  - [ ] Login with credentials
  - [ ] Access protected routes
  - [ ] Refresh token
  - [ ] Logout
- [ ] Test error scenarios:
  - [ ] Invalid credentials
  - [ ] Expired token
  - [ ] Missing token
  - [ ] Validation errors

## Phase 18: Documentation & Finalization

- [ ] Write comprehensive README with:
  - [ ] Project overview
  - [ ] Installation instructions
  - [ ] Environment variables setup
  - [ ] Running the project
  - [ ] API endpoints documentation
  - [ ] Customization guide
- [ ] Create `.env.example` files for both server and client
- [ ] Add comments to key files
- [ ] Remove console.logs and sensitive data
- [ ] Test full production-ready setup

---

**Tip**: Start with Phase 1-8 to get the backend working, then move to Phase 9-15 for the frontend. Test early and often!
