# QuickShop E-Commerce Platform

A sleek, responsive, and fully-featured single-vendor E-Commerce web application built using Django. QuickShop provides a complete end-to-end shopping experience, catering to both consumers and sellers.

## Project Overview
QuickShop is a robust full-stack e-commerce architecture designed for managing products, carts, orders, and payments seamlessly. It supports role-based access, ensuring a smooth flow for both shoppers and shop administrators.

### User Roles
- **Consumers:** Can browse the product catalog, add items to their shopping cart, place orders, and manage their checkout process securely.
- **Sellers / Admins:** Have access to a dedicated dashboard to manage the product inventory (CRUD operations), track orders, and handle platform data.

## Key Modules & Features
* **Authentication (`accounts`):** Role-based seamless user registration, login, and profile management.
* **Shopping Cart (`cart`):** Session-based reliable cart mechanism allowing users to add products, adjust quantities, and save items for checkout.
* **Order Management (`orders`):** Comprehensive checkout process, order tracking, and history.
* **Products Catalog (`products`):** Interactive product browsing UI, category filtering, and image previews.
* **Seller Dashboard (`seller` & `admin_app`):** An intuitive back-office interface for sellers to add, edit, or delete products and manage stock.
* **Payments (`payment`):** Basic QR code integration and checkout flow components, scalable for integrating full payment gateways in the future.

## Tech Stack
- **Backend Framework:** Django (Python)
- **Frontend / UI:** Django Templates (HTML), standard CSS, and vanilla JavaScript
- **Database:** SQLite (Default for development)
- **Architecture Pattern:** MVC (Model-View-Controller) adapted to Django's MVT (Model-View-Template) logic.

## Architecture Flow (MVC/MVT)
1. **Model (Data Layer):** Database mapping via Django Models (e.g., `auth_user`, `profile`, `product`, `cartitem`, `order`).
2. **View (Controller Logic):** Python functions that process user requests, handle authentication, interact with models, and prepare context.
3. **Template (UI Layer):** Server-side rendered HTML sent back to the browser dynamically populated with data.

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Elijah19Github/quickshop.git
   cd quickshop
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On Mac/Linux:
   source venv/bin/activate
   ```

3. **Install Dependencies:**
   *(Ensure you have Python and Django installed)*
   ```bash
   pip install django
   # Alternatively if a requirements file exists: pip install -r requirements.txt
   ```

4. **Run Database Migrations:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Run the local Development Server:**
   ```bash
   python manage.py runserver
   ```
   Open `http://127.0.0.1:8000/` in your browser to view the app!

## Screenshots
*(Please add your project screenshots into the `screenshots/` folder, then link them here! Example format below:)*

`![Homepage Screenshot](screenshots/home.png)`

## Future Enhancements
- Integration with major payment gateways (e.g., Stripe or PayPal).
- Implementing user reviews, ratings, and advanced search filters.
- Transitioning the database from SQLite to PostgreSQL for production deployment.
- Enabling a REST API for future mobile app integration.
