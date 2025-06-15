# PJ Farmers Market

A modern e-commerce platform connecting local farmers and artisans with customers, built with Next.js, Supabase, and Stripe.

## 🌱 About

PJ Farmers Market is a digital marketplace that enables local vendors to sell their products directly to customers. The platform supports multiple vendor accounts, product listings, shopping cart functionality, secure checkout with Stripe, and vendor dashboards for managing products and orders.

## 🚀 Features

- **User Authentication**
  - Customer and vendor registration/login
  - Session management with NextAuth.js
  - Secure password handling with bcrypt

- **Product Management**
  - Vendors can create, edit, and delete products
  - Product categorization and search
  - Image upload and management

- **Shopping Experience**
  - Product browsing and filtering
  - Shopping cart functionality
  - Responsive product detail pages

- **Checkout & Payments**
  - Secure checkout with Stripe
  - Support for multiple payment methods
  - Order tracking and history

- **Vendor Dashboard**
  - Sales analytics and reporting
  - Order management
  - Stripe Connect integration for direct payments

- **Modern UI/UX**
  - Responsive design with Tailwind CSS
  - Smooth animations with Framer Motion
  - Interactive components with shadcn/ui

## 💻 Tech Stack

- **Frontend**
  - Next.js 15.x (React framework)
  - Tailwind CSS (Styling)
  - Framer Motion (Animations)
  - shadcn/ui (UI components)
  - React Hot Toast (Notifications)

- **Backend**
  - Next.js API Routes
  - Supabase (Database & Authentication)
  - NextAuth.js (Authentication)
  - Stripe (Payment Processing)

- **Deployment**
  - Vercel (Recommended)

## 🛠️ Getting Started

### Prerequisites

- Node.js 18.x or higher
- npm or yarn
- Supabase account
- Stripe account

### Environment Variables

Create a `.env.local` file in the root directory with the following variables:

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key

NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret

NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your_nextauth_secret

NEXT_PUBLIC_BASE_URL=http://localhost:3000
```

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/PJFarmersMarket.git
   cd PJFarmersMarket
   ```

2. Install dependencies
   ```bash
   npm install
   # or
   yarn install
   ```

3. Run the development server
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## 📊 Database Schema

The application uses Supabase with the following main tables:
- `customer` - Customer user data
- `vendor` - Vendor user data
- `product` - Product listings
- `cart_items` - Shopping cart items
- `orders` - Order information
- `order_items` - Items within orders
- `stripe_accounts` - Vendor Stripe Connect accounts

## 🔒 Authentication

The application uses NextAuth.js with a custom CredentialsProvider that authenticates against Supabase. User passwords are hashed with bcrypt before storage.

## 💳 Payment Processing

Payments are processed through Stripe with support for:
- Regular checkout for customers
- Stripe Connect for vendor payouts
- Automatic fee calculation and distribution

## 🚀 Deployment

The application can be deployed on Vercel:

```bash
npm run build
# or
yarn build
```

## 📝 License

[MIT](https://choosealicense.com/licenses/mit/)

## 👥 Contributors

- [Your Name](https://github.com/yourusername)
