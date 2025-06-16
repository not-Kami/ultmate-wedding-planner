# Wedding Planner

A modern, full-stack wedding planning application to manage weddings, guests, vendors, tasks, and budgets with a beautiful and interactive UI.

---

## ✨ Features

- User authentication (register/login)
- Dashboard with wedding overview and management
- Create, edit, and delete weddings
- Manage guests (RSVP, +1, status)
- Manage vendors (type, contact, assignment)
- Task management (to-dos, priorities, deadlines)
- Budget tracking (spending, categories, status)
- Responsive, modern UI with beautiful effects (e.g. sakura petals)
- Demo account for quick testing

---

## 🛠️ Tech Stack

- **Frontend:** React, TypeScript, React Router, React Hot Toast, CSS (custom)
- **Backend:** Node.js, Express, MongoDB (Mongoose)
- **Authentication:** JWT (JSON Web Token)
- **Other:** Toast notifications, Unsplash backgrounds, Sakura petal animation

---

## 📦 Main Data Models

### User

| Field      | Type    | Description         |
|------------|---------|---------------------|
| name       | String  | User's full name    |
| email      | String  | User's email (unique) |
| password   | String  | Hashed password     |
| timestamps | Object  | Created/updated at  |

---

### Wedding

| Field      | Type    | Description         |
|------------|---------|---------------------|
| name       | String  | Wedding name        |
| date       | Date    | Wedding date        |
| place      | String  | Location            |
| vendors    | [ObjectId] | Linked vendors   |
| timestamps | Object  | Created/updated at  |

---

### Guest

| Field      | Type    | Description         |
|------------|---------|---------------------|
| wedding    | ObjectId| Linked wedding      |
| name       | String  | Guest name          |
| RSVP       | Boolean | RSVP status         |
| plusOne    | Boolean | Has +1              |
| status     | String  | 'pending', 'confirmed', 'cancelled' |
| timestamps | Object  | Created/updated at  |

---

### Vendor

| Field      | Type    | Description         |
|------------|---------|---------------------|
| name       | String  | Vendor name         |
| type       | String  | 'photographer', 'caterer', 'decorator', 'musician', 'transportation' |
| contact    | String  | Contact info        |
| wedding    | ObjectId| Linked wedding      |

---

### Task (Todo)

| Field      | Type    | Description         |
|------------|---------|---------------------|
| wedding    | ObjectId| Linked wedding      |
| title      | String  | Task title          |
| description| String  | Task details        |
| completed  | Boolean | Done or not         |
| priority   | String  | 'low', 'medium', 'high' |
| dueDate    | Date    | Deadline            |
| category   | String  | 'planning', 'venue', 'catering', etc. |
| timestamps | Object  | Created/updated at  |

---

### Budget

| Field      | Type    | Description         |
|------------|---------|---------------------|
| wedding    | ObjectId| Linked wedding      |
| spending   | Number  | Amount spent        |
| totalBudget| Number  | Total budget        |
| category   | String  | Budget category     |
| description| String  | Details             |
| status     | String  | 'pending', 'approved', 'rejected' |
| timestamps | Object  | Created/updated at  |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/wedding-planner.git
cd wedding-planner
```

### 2. Install dependencies

```bash
cd server
npm install
cd ../client
npm install
```

### 3. Configure environment

- Copy `.env.example` to `.env` in the `server` folder and fill in your MongoDB URI and JWT secret.

### 4. Start the app

```bash
# In one terminal
cd server
npm run dev

# In another terminal
cd client
npm start
```

The app will be available at [http://localhost:3000](http://localhost:3000) (or your configured port).

---

## 🧪 Demo Account

You can use the following credentials to test the app:

- **Email:** demo@weddingplanner.com
- **Password:** Demo123!

---

## 🎨 Special UI Features

- Sakura petal animation (can be toggled in code)
- Unsplash backgrounds on login/register
- Modern, accessible, and responsive design

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License

[MIT](LICENSE)

---

*This README was generated to be as complete and safe as possible, with no sensitive data included.*
