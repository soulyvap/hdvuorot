# HDVUOROT

**HDVUOROT** is a platform that allows Metropolia IT helpdesk workers to keep track of each other's availability statuses. The app consists of a shared calendar in which users can notify others of their future absences, remote working days, and more.

## Disclaimer

Due to company restrictions, the source code is private, but I’ve documented the project here.

## Pictures

<img width="1680" alt="Screenshot 2025-02-05 at 16 05 48" src="https://github.com/user-attachments/assets/2a58b45e-c556-42b9-9362-9d1674f3fa2f" />

**Home page - Table view**: Allows a user to visualize their coworkers' status for a month, sort them and filter them by name, title, unit, location and status.

<img width="1680" alt="Screenshot 2025-02-05 at 16 06 37" src="https://github.com/user-attachments/assets/c9fae500-67b8-462e-b53d-43109923d4a9" />

**Home page - Edit mode**: Allows a user user to edit their own availability statuses or other coworker's status if the current user is an admin.

<img width="1680" alt="Screenshot 2025-02-05 at 16 08 52" src="https://github.com/user-attachments/assets/fa677e79-09e0-45c4-9f5d-f5f2eaa0cc9e" />

**Home page - Calendar view**: Allows a user to visualize their coworkers' status for a week, sorted by status.

<img width="1680" alt="Screenshot 2025-02-05 at 16 07 02" src="https://github.com/user-attachments/assets/23d0c84c-cf70-46a0-bac2-3c4afd52fb90" />

**Admin page - User management view**: Allows an admin user to add/delete/edit users on the platform.

<img width="1680" alt="Screenshot 2025-02-05 at 16 07 22" src="https://github.com/user-attachments/assets/d731f52e-43bb-44e9-81e2-6947a92625da" />

**Admin page - Unit management view**: Allows an admin user to add/delete/edit units in which employees work.

<img width="1680" alt="Screenshot 2025-02-05 at 16 07 37" src="https://github.com/user-attachments/assets/05119395-5039-4b93-945c-41410df80a26" />

**Admin page - Logs view**: Allows an admin user to visualize change logs.

<img width="369" alt="Screenshot 2025-02-05 at 16 08 24" src="https://github.com/user-attachments/assets/ccec5245-a50f-416e-b16e-5d2be4aa1bef" />

**Home page - Table view (mobile)**: Allows a user to visualize their coworkers' status for a week on a mobile phone.

## Features

- Shared calendar for tracking availability statuses, customizable from the admin panel
- Next.js 14 with server-side rendering (SSR) and static site generation (SSG)
- Sequelize for database modeling and querying
- Azure AD authentication for secure login and user management
## Prerequisites

Ensure you have the following installed:

- Node.js (v16 or later)
- npm or Yarn
- An Azure AD tenant with app registration configured

## Getting Started

### 1. Clone the Repository

```bash
$ git clone https://github.com/your-username/your-repo.git
$ cd your-repo
```

### 2. Install Dependencies

Install both frontend and backend dependencies:

```bash
# Start the frontend server
$ cd frontend && npm install

# Start the backend server
$ cd backend && npm install
```

### 3. Setup Environment Variables

#### Backend `.env` File

Create a `.env` file in the `backend` directory with the following variables:

```env
# Database Configuration
DB_URL=your_database_url

# Authentication Configuration
JWT_SECRET=your_jwt_secret

# LDAP Configuration
LDAP_URL=your_ldap_url
LDAP_USER=your_ldap_user
LDAP_PASSWORD=your_ldap_password
```

#### Frontend `.env.local` File

Create a `.env.local` file in the `frontend` directory with the following variables:

```env
# Authentication Configuration
JWT_SECRET=your_jwt_secret
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your_nextauth_secret
AZURE_AD_CLIENT_ID=your_azure_ad_client_id
AZURE_AD_CLIENT_SECRET=your_azure_ad_client_secret
AZURE_AD_TENANT_ID=your_azure_ad_tenant_id
BASE_PATH=/ (optional)
```

### 6. Start the Development Server

Run the application in development mode:

```bash
# Start the frontend server
$ cd frontend && npm run dev

# Start the backend server
$ cd backend && npm run dev
```

The application will be available at `http://localhost:3000`.

## Project Structure

```
.
├── backend
│   ├── controllers      # Request handlers for business logic
│   ├── models           # Sequelize models
│   ├── requests         # API request schemas or handlers
│   ├── utils            # Utility functions
│   ├── .env             # Backend environment variables
│   ├── app.js           # Express app setup
│   ├── index.js         # Entry point for backend
│   └── package.json     # Backend dependencies and scripts
├── frontend
│   ├── app              # Application core structure
│   │   ├── [locale]        # Locale-specific routes
│   │   ├── api             # API route handlers
│   │   ├── components      # Reusable React components
│   │   ├── enums           # Enums for static data
│   │   ├── hooks           # Custom React hooks
│   │   ├── server-actions  # Server actions for async calls
│   │   ├── favicon.ico     # App favicon
│   │   └── globals.css     # Global styles
│   ├── public            # Public assets
│   ├── translations      # Translation files for i18n
│   ├── .env.local        # Frontend environment variables
│   ├── i18n              # Internationalization setup
│   ├── middleware.ts     # Middleware configuration
│   ├── navigation.ts     # Navigation logic
│   ├── next.config.mjs   # Next.js configuration
│   ├── tailwind.config.js # TailwindCSS configuration
│   ├── tsconfig.json     # TypeScript configuration
│   └── types.d.ts        # TypeScript type definitions
├── .env                # Environment variables
├── package.json        # Root project metadata
└── README.md           # Documentation
```

## Backend Libraries

The following libraries are used in the backend:

### Dependencies

- **[cors](https://www.npmjs.com/package/cors)**: Middleware for enabling CORS.
- **[dotenv](https://github.com/motdotla/dotenv)**: Loads environment variables from a `.env` file.
- **[express](https://expressjs.com/)**: Web framework for Node.js.
- **[express-async-errors](https://www.npmjs.com/package/express-async-errors)**: Simplifies error handling in Express.
- **[jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)**: JWT implementation.
- **[ldapjs](http://ldapjs.org/)**: LDAP client library for Node.js.
- **[sequelize](https://sequelize.org/)**: Promise-based Node.js ORM.
- **[sqlite3](https://github.com/TryGhost/node-sqlite3)**: SQLite database bindings for Node.js.

### Dev Dependencies

- **[nodemon](https://nodemon.io/)**: Utility for monitoring changes in code during development.

## Frontend Libraries

The following libraries are used in the frontend:

### Dependencies

- **[@heroicons/react](https://github.com/tailwindlabs/heroicons)**: Icon set for React.
- **[@uiw/react-color](https://uiwjs.github.io/react-color/)**: Color picker components for React.
- **[axios](https://github.com/axios/axios)**: Promise-based HTTP client for the browser and Node.js.
- **[date-holidays](https://www.npmjs.com/package/date-holidays)**: Library for managing and calculating holidays.
- **[dotenv](https://github.com/motdotla/dotenv)**: Loads environment variables from a `.env` file.
- **[jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)**: JWT implementation.
- **[next](https://nextjs.org/)**: React framework for production.
- **[next-auth](https://next-auth.js.org/)**: Authentication for Next.js.
- **[next-intl](https://www.npmjs.com/package/next-intl)**: Internationalization library for Next.js.
- **[punycode](https://github.com/bestiejs/punycode.js)**: Unicode to ASCII encoding library.
- **[react](https://reactjs.org/)**: A JavaScript library for building user interfaces.
- **[react-dom](https://reactjs.org/docs/react-dom.html)**: React package for working with the DOM.
- **[zustand](https://github.com/pmndrs/zustand)**: State management library for React.

### Dev Dependencies

- **[@types/jsonwebtoken](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/jsonwebtoken)**: TypeScript definitions for jsonwebtoken.
- **[@types/node](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/node)**: TypeScript definitions for Node.js.
- **[@types/react](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/react)**: TypeScript definitions for React.
- **[@types/react-dom](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/react-dom)**: TypeScript definitions for React DOM.
- **[@typescript-eslint/eslint-plugin](https://typescript-eslint.io/)**: Linter plugin for TypeScript.
- **[@typescript-eslint/parser](https://typescript-eslint.io/)**: Linter parser for TypeScript.
- **[autoprefixer](https://github.com/postcss/autoprefixer)**: Adds vendor prefixes to CSS.
- **[eslint](https://eslint.org/)**: Pluggable JavaScript linter.
- **[eslint-config-next](https://nextjs.org/docs/basic-features/eslint)**: ESLint configuration for Next.js.
- **[eslint-config-prettier](https://github.com/prettier/eslint-config-prettier)**: Turns off ESLint rules that conflict with Prettier.
- **[eslint-config-standard-with-typescript](https://github.com/standard/eslint-config-standard-with-typescript)**: Standard JavaScript style guide with TypeScript support.
- **[eslint-plugin-import](https://github.com/import-js/eslint-plugin-import)**: Ensures proper imports.
- **[eslint-plugin-n](https://github.com/eslint-community/eslint-plugin-n)**: ESLint rules for Node.js.
- **[eslint-plugin-promise](https://github.com/eslint-community/eslint-plugin-promise)**: Enforces best practices for JavaScript promises.
- **[eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react)**: React-specific linting rules.
- **[postcss](https://postcss.org/)**: A tool for transforming CSS.
- **[prettier](https://prettier.io/)**: Code formatter.
- **[tailwindcss](https://tailwindcss.com/)**: Utility-first CSS framework.
- **[typescript](https://www.typescriptlang.org/)**: Typed superset of JavaScript.

## Scripts

- `npm run dev`: Start the development server
- `npm run build`: Build the Next.js application for production
- `npm start`: Start the production server

## Deployment

1. Build the application:

```bash
$ npm run build
```

2. Run the production server:

```bash
$ npm start
```

Ensure the `NODE_ENV` is set to `production` and the `.env` file contains production-ready configurations.

## Repository and Licensing

This repository is private and owned by Metropolia. No licensing applies to this project at this time.

## Acknowledgments

- [Next.js Documentation](https://nextjs.org/docs)
- [Sequelize Documentation](https://sequelize.org/)
- [Azure AD Documentation](https://learn.microsoft.com/en-us/azure/active-directory/)
- [Tailwind CSS](https://tailwindcss.com/)
