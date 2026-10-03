# ⚙️ NXT Store — Backend API & Service Layer

The scalable backend and API architecture powering the [NXT Store E-Commerce Platform](https://github.com/muge-yilmaz/NXT-Store-Ecommerce). Built with Node.js, Express, and Prisma ORM to handle secure identity pipelines, database queries, and payment processing.

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/muge-yilmaz/ecom-backend)
[![Frontend Repo](https://img.shields.io/badge/Frontend-NXT_Store-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://github.com/muge-yilmaz/NXT-Store-Ecommerce)

---

## 🚀 Key Features

### 🛡️ Authentication & Session Security
- **Auth0 Security Integration:** Protected RESTful endpoints verifying session tokens and managing user roles.
- **Middleware Guard:** Granular access control for checkout processes and user profile management.

### 🗄️ Relational Data Layer & Queries
- **Prisma ORM & MongoDB:** Structured relational schemas and type-safe query building.
- **Optimized Pipelines:** Dynamic aggregation for catalog filtering, cart updates, and checkout status.

### 💳 Transactional Services
- **Stripe API Integration:** Server-side payment intent generation and secure webhook handling.

---

## 🛠 Tech Stack

| Category | Technologies |
| :--- | :--- |
| **Runtime & Framework** | Node.js, Express.js |
| **Database & ORM** | MongoDB Atlas, Prisma ORM |
| **Auth & Payments** | Auth0, Stripe API |
| **Testing & Tooling** | Jest, Postman, Nodemon |
| **Deployment** | Vercel / Render |

---

## ⚙️ Backend Architecture & Service Flow


```

[ Frontend / Client ]
│
├──► Auth0 Middleware (Token Verification & Identity Guard)
│         │
│         ├──► Express Controllers (Business Logic & Validation)
│         │         │
│         │         ├──► Prisma ORM ──► MongoDB Atlas (Persistence)
│         │         └──► Stripe API (Server-Side Payment Intents)
│         │
│         └──► Global Error Middleware & JSON Responses

```

---

## 💻 Local Setup & Installation

Follow these steps to run the backend API server locally:

### 1. Clone the Repository
```bash
git clone [https://github.com/muge-yilmaz/ecom-backend.git](https://github.com/muge-yilmaz/ecom-backend.git)
cd ecom-backend

```

### 2. Install Dependencies

```bash
npm install

```

### 3. Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000
DATABASE_URL="your-mongodb-prisma-connection-string"
AUTH0_SECRET="your-auth0-secret"
STRIPE_SECRET_KEY="your-stripe-secret-key"

```

### 4. Sync Database & Start Server

```bash
# Push Prisma schema to MongoDB
npx prisma db push

# Start in development mode
npm run dev

```

The server will start at `http://localhost:5000`.

---

## 👩‍💻 Author & Contact

**Müge Yılmaz** — Full-Stack Developer AI & UI/UX Engineer

* **Email:** [mugeyilmaz.web@gmail.com](https://www.google.com/search?q=mailto%3Amugeyilmaz.web%40gmail.com)
* **LinkedIn:** [linkedin.com/in/muge-yilmaz](https://linkedin.com/in/muge-yilmaz)
* **GitHub:** [github.com/muge-yilmaz](https://github.com/muge-yilmaz)
