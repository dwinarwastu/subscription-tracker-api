## Features

- **Advanced Rate Limiting and Bot Protection**: with Arcjet that helps you secure the whole app.
- **Database Modeling**: Models and relationships using MongoDB & Mongoose.
- **JWT Authentication**: User CRUD operations and subscription management.
- **Global Error Handling**: Input validation and middleware integration.
- **Logging Mechanisms**: For better debugging and monitoring.
- **Email Reminders**: Automating smart email reminders with workflows using Upstash.

## Tech Stack

- Node.js
- Express.js
- MongoDB

## API Endpoints

### Authentication

- `POST /auth/sign-up` - Register a new user
- `POST /auth/sign-in` - Log in a user

### Users

- `GET /users` - Get all users
- `GET /users/:id` - Get user by ID (protected)
- `PUT /users/:id` - Update user (protected)
- `DELETE /users/:id` - Delete user (protected)

### Subscriptions

- `GET /subscriptions` - Get all subscriptions (protected)
- `GET /subscriptions/upcoming-renewals` - Get upcoming renewal subscriptions (protected)
- `GET /subscriptions/:id` - Get subscription by ID (protected)
- `POST /subscriptions` - Create a new subscription (protected)
- `PUT /subscriptions/:id` - Update subscription (protected)
- `DELETE /subscriptions/:id` - Delete subscription (protected)
- `GET /subscriptions/user/:id` - Get user's subscriptions (protected)
- `PUT /subscriptions/:id/cancel` - Cancel subscription (protected)

## Installation

1. Clone the repository

```bash
git clone https://github.com/dwinarwastu/subscription-tracker-api.git
cd subscription-tracker-api
```

2. Install dependencies

```bash
npm install
```

3. Create a `.env.local` file in the root directory with the following variables

```
# PORT
PORT=5500
SERVER_URL="http://localhost:5500"

# ENVIRONMENT
NODE_ENV=development

# DATABASE
DB_URI=

# JWT AUTH
JWT_SECRET=
JWT_EXPIRES_IN="1d"

# ARCJET
ARCJET_KEY=
ARCJET_ENV="development"

# UPSTASH
QSTASH_URL=http://127.0.0.1:8080
QSTASH_TOKEN=

# NODEMAILER
EMAIL_PASSWORD=
```

4. Run the server

```bash
npm run dev
```

## Links

- **Arcjet** - [https://launch.arcjet.com/4g2R2e4](https://launch.arcjet.com/4g2R2e4)
- **Upstash** - [https://bit.ly/42ealiN](https://bit.ly/42ealiN)
