# Mahadev Baby Shop - Premium E-commerce Platform




> **🌐 Live Demo:** [https://mahadev-baby-shop.vercel.app/](https://mahadev-baby-shop.vercel.app/)



A modern, full-stack e-commerce platform built with **Next.js 15**, **TypeScript**, and **MongoDB**, specifically designed for premium baby care products and accessories. Features a beautiful animated UI, comprehensive authentication system, and complete order management.

## Key Features

### **Premium UI/UX Experience**

- **Animated Background**: Floating baby-themed icons with smooth CSS animations
- **Gradient Design**: Beautiful pink, purple, and blue gradient themes throughout
- **Dark/Light Mode**: Complete theme switching with system preference detection
- **Mobile-First**: Fully responsive design optimized for all device sizes
- **Premium Components**: Custom shadcn/ui components with enhanced styling


### **Advanced Authentication System**

- **Multi-step Registration**: Email verification with secure OTP system
- **Real-time Validation**: Instant field validation with backend checks
- **Password Recovery**: Complete forgot password flow with OTP verification
- **Admin Detection**: Automatic admin privileges based on email configuration
- **Secure Sessions**: JWT-based authentication with HTTP-only encrypted cookies


### ️ **Complete E-commerce Solution**

- **Product Catalog**: Multi-category products (Clothes, Toys, Bath Items, Newborn)
- **Smart Shopping Cart**: Persistent cart with real-time stock validation
- **Order Management**: Complete order lifecycle from placement to delivery
- **Invoice Generation**: Professional PDF invoices for completed orders
- **Inventory Tracking**: Real-time stock management and availability


### ‍ **Comprehensive Admin Panel**

- **Order Processing**: Accept, dispatch, and complete orders with status tracking
- **Product Management**: CRUD operations for all product categories
- **Customer Management**: View customer details and order history
- **Analytics Dashboard**: Sales reports and business insights
- **Bulk Operations**: Mass order processing and inventory updates


### **Smart Location System**

- **Dynamic Address Selection**: Complete India address hierarchy (State → District → Sub-district → Village)
- **Pincode Validation**: 6-digit pincode validation with area detection
- **Delivery Zones**: Zone-based delivery charges and free delivery areas
- **Location Autocomplete**: Smart address suggestions and validation


## Tech Stack

### **Frontend**

- **Next.js 15** - React framework with App Router and Server Components
- **TypeScript** - Type-safe development with strict mode
- **Tailwind CSS** - Utility-first CSS framework with custom design system
- **shadcn/ui** - High-quality, accessible UI component library
- **Lucide React** - Beautiful, customizable icon library
- **Framer Motion** - Smooth animations and micro-interactions


### **Backend**

- **Next.js API Routes** - Serverless API endpoints with middleware
- **MongoDB** - NoSQL database with Mongoose ODM
- **JWT Authentication** - Secure token-based authentication
- **Nodemailer** - Email services for OTP and notifications
- **PDFKit** - Professional PDF generation for invoices
- **Zod** - Runtime type validation and schema parsing


### **Development Tools**

- **ESLint** - Code linting with TypeScript rules
- **Prettier** - Code formatting and style consistency
- **Husky** - Git hooks for code quality
- **TypeScript** - Static type checking


## Quick Start

### **Prerequisites**

- Node.js 18+
- MongoDB database (local or Atlas)
- Gmail account for email services




### **2. Environment Setup**

Create `.env.local` in the root directory:

```plaintext
# Database
MONGODB_URI=mongodb://localhost:27017/mahadev-baby-shop
# or MongoDB Atlas: mongodb+srv://username:password@cluster.mongodb.net/mahadev-baby-shop

# Authentication (generate with: node -e "console.log(require('crypto').randomBytes(32).toString('hex'))")
AUTH_SECRET=your-super-secret-key-here-minimum-32-characters
JWT_SECRET=your-super-secret-key-here-minimum-32-characters

# Admin Configuration
ADMIN_EMAIL=

# Email Configuration (Gmail App Password)
EMAIL_USER=your-gmail@gmail.com
EMAIL_PASS=your-app-specific-password

# Application URL
NEXT_PUBLIC_APP_URL=
```


## ️ Project Architecture

```plaintext
mahadev-baby-shop/
├── app/                          # Next.js 15 App Router
│   ├── admin/                    # Admin dashboard pages
│   │   ├── orders/              # Order management interface
│   │   ├── products/            # Product management (CRUD)
│   │   └── dashboard/           # Analytics and overview
│   ├── api/                     # API routes and endpoints
│   │   ├── auth/                # Authentication endpoints
│   │   ├── orders/              # Order management API
│   │   ├── products/            # Product CRUD API
│   │   └── admin/               # Admin-specific endpoints
│   ├── auth/                    # Authentication pages
│   │   ├── login/               # Login page
│   │   ├── signup/              # Registration page
│   │   └── forgot-password/     # Password recovery
│   ├── checkout/                # Multi-step checkout process
│   ├── products/                # Product catalog pages
│   │   ├── clothes/             # Baby clothes category
│   │   ├── toys/                # Toys category
│   │   ├── bath/                # Bath products category
│   │   └── newborn/             # Newborn essentials
│   ├── orders/                  # Order tracking and history
│   ├── cart/                    # Shopping cart page
│   └── globals.css              # Global styles and CSS variables
├── components/                   # Reusable React components
│   ├── ui/                      # shadcn/ui component library
│   ├── animated-background.tsx  # Floating icons animation
│   ├── header.tsx               # Navigation with cart/auth
│   ├── footer.tsx               # Site footer with dark mode
│   ├── hero.tsx                 # Homepage hero section
│   ├── featured-products.tsx    # Product showcase
│   ├── location-selector.tsx    # Address selection component
│   └── conditional-header.tsx   # Context-aware navigation
├── contexts/                     # React Context providers
│   └── auth-provider.tsx        # Authentication state management
├── lib/                         # Utility libraries and configurations
│   ├── models/                  # MongoDB/Mongoose schemas
│   │   ├── user.ts             # User model with authentication
│   │   ├── order.ts            # Order model with status tracking
│   │   ├── clothes.ts          # Clothes product model
│   │   ├── toys.ts             # Toys product model
│   │   ├── bath.ts             # Bath products model
│   │   └── newborn.ts          # Newborn products model
│   ├── validations/             # Zod validation schemas
│   ├── verification/            # OTP and email verification
│   ├── auth.ts                  # Authentication utilities
│   ├── mongodb.ts               # Database connection
│   └── utils.ts                 # General utility functions
├── hooks/                       # Custom React hooks
│   ├── use-auth.ts             # Authentication hook
│   ├── use-cart.ts             # Shopping cart management
│   └── use-mobile.ts           # Mobile device detection
└── public/                      # Static assets and images
```

## Core Features Deep Dive

### **Authentication System**

- **Registration Flow**: Multi-step process with email verification
- **Login Security**: Rate limiting and secure session management
- **Password Recovery**: OTP-based reset with email verification
- **Admin Access**: Automatic admin detection based on email configuration
- **Session Management**: JWT tokens with automatic refresh and secure storage
- 🔄 Customer review and rating system


### **Product Management**

- **Multi-Category Support**: Clothes, Toys, Bath Products, Newborn Items
- **Advanced Schemas**: Size variants, age groups, weight specifications
- **Image Management**: Multiple product images with optimization
- **Inventory Tracking**: Real-time stock management and availability
- **Search & Filter**: Advanced product filtering and search capabilities


### **Order Processing**

- **Complete Lifecycle**: Pending → Accepted → Dispatched → Completed
- **Status Tracking**: Real-time updates with email notifications
- **Invoice Generation**: Professional PDF invoices with branding
- **Delivery Management**: Zone-based charges and tracking integration
- **Customer Communication**: Automated status update emails


### **Admin Dashboard**

- **Order Management**: Bulk operations and status updates
- **Analytics**: Sales reports, inventory insights, customer analytics
- **Product CRUD**: Complete product management interface
- **Customer Management**: Order history and customer insights
- **Report Generation**: PDF reports with custom date ranges


## Design System

### **Color Palette**

- **Primary**: Pink to Purple gradient (`from-pink-500 to-purple-500`)
- **Secondary**: Purple to Blue gradient (`from-purple-500 to-blue-500`)
- **Accent**: Rose to Pink gradient (`from-rose-500 to-pink-500`)
- **Neutral**: Gray scale with dark mode support


### **Typography**

- **Font**: Inter (Google Fonts) for clean, modern readability
- **Hierarchy**: Consistent heading sizes and spacing
- **Responsive**: Fluid typography that scales with screen size


### **Components**

- **Cards**: Elevated cards with subtle shadows and hover effects
- **Buttons**: Gradient backgrounds with smooth hover transitions
- **Forms**: Clean inputs with real-time validation feedback
- **Navigation**: Sticky header with mobile-responsive menu


## Mobile Optimization

### **Responsive Design**

- **Breakpoints**: Mobile (320px+), Tablet (768px+), Desktop (1024px+)
- **Touch-Friendly**: 44px minimum touch targets
- **Performance**: Optimized images and lazy loading
- **Navigation**: Mobile-first navigation with slide-out menu


### **Progressive Web App (PWA) Ready**

- **Service Worker**: Offline functionality (optional)
- **App Manifest**: Install as native app
- **Push Notifications**: Order updates and promotions


## Security & Performance

### **Security Features**

- **Password Hashing**: bcrypt with salt rounds
- **JWT Security**: HTTP-only cookies with expiration
- **Input Validation**: Zod schema validation on all inputs
- **CSRF Protection**: Built-in Next.js protection
- **Rate Limiting**: API endpoint protection


### **Performance Optimization**


- **Image Optimization**: Next.js automatic optimization
- **Code Splitting**: Route-based and component-based splitting
- **Caching**: Static generation and API response caching
- **Bundle Analysis**: Optimized bundle size


## Deployment

### **Vercel (Recommended)**

1. **Connect Repository**: Link your GitHub repository to Vercel
2. **Environment Variables**: Add all environment variables in Vercel dashboard
3. **Domain Setup**: Configure custom domain (optional)
4. **Automatic Deployments**: Push to main branch for automatic deployment


### **Production Environment Variables**

```plaintext
MONGODB_URI=your-production-mongodb-atlas-uri
AUTH_SECRET=your-production-secret-32-chars
JWT_SECRET=your-production-secret-32-chars
ADMIN_EMAIL=admin@yourdomain.com
EMAIL_USER=your-production-email@gmail.com
EMAIL_PASS=your-production-app-password
NEXT_PUBLIC_APP_URL=https://yourdomain.com
```

### **MongoDB Atlas Setup**

1. Create MongoDB Atlas account
2. Create new cluster (free tier available)
3. Add database user with read/write permissions
4. Configure network access (allow all IPs for Vercel)
5. Get connection string and add to environment variables


## Business Features

### **Mahadev Baby Shop Details**

- **Location**: Vithalani Complex, Mangrol, Gujarat, India
- **Owner**: Divyesh Nanadaniya

## ️ Development

### **Available Scripts**

```shellscript
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # TypeScript type checking
```

### **Code Quality**

- **ESLint**: Configured with TypeScript and React rules
- **Prettier**: Code formatting with consistent style
- **TypeScript**: Strict mode with comprehensive type checking
- **Git Hooks**: Pre-commit hooks for code quality


### **Testing (Future Enhancement)**

```shellscript
npm run test         # Run unit tests
npm run test:e2e     # Run end-to-end tests
npm run test:watch   # Run tests in watch mode
```

## Contributing

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit your changes**: `git commit -m 'Add amazing feature'`
4. **Push to the branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**


### **Development Guidelines**

- Follow TypeScript and ESLint rules
- Use functional components with hooks
- Follow the existing code structure and naming conventions
- Add proper TypeScript types for all new code
- Test your changes thoroughly before submitting


## Roadmap

### **Current Version (v1.0)**

- ✅ Complete authentication system with OTP verification
- ✅ Premium UI with animations and dark mode
- ✅ Mobile-responsive design
- ✅ Product catalog with multiple categories
- ✅ Shopping cart and order management
- ✅ Admin dashboard with order processing
- ✅ Location-based delivery system
- ✅ Professional invoice generation



## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **[Next.js Team](https://nextjs.org/)** - For the incredible React framework
- **[Vercel](https://vercel.com/)** - For seamless deployment and hosting
- **[shadcn/ui](https://ui.shadcn.com/)** - For beautiful, accessible UI components
- **[Tailwind CSS](https://tailwindcss.com/)** - For the utility-first CSS framework
- **[MongoDB](https://www.mongodb.com/)** - For the flexible database solution
- **[Lucide](https://lucide.dev/)** - For the beautiful icon library


## Support & Contact

### **Technical Support**

- **Email**: [mahadevbabyshop5@gmail.com](mailto:mahadevbabyshop5@gmail.com)
- **GitHub Issues**: [Create an issue](https://github.com/yourusername/mahadev-baby-shop/issues)


### **Business Inquiries**

- **Phone**: +91 99137 37023, +91 98988 93380
- **WhatsApp**: [Chat with us](https://wa.me/919913737023)
- **Email**: [mahadevbabyshop5@gmail.com](mailto:mahadevbabyshop5@gmail.com)
- **Address**: Vithalani Complex, Mangrol, Gujarat, India


### **Social Media**

- **Instagram**: [@mahadev_baby_shop](https://www.instagram.com/mahadev_baby_shop?igsh=eDlna2prOTVkNW5z)
- **Website**: [https://mahadev-baby-shop.vercel.app/](https://mahadev-baby-shop.vercel.app/)


---



**🌐 [Visit Live Site](https://mahadev-baby-shop.vercel.app/)**
