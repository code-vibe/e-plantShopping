# e-plantShopping

A modern, interactive e-commerce plant shopping application built with React, Redux, and Vite. Browse, add plants to your cart, and manage your shopping experience with real-time state management.

## 🌿 Features

- **Product Catalog**: Browse five categories of plants:
  - Air Purifying Plants
  - Aromatic Fragrant Plants
  - Insect Repellent Plants
  - Medicinal Plants
  - Low Maintenance Plants

- **Shopping Cart**: 
  - Add items to cart with single click
  - View real-time cart quantity badge
  - Increment/decrement item quantities
  - Remove items from cart
  - Calculate item subtotals and total cart cost

- **Global State Management**: Redux Toolkit for centralized cart state
- **Real-time Updates**: UI updates instantly when cart changes
- **Responsive Design**: Modern, user-friendly interface

## 🛠️ Tech Stack

- **Frontend**: React 18.2.0
- **State Management**: Redux Toolkit 2.2.3 & React-Redux 9.1.1
- **Build Tool**: Vite 5.2.0
- **Styling**: CSS
- **Deployment**: GitHub Pages

## 📋 Project Structure

```
e-plantShopping/
├── src/
│   ├── components/
│   │   ├── ProductList.jsx       # Plant product listing & cart icon
│   │   ├── CartItem.jsx          # Cart management & checkout
│   │   ├── App.jsx               # Main app component
│   │   └── AboutUs.jsx           # About page
│   ├── CartSlice.jsx             # Redux slice for cart state
│   ├── store.js                  # Redux store configuration
│   ├── main.jsx                  # Entry point with Provider
│   ├── index.css                 # Global styles
│   └── assets/                   # Images & static files
├── public/                       # Static assets
├── vite.config.js                # Vite configuration
├── package.json                  # Dependencies & scripts
└── README.md                     # This file
```

## 🚀 Getting Started

### Installation

```bash
# Clone the repository
git clone https://github.com/code-vibe/e-plantShopping.git
cd e-plantShopping

# Install dependencies
npm install
```

### Development

```bash
# Start development server
npm run dev

# Open browser at http://localhost:5173
```

### Build

```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

## 📦 Redux Architecture

### Store Structure
```javascript
{
  cart: {
    items: [
      { name, image, cost, quantity }
    ]
  }
}
```

### Actions
- `addItem(product)` - Add item or increment quantity
- `removeItem(name)` - Remove item from cart
- `updateQuantity({ name, quantity })` - Update item quantity

## 🎨 Key Components

### ProductList.jsx
- Displays all plant categories and products
- Maps over plant array to render cards
- Handles add-to-cart functionality
- Shows cart quantity badge in navbar
- Manages local state for "Added to Cart" button states

### CartItem.jsx
- Displays cart items with images and details
- Increment/decrement quantity buttons
- Delete item button
- Calculates item subtotals and total cart amount
- Continue Shopping and Checkout buttons

### CartSlice.jsx
- Redux reducer for cart state management
- Three reducer functions: addItem, removeItem, updateQuantity
- Handles duplicate item detection (increments quantity vs. adds new)

## 💳 Shopping Flow

1. **Browse Products** - View plants organized by category
2. **Add to Cart** - Click "Add to Cart" button on any plant
3. **View Cart** - Click cart icon to see all items
4. **Manage Quantities** - Use +/- buttons to adjust quantities
5. **Remove Items** - Delete button removes item completely
6. **Checkout** - Placeholder for future implementation

## 🌐 Deployment

### Deploy to GitHub Pages

```bash
# Build and deploy to gh-pages branch
npm run deploy
```

The app will be live at: `https://code-vibe.github.io/e-plantShopping/`

### Configuration
- `vite.config.js` includes `base: "/shoppingreact"` for correct routing
- `package.json` includes predeploy and deploy scripts
- GitHub Pages builds from `gh-pages` branch

## 📝 Tasks Completed

- ✅ **Task 1**: Product listing with map() and Add to Cart functionality
- ✅ **Task 2**: Redux reducer functions (addItem, removeItem, updateQuantity)
- ✅ **Task 3**: Cart item management and calculations
- ✅ **Task 4**: Redux integration in ProductList & CartItem
- ✅ **Task 5**: Product page styling and functionality
- ✅ **Task 6**: Global Redux store setup and GitHub Pages deployment

## 🔧 Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run deploy       # Deploy to GitHub Pages
npm run lint         # Run ESLint
```

## 📄 License

This project is part of a coding curriculum and is open for educational purposes.

## 👨‍💻 Author

**code-vibe** - Repository Owner

---

**Paradise Nursery** - Where Green Meets Serenity 🌱