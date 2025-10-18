# 🎬 Movie Browsing App

A modern mobile application for exploring popular and trending movies and TV shows. Built with Expo and React Native, this app provides users with a seamless experience to discover, browse, and save their favorite content.

## ✨ Features

- **Browse Movies & Shows**: Explore popular and trending movies and TV shows
- **User Authentication**: Secure sign-up and login functionality
- **Personalized Favorites**: Save and manage your favorite movies and shows in a dedicated "Saved" page
- **Real-time Content**: Always up-to-date content powered by TMDB API
- **Responsive Design**: Smooth and intuitive mobile experience with gesture support

## 🛠️ Tech Stack

- **Framework**: Expo ~54.0.13
- **Frontend**: React Native 0.81.4 with React 19.1.0
- **Styling**: NativeWind (Tailwind CSS for React Native)
- **Navigation**: Expo Router ~6.0.11 with React Navigation
- **Backend**: Appwrite
- **API**: The Movie Database (TMDB) API
- **Authentication**: Appwrite Auth
- **Animations**: React Native Reanimated

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v18 or higher)
- npm or yarn
- Expo CLI (`npm install -g expo-cli`)
- Expo Go app on your mobile device (for testing)
- Appwrite instance (self-hosted or cloud)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/movies-react-native.git
cd movies-react-native
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory and add the following:

```env
EXPO_PUBLIC_TMDB_API_KEY=your_tmdb_api_key
EXPO_PUBLIC_APPWRITE_ENDPOINT=your_appwrite_endpoint
EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_appwrite_project_id
EXPO_PUBLIC_APPWRITE_DATABASE_ID=your_database_id
EXPO_PUBLIC_APPWRITE_COLLECTION_ID=your_collection_id
```

> **Note**: Expo requires environment variables to be prefixed with `EXPO_PUBLIC_` to be accessible in your app.

### 4. Configure TMDB API

1. Visit [The Movie Database](https://www.themoviedb.org/)
2. Create an account and request an API key
3. Add your API key to the `.env` file

### 5. Configure Appwrite

1. Set up an Appwrite instance (cloud or self-hosted)
2. Create a new project
3. Set up authentication (Email/Password)
4. Create a database and collection for saved movies with the following attributes:
   - `userId` (string)
   - `movieId` (string)
   - `title` (string)
   - `posterPath` (string)
   - `savedAt` (datetime)
5. Add your Appwrite credentials to the `.env` file

### 6. Run the Application

Start the development server:

```bash
npm start
# or
expo start
```

Run on specific platforms:

```bash
# For iOS
npm run ios

# For Android
npm run android

# For Web
npm run web
```

Or scan the QR code with the Expo Go app on your mobile device.

## 📱 App Structure

```
movies-react-native/
├── app/                  # Expo Router app directory
│   ├── (tabs)/          # Tab-based navigation
│   │   ├── index.tsx    # Home screen
│   │   ├── saved.tsx    # Saved movies screen
│   │   └── _layout.tsx  # Tab layout
│   ├── auth/            # Authentication screens
│   │   ├── login.tsx
│   │   └── signup.tsx
│   ├── movie/           # Movie details
│   │   └── [id].tsx
│   └── _layout.tsx      # Root layout
├── components/          # Reusable UI components
├── services/            # API services
│   ├── tmdb.ts
│   └── appwrite.ts
├── lib/                 # Utilities and helpers
├── constants/           # App constants
├── .env                 # Environment variables
├── tailwind.config.js   # Tailwind configuration
└── package.json
```

## 🎨 Styling

This project uses **NativeWind**, which brings Tailwind CSS to React Native. You can style components using familiar Tailwind utility classes:

```jsx
<View className="flex-1 bg-gray-900 p-4">
  <Text className="text-white text-2xl font-bold">Movies</Text>
</View>
```

## 🔑 Key Features Explained

### Authentication

- User registration and login powered by Appwrite
- Secure session management
- Persistent authentication state
- Password reset functionality

### Movie Browsing

- Browse popular movies and TV shows
- View trending content daily and weekly
- Detailed information for each title including cast, ratings, and synopsis
- High-quality posters and backdrops from TMDB

### Saved Content

- Add movies and shows to your personal "Saved" collection
- Remove items from favorites
- Persistent storage via Appwrite database
- Synced across all user devices

### Navigation

- File-based routing with Expo Router
- Bottom tab navigation for main sections
- Smooth transitions and animations
- Deep linking support

## 🔧 Available Scripts

- `npm start` - Start the Expo development server
- `npm run android` - Run on Android device/emulator
- `npm run ios` - Run on iOS device/simulator
- `npm run web` - Run in web browser
- `npm run lint` - Run ESLint for code quality
- `npm run reset-project` - Reset project to initial state

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [TMDB](https://www.themoviedb.org/) for providing the movie database API
- [Appwrite](https://appwrite.io/) for backend services
- [Expo](https://expo.dev/) for the amazing development platform
- [NativeWind](https://www.nativewind.dev/) for Tailwind CSS support in React Native

## 📧 Contact

For questions or feedback, please reach out to [kjcodes2002@gmail.com]

## 📚 Additional Resources

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)
- [TMDB API Documentation](https://developers.themoviedb.org/3)
- [Appwrite Documentation](https://appwrite.io/docs)
- [NativeWind Documentation](https://www.nativewind.dev/)

---
