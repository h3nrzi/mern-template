# MERN E-Commerce Template

A full-stack e-commerce application template built with MongoDB, Express.js, React, and Node.js. This template provides a solid foundation for building modern e-commerce applications with TypeScript support.

## 🚀 Features

- **Full-Stack TypeScript**: End-to-end type safety with TypeScript
- **Modern React Frontend**: Built with React 18, Vite, and TypeScript
- **RESTful API**: Express.js backend with MongoDB integration
- **Product Management**: Complete CRUD operations for products
- **Advanced Filtering**: Search, sort, pagination, and field limiting
- **Responsive Design**: Mobile-first approach with modern CSS
- **Persian Font Support**: Includes IRANSans font family
- **Data Seeding**: Built-in data seeder for development
- **Error Handling**: Centralized error handling with custom error classes
- **Development Tools**: Hot reload, linting, and formatting configured

## 🛠️ Tech Stack

### Backend

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **TypeScript** - Type safety
- **Pug** - Template engine
- **Morgan** - HTTP request logger
- **Bcrypt** - Password hashing

### Frontend

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **ESLint** - Code linting

### Development Tools

- **Nodemon** - Auto-restart server
- **Concurrently** - Run multiple commands
- **Prettier** - Code formatting
- **ts-node** - TypeScript execution

## 📦 Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd mern-template
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**

   ```bash
   cp .env.example .env
   ```

   Configure your environment variables:

   ```env
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/ecommerce
   NODE_ENV=development
   ```

4. **Start the development server**
   ```bash
   npm run start:dev
   ```

## 🚀 Available Scripts

### Root Level Scripts

- `npm run start:dev` - Start both backend and frontend in development mode
- `npm run server` - Start backend server with nodemon
- `npm run client` - Start frontend development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run data:import` - Import sample data
- `npm run data:destroy` - Remove all data

### Client Scripts

- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

## 📁 Project Structure

```
mern-template/
├── client/                 # React frontend
│   ├── public/            # Static assets
│   ├── src/               # Source code
│   │   ├── App.tsx        # Main App component
│   │   ├── main.tsx       # Entry point
│   │   └── ...
│   └── package.json       # Frontend dependencies
├── src/                   # Backend source code
│   ├── controllers/       # Route controllers
│   ├── data/             # Sample data and seeder
│   ├── middlewares/      # Custom middlewares
│   ├── models/           # Mongoose models
│   ├── routers/          # Route definitions
│   ├── start/            # App configuration
│   ├── types/            # TypeScript type definitions
│   ├── utils/            # Utility functions
│   ├── views/            # Pug templates
│   └── server.ts         # Server entry point
└── package.json          # Root dependencies
```

## 🔧 API Endpoints

### Products

- `GET /api/products` - Get all products with filtering, sorting, and pagination
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create new product
- `DELETE /api/products/:id` - Delete product

### Query Parameters

- `page` - Page number for pagination
- `limit` - Number of items per page
- `sort` - Sort by field (e.g., `price`, `-createdAt`)
- `fields` - Select specific fields
- `search` - Search in product names and descriptions

## 🎨 Frontend Features

- **Product Listing**: Display products with pagination
- **Type Safety**: Full TypeScript integration
- **Modern React**: Hooks and functional components
- **Responsive Design**: Mobile-first approach

## 🗄️ Database Schema

### Product Model

```typescript
{
  name: string;           // Product name
  slug: string;           // URL-friendly identifier
  description: string;    // Product description
  image: string;          // Main product image
  images: string[];       // Additional images
  countInStock: number;   // Inventory count
  isAvailable: boolean;   // Availability status
  brand: string;          // Product brand
  category: string;       // Product category
  rating: number;         // Average rating
  numReviews: number;     // Number of reviews
  price: number;          // Original price
  discount: number;       // Discount percentage
  discountedPrice: number; // Calculated discounted price
}
```

## 🔒 Environment Variables

Create a `.env` file in the root directory:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database
MONGODB_URI=mongodb://localhost:27017/ecommerce

# Add other environment variables as needed
```

## 🚀 Deployment

### Production Build

```bash
npm run build
```

### Start Production Server

```bash
npm start
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

**Hossein Rezaei**

## 🙏 Acknowledgments

- Built with modern web technologies
- Inspired by e-commerce best practices
- Persian language support included

---

**Happy Coding!** 🎉
