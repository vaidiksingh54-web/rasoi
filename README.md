# 🍲 Bharat Rasoi (भारत रसोई) — Authentic Indian Culinary & AI Kitchen Platform

> **An intelligent, regional Indian recipe explorer, daily meal planner, and AI Chef powered by Google Gemini.**

[![React](https://img.shields.io/badge/React-19.0-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-8.x-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4.0-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini_AI-2.x-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 🌟 Overview

**Bharat Rasoi** is a full-featured culinary platform dedicated to celebrating the rich diversity of traditional and modern Indian home cooking. From fragrant Biryanis of Hyderabad to crispy Dosas of Tamil Nadu, tangy Machher Jhol of Bengal, and earthy Dal Baati Churma of Rajasthan, Bharat Rasoi pairs authentic cultural heritage with modern artificial intelligence.

With an integrated **AI Chef** powered by Google's Gemini API, dynamic meal planning algorithms, ingredient-based dish discovery, and categorized grocery automation, Bharat Rasoi transforms everyday kitchen cooking into an inspiring, effortless experience.

---

## ✨ Key Features

### 🤖 1. AI Chef Companion (Powered by Google Gemini)
- **Interactive Culinary Assistant**: Ask real-time questions about cooking techniques, substitutions, spice balancing, or tips to rescue an over-salted curry.
- **Smart Dietary Customization**: Get customized dish recommendations based on dietary constraints (Jain, Gluten-Free, Vegan, High-Protein, Diabetic-Friendly).

### 🍛 2. Pan-Indian Regional Recipe Directory
- **Authentic Regional Cuisines**: Explore hand-curated recipes spanning **North, South, East, West, Central, and North-East India**.
- **Comprehensive Cooking Metrics**: Prep time, cook time, difficulty level, spice level rating, calories, and complete macronutrient breakdowns.
- **Step-by-Step Guided Cooking**: Detailed preparation stages with integrated step timers and chef notes.

### 🍱 3. Daily Meal Recommendation Engine
- **Automated Daily Menus**: Fresh daily recommendations across **Breakfast, Lunch, Evening Snacks, and Dinner**.
- **Preference Signatures**: Adapts automatically to your household diet, preferred spice tolerances, and regional favorites.
- **Instant Slot Swaps**: Swap any meal recommendation with alternative matching recipes in one click.

### 🥕 4. "What's in My Fridge?" Ingredient Finder
- Select ingredients available in your pantry, and the intelligent matching engine discovers recipes you can cook immediately without an emergency grocery run.

### 📅 5. Weekly Meal Planner & Kitchen Tools
- **7-Day Meal Scheduler**: Plan meals for every day of the week to save time and reduce food waste.
- **Automated Smart Grocery List**: Aggregates ingredients across your planned meals, groups them by aisle categories (Produce, Spices, Dairy, Grains), and tracks checklist progress.
- **Dynamic Servings Scaler**: Scale recipes from a single portion to a family feast with automatic mathematical ingredient recalculation.

### 📚 6. Masterclasses & Masala Blends Guide
- Traditional spice-blending recipes (Garam Masala, Sambhar Podi, Panch Phoron, Rasam Powder).
- Fundamental Indian culinary techniques: *Tadka/Chhonk* (tempering), *Bhunao* (roasting paste), *Dum* (slow steam cooking).

---

## 🛠️ Tech Stack & Architecture

| Layer | Technologies |
|---|---|
| **Frontend** | React 19, TypeScript, Vite 8 |
| **Styling** | Tailwind CSS v4, Custom Design Tokens |
| **Animation** | Motion (`motion/react` / Framer Motion) |
| **Icons** | Lucide React |
| **AI / LLM** | Google Gemini API (`@google/genai`) |
| **Backend & Server** | Express.js, TypeScript Execution (`tsx`) |
| **State Management** | React State Hooks + Local Storage Persistence with sync |

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [Bun](https://bun.sh/) or [npm](https://www.npmjs.com/) / [pnpm](https://pnpm.io/)
- Google Gemini API Key (get one free at [Google AI Studio](https://aistudio.google.com/))

### 1. Clone the Repository
```bash
git clone https://github.com/vaidiksingh54-web/rasoi.git
cd rasoi
```

### 2. Install Dependencies
```bash
# Using bun (recommended)
bun install

# Or using npm
npm install
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory (or copy from `.env.example`):
```env
GEMINI_API_KEY=your_gemini_api_key_here
PORT=3000
```

### 4. Run Development Server
```bash
# Using bun
bun run dev

# Or using npm
npm run dev
```

Open your browser and navigate to:
```
http://localhost:3000
```

---

## 📁 Project Structure

```
rasoi/
├── public/                 # Static assets & screenshots
├── src/
│   ├── components/         # Reusable UI components (Header, Sidebar, RecipeCard, DishVisual, Footer)
│   ├── data/               # Regional recipe database & seed datasets
│   ├── pages/              # View screens
│   │   ├── HomePage.tsx            # Hero showcase, trending recipes & regional filters
│   │   ├── ExploreRecipesPage.tsx  # Multi-faceted search & filtering
│   │   ├── TodaysFoodPage.tsx      # Daily 4-meal recommendation board
│   │   ├── RecipeDetailsPage.tsx   # Step-by-step instructions, timers & scaling
│   │   ├── AIChefPage.tsx          # Google Gemini-powered cooking assistant
│   │   ├── IngredientFinderPage.tsx# Pantry ingredient matching engine
│   │   ├── KitchenToolsPages.tsx   # Meal planner & shopping list
│   │   ├── LearnCookingPage.tsx    # Spices & techniques masterclass
│   │   ├── FavouritesPage.tsx      # Bookmarked dishes
│   │   ├── ProfilePage.tsx         # User taste preferences & diet goals
│   │   └── AccountAndAuthPages.tsx # Authentication & settings
│   ├── utils/              # Recommendation algorithm & ingredient math
│   ├── types.ts            # TypeScript interfaces & domain types
│   ├── App.tsx             # Master application state router
│   ├── main.tsx            # React application root
│   └── index.css           # Tailwind CSS directives
├── server.ts               # Express backend & Vite dev middleware
├── vite.config.ts          # Vite configuration with Tailwind v4 & React plugin
├── tsconfig.json           # TypeScript configuration
└── package.json            # Scripts & project dependencies
```

---

## 🎯 Target Audience & Use Cases
- **Home Cooks & Students**: Easy everyday meal planning with minimal ingredient wastage.
- **Culinary Enthusiasts**: Mastering regional Indian flavors and traditional cooking methods.
- **Health-Conscious Individuals**: Tracking dietary requirements, protein intake, and calorie counts for Indian dishes.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

<p align="center">
  Made with 🧡 for the love of authentic Indian cuisine
</p>
