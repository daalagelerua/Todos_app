# Todos_app

## ✨ Features

### Core Functionality
- ✅ **Create, Read, Update, Delete** (CRUD) operations for todos
- 🔄 **Real-time synchronization** using Convex backend
- ✏️ **Inline editing** of todos with save/cancel options
- ✓ **Toggle completion status** with visual feedback
- 🗑️ **Delete confirmation** to prevent accidental deletions
- 📊 **Progress tracking** with visual progress bar

### User Interface
- 🎨 **Beautiful gradient designs** throughout the app
- 🌓 **Dark mode support** with theme persistence
- 📱 **Responsive layout** that works on all screen sizes
- ⚡ **Smooth animations** and transitions
- 🎯 **Intuitive user experience** with clear visual hierarchy

### Settings & Statistics
- 📈 **Statistics dashboard** showing:
  - Total todos count
  - Completed todos count
  - Active todos count
- ⚙️ **User preferences**:
  - Dark/Light mode toggle
  - Notifications toggle (UI ready)
  - Auto-sync toggle (UI ready)
- 🔴 **Danger zone** for resetting all data

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- A Convex account (free at [convex.dev](https://convex.dev))

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd Todos_app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up Convex**
   
   a. Create a new Convex project at [convex.dev](https://convex.dev)
   
   b. Get your deployment URL from the Convex dashboard
   
   c. Create a `.env` file in the root directory:
   ```env
   EXPO_PUBLIC_CONVEX_URL=https://your-deployment-url.convex.cloud
   ```

4. **Deploy Convex functions**
   ```bash
   npx convex dev
   ```

5. **Start the app**
   ```bash
   npx expo start
   ```

## 📱 Running the App

After starting the development server, you can run the app on:

- **iOS Simulator**: Press `i` in the terminal
- **Android Emulator**: Press `a` in the terminal
- **Physical Device**: Scan the QR code with the Expo Go app
- **Web Browser**: Press `w` in the terminal

## 🏗️ Project Structure

```
Todos_app/
├── app/                      # Main application code
│   ├── (tabs)/              # Tab-based navigation
│   │   ├── index.tsx        # Home screen (Todos list)
│   │   ├── settings.tsx     # Settings screen
│   │   └── _layout.tsx      # Tabs layout configuration
│   ├── components/          # Reusable components
│   │   ├── DangerZone.tsx   # Reset app component
│   │   ├── EmptyState.tsx   # Empty todos state
│   │   ├── Header.tsx       # Home screen header
│   │   ├── LoadingSpinner.tsx
│   │   ├── Preferences.tsx  # Settings preferences
│   │   ├── ProgressStats.tsx # Statistics display
│   │   └── TodoInput.tsx    # Todo creation input
│   └── _layout.tsx          # Root layout with providers
├── assets/
│   └── styles/             # Centralized styling
│       ├── home.styles.ts
│       └── settings.styles.ts
├── convex/                 # Backend functions
│   ├── schema.ts           # Database schema
│   ├── todos.ts            # Todo CRUD operations
│   └── _generated/         # Auto-generated types
├── hooks/
│   └── useTheme.tsx        # Theme management hook
└── package.json
```

## 🔧 Technologies Used

### Frontend
- **[React Native](https://reactnative.dev/)** - Mobile app framework
- **[Expo](https://expo.dev/)** - Development platform
- **[Expo Router](https://expo.github.io/router/)** - File-based routing
- **[TypeScript](https://www.typescriptlang.org/)** - Type safety

### Backend
- **[Convex](https://www.convex.dev/)** - Real-time backend platform
  - Real-time data synchronization
  - Type-safe queries and mutations
  - Automatic API generation

### UI Libraries
- **[Expo Linear Gradient](https://docs.expo.dev/versions/latest/sdk/linear-gradient/)** - Gradient effects
- **[Expo Vector Icons](https://docs.expo.dev/guides/icons/)** - Icon library
- **[React Native Safe Area Context](https://github.com/th3rdwave/react-native-safe-area-context)** - Safe area handling

### State Management
- **[AsyncStorage](https://react-native-async-storage.github.io/async-storage/)** - Local storage for preferences

## 🎨 Customization

### Changing Theme Colors

Edit the color schemes in `hooks/useTheme.tsx`:

```typescript
const lightColors: ColorScheme = {
  primary: "#3b82f6", // Change primary color
  success: "#10b981",
  // ... other colors
};

const darkColors: ColorScheme = {
  primary: "#60a5fa",
  // ... other colors
};
```

### Adding New Features

1. **Backend**: Add new functions in `convex/todos.ts`
2. **Frontend**: Create components in `app/components/`
3. **Styling**: Add styles in `assets/styles/`

## 📊 Convex Schema

The app uses a simple schema with one table:

```typescript
todos: {
  text: string,
  isCompleted: boolean,
}
```

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
EXPO_PUBLIC_CONVEX_URL=https://your-deployment.convex.cloud
```

## 🐛 Troubleshooting

### Common Issues

1. **"Cannot connect to Convex"**
   - Ensure your `EXPO_PUBLIC_CONVEX_URL` is correct
   - Check if `npx convex dev` is running

2. **"Module not found" errors**
   - Run `npm install` again
   - Clear Metro bundler cache: `npx expo start -c`

3. **Dark mode not persisting**
   - Check AsyncStorage permissions
   - Clear app data and try again

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [Expo Team](https://expo.dev/) for the amazing development platform
- [Convex](https://www.convex.dev/) for the powerful backend
- [Ionicons](https://ionic.io/ionicons) for the beautiful icons

## 📧 Contact

Aurèle Perillat - aurele284@gmail.com

Project Link: [https://github.com/daalagelerua/Todos_app/](https://github.com/daalagelerua/Todos_app/)

---

Made with ❤️ using React Native and Convex


