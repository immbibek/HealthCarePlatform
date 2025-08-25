# 🏥 Prescripto

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)](https://jwt.io/)
[![Stripe](https://img.shields.io/badge/Stripe-626CD9?style=for-the-badge&logo=Stripe&logoColor=white)](https://stripe.com/)
[![Razorpay](https://img.shields.io/badge/Razorpay-02042B?style=for-the-badge&logo=razorpay&logoColor=3395FF)](https://razorpay.com/)

> 📅 A comprehensive doctor appointment booking platform built with the MERN stack

Prescripto is a full-featured healthcare appointment management system that connects patients with healthcare providers. The platform offers a seamless experience for booking appointments, managing schedules, and maintaining medical records across multiple user roles.

---

## ✨ Features

### 👤 **Patient Features**
- 🔐 Secure user authentication and registration
- 🔍 Advanced doctor search by specialty, location, and availability
- 📅 Easy appointment booking with real-time availability
- 💳 Secure payment processing (Stripe & Razorpay)
- 📋 Comprehensive appointment history tracking
- 👨‍⚕️ Detailed doctor profiles and ratings
- ⚙️ Personal profile management and settings

### 👨‍⚕️ **Doctor Features**
- 🏥 Professional dashboard for appointment management
- ⏰ Flexible availability scheduling
- 📊 Patient appointment overview and history
- 👤 Professional profile customization
- 📈 Appointment analytics and insights
- 💰 Payment and earnings tracking

### 🛡️ **Admin Features**
- 🎛️ Comprehensive admin panel
- 👥 User and doctor account management
- 📊 Platform analytics and reporting
- 🔧 System configuration and maintenance
- 📋 Appointment oversight and management
- 💳 Payment gateway management

---

## 📸 Screenshots

### **Homepage**
![Homepage](assets/Homepage.png)
*Clean and intuitive homepage with doctor search functionality*

### **DoctorPage**
![Doctor Page](assets/DoctorPage.png)
*Streamlined appointment booking process*

### **Booking Panel**
![Booking](assets/Booking.png)
![Booking](assets/DoctorBooking.png)
*Comprehensive patient dashboard with appointment management*

### **Doctor Admin**
![Doctor Admin](assets/doctorAdmin.png)
*Detailed doctor profiles with ratings and availability*

### **User Profile**
![User Profile](assets/Userprofile.png)
*Streamlined appointment booking process*

---

## 🛠️ Tech Stack

### **Frontend**
- ⚛️ **React.js** - Modern JavaScript library for building user interfaces
- 🎨 **Tailwind CSS** - Utility-first CSS framework for rapid UI development
- 🧭 **React Router** - Declarative routing for React applications
- 🌐 **Axios** - Promise-based HTTP client for API requests
- ⚡ **Vite** - Fast build tool and development server

### **Backend**
- 🟢 **Node.js** - JavaScript runtime environment
- 🚀 **Express.js** - Fast, unopinionated web framework for Node.js
- 🍃 **MongoDB** - NoSQL database for flexible data storage
- 🔒 **JWT** - JSON Web Tokens for secure authentication
- 🛡️ **bcrypt** - Password hashing library for enhanced security
- 💳 **Stripe** - International payment processing
- 💰 **Razorpay** - Indian payment gateway integration

---

## 🚀 Installation & Setup

### **Prerequisites**
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- Git
- Stripe Account (for payment processing)
- Razorpay Account (for Indian payments)

### **1. Clone the Repository**
```bash
git clone https://github.com/immbibek/Healthcareplatform.git
cd prescripto
```

### **2. Backend Setup**
```bash
# Navigate to server directory
cd server

# Install dependencies
npm install

# Create .env file
touch .env
```

**Configure your `.env` file:**
```env
# Database
MONGODB_URI=mongodb://localhost:27017/prescripto
# or use MongoDB Atlas: mongodb+srv://username:password@cluster.mongodb.net/prescripto

# JWT Secret
JWT_SECRET=your_super_secret_jwt_key_here

# Server Configuration
PORT=5000
NODE_ENV=development

# Cloudinary Configuration (for image uploads)
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name

# Payment Gateway Configuration
# Stripe Configuration
STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_publishable_key
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key

# Razorpay Configuration
RAZORPAY_KEY_ID=rzp_test_your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
```

**Start the backend server:**
```bash
npm run dev
# Server will run on http://localhost:5000
```

### **3. Frontend Setup**
```bash
# Navigate to client directory
cd ../client

# Install dependencies
npm install

# Create .env file for frontend (if needed)
touch .env
```

**Configure your frontend `.env` file:**
```env
VITE_API_URL=http://localhost:5000/api

# Payment Gateway Public Keys
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_publishable_key
VITE_RAZORPAY_KEY_ID=rzp_test_your_razorpay_key_id
```

**Start the frontend development server:**
```bash
npm run dev
# Client will run on http://localhost:3000
```

### **4. Database Setup**
Make sure MongoDB is running on your system or you have a valid MongoDB Atlas connection string configured in your backend `.env` file.

### **5. Payment Gateway Setup**

#### **Stripe Setup:**
1. Create a Stripe account at [stripe.com](https://stripe.com)
2. Get your API keys from the Stripe Dashboard
3. Add the keys to your `.env` files

#### **Razorpay Setup:**
1. Create a Razorpay account at [razorpay.com](https://razorpay.com)
2. Get your Key ID and Secret from the Razorpay Dashboard
3. Add the keys to your `.env` files

---

## 📁 Folder Structure

```
prescripto/
├── 📁 client/                    # Frontend React application
│   ├── 📁 public/               # Static assets
│   ├── 📁 src/
│   │   ├── 📁 components/       # Reusable React components
│   │   ├── 📁 pages/           # Page components
│   │   ├── 📁 context/         # React context providers
│   │   ├── 📁 utils/           # Utility functions
│   │   ├── 📁 hooks/           # Custom React hooks
│   │   ├── 📁 assets/          # Images, icons, etc.
│   │   └── 📄 App.jsx          # Main App component
│   ├── 📄 package.json
│   ├── 📄 vite.config.js
│   └── 📄 tailwind.config.js
├── 📁 server/                   # Backend Node.js application
│   ├── 📁 controllers/         # Route controllers
│   ├── 📁 models/              # MongoDB models
│   ├── 📁 routes/              # API routes
│   ├── 📁 middleware/          # Custom middleware
│   ├── 📁 utils/               # Utility functions
│   ├── 📁 config/              # Database and other configurations
│   ├── 📄 server.js            # Main server file
│   └── 📄 package.json
├── 📄 README.md
└── 📄 .gitignore
```

---

## 💡 Usage

### **For Patients**

1. **Registration & Login** 🔐
   - Visit the homepage and click "Sign Up"
   - Fill in your personal details
   - Verify your email address
   - Login with your credentials

2. **Booking an Appointment** 📅
   - Use the search functionality to find doctors
   - Filter by specialty, location, or availability
   - Select your preferred doctor and time slot
   - Choose payment method (Stripe or Razorpay)
   - Complete secure payment processing
   - Receive confirmation notification and receipt

3. **Managing Appointments** 📋
   - View upcoming appointments in your dashboard
   - Access your appointment history
   - Download payment receipts and invoices
   - Reschedule or cancel appointments if needed
   - Track payment status and refunds

### **For Doctors**

1. **Profile Setup** 👨‍⚕️
   - Complete your professional profile
   - Upload credentials and certifications
   - Set your specialties and services
   - Configure consultation fees

2. **Managing Schedule** ⏰
   - Set your available time slots
   - Block unavailable dates
   - Configure appointment duration
   - Set recurring availability patterns

3. **Appointment Management** 📊
   - View daily/weekly appointment schedule
   - Access patient information
   - Update appointment status
   - Generate reports and analytics
   - Track earnings and payments

### **For Administrators**

1. **User Management** 👥
   - Monitor user registrations
   - Manage user accounts and permissions
   - Handle user complaints and issues
   - Generate user analytics reports

2. **Doctor Verification** ✅
   - Review doctor applications
   - Verify medical credentials
   - Approve or reject doctor profiles
   - Monitor doctor performance

3. **Platform Management** 🎛️
   - Monitor system health and performance
   - Configure platform settings
   - Manage payment gateway settings (Stripe & Razorpay)
   - Handle payment disputes and refunds
   - Generate financial and transaction reports
   - Monitor payment analytics and trends

---

## 💳 Payment Integration

### **Supported Payment Methods**

#### **Stripe (International)**
- Credit/Debit Cards (Visa, Mastercard, American Express)
- Digital Wallets (Apple Pay, Google Pay)
- Bank Transfers (ACH, SEPA)
- Multiple Currency Support

#### **Razorpay (India)**
- Credit/Debit Cards
- Net Banking
- UPI (Unified Payments Interface)
- Digital Wallets (Paytm, PhonePe, Google Pay)
- EMI Options

### **Payment Flow**
1. Patient selects doctor and time slot
2. System calculates total fee
3. Patient chooses payment method
4. Secure payment processing
5. Payment confirmation and receipt
6. Appointment confirmed
7. Email/SMS notifications sent

---

## 🤝 Contributing

We welcome contributions to improve Prescripto! Here's how you can help:

### **Getting Started**
1. **Fork** the repository
2. **Clone** your fork locally
3. **Create** a new branch for your feature
4. **Make** your changes
5. **Test** thoroughly
6. **Submit** a pull request

### **Development Guidelines**
- Follow existing code style and conventions
- Write clear, descriptive commit messages
- Include tests for new features
- Update documentation as needed
- Ensure your code passes all existing tests

### **Code Style**
- Use consistent indentation (2 spaces)
- Follow React best practices
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions small and focused

### **Pull Request Process**
1. Update the README.md with details of changes if needed
2. Increase version numbers following [Semantic Versioning](https://semver.org/)
3. Ensure all status checks pass
4. Request review from maintainers

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Prescripto

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contact & Support

- 📧 **Email**: bibekchy2022@gmail.com
- 🐛 **Issues**: [GitHub Issues](https://github.com/immbibek/Healthcareplatform/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/immbibek/Healthcareplatform/discussions)
- 📚 **Documentation**: [Wiki](https://github.com/immbibek/Healthcareplatform/wiki)

---

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape Prescripto
- Special appreciation to the open-source community
- Inspired by modern healthcare digital transformation needs

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ and ☕ by [Bibek Chaudhary]

![Prescripto](https://img.shields.io/badge/Prescripto-Healthcare%20Platform-blue?style=for-the-badge)

</div>
