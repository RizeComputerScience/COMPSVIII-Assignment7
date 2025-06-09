# Unit 10: Automated Test Suite for Recipe Sharing Application

This repository contains the test files and configuration updates needed for Unit 10's CI/CD pipeline assignment.

## What's Included

### Backend Tests
- `backend/tests/api.test.js` - API endpoint tests for all CRUD operations
- Updated `backend/package.json` - Includes Jest and Supertest dependencies
- Updated `backend/server.js` - Modified to export app for testing

### Frontend Tests  
- `frontend/src/test/App.test.jsx` - Utility function and API integration tests
- Updated `frontend/package.json` - Includes Vitest testing dependencies
- Updated `frontend/vite.config.js` - Configured for testing environment

## Installation Instructions

1. **Copy the test files** to your Recipe Sharing Application repository
2. **Install backend dependencies**:
   ```bash
   cd backend
   npm install
   ```
3. **Install frontend dependencies**:
   ```bash
   cd frontend
   npm install
   ```
4. When done, your project should have the following structure:

```bash
recipe-app/
├── backend/
│   ├── test/
│   │   ├── api.test.js # New folder and file
│   ├── database.js
│   ├── Dockerfile
│   ├── package.json	# Updated
│   └── server.js		# Updated
├── frontend/
│   ├── src/
│   │   ├── test/
│   │   │   ├── App.test.jsx    # New folder and file
│   │   │   ├── setup.js        # New folder and file
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── Dockerfile
│   ├── index.html
│   ├── package.json	# Updated
│   └── Dockerfile	    # Updated
├── docker-compose.yml
├── cloudbuild-backend.yaml
├── cloudbuild-frontend.yaml
└── README.md
```


## Running Tests Locally

**Backend tests**:
```bash
cd backend
npm test
```

**Frontend tests**:
```bash
cd frontend
npm test
```

## What the Tests Cover

### Backend Tests
- ✅ `GET /api/recipes` - Retrieve all recipes
- ✅ `POST /api/recipes` - Create new recipe
- ✅ `GET /api/recipes/:id` - Get specific recipe
- ✅ `PUT /api/recipes/:id` - Update recipe
- ✅ `DELETE /api/recipes/:id` - Delete recipe
- ✅ Input validation and error handling

### Frontend Tests
- ✅ Recipe data validation functions
- ✅ Cooking time formatting utilities
- ✅ API URL construction
- ✅ Error handling for network failures

## Important Notes

- Tests are designed to work with your existing Recipe Sharing Application
- Backend tests expect your server to have recipe CRUD endpoints
- Frontend tests focus on utility functions rather than React components
- All tests should pass before setting up your GitHub Actions pipeline