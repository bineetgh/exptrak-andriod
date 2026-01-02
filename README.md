# ExpTrak - Recurring Expense Tracker

A React Native mobile app for tracking recurring expenses with intelligent recurrence patterns, category management, and visual analytics.

## Features

### Core Functionality
- ✅ **Add/Edit/Delete Recurring Expenses** - Track rent, subscriptions, bills, and more
- ✅ **Flexible Recurrence Patterns** - Daily, weekly, monthly, and yearly with custom intervals
- ✅ **Smart Upcoming View** - See all upcoming expenses grouped by time (Overdue, Today, This Week, Later)
- ✅ **Category Management** - 8 default categories with icons and colors
- ✅ **Visual Analytics** - Pie chart showing spending breakdown by category
- ✅ **Local Data Storage** - All data stored locally using AsyncStorage

### Recurrence Patterns
The app supports sophisticated recurrence patterns:
- **Daily**: Every N days
- **Weekly**: Every N weeks on a specific day
- **Monthly**: Every N months on a specific day (handles edge cases like 31st → Feb 28/29)
- **Yearly**: Every N years on a specific date

### Smart Features
- Automatic calculation of next occurrence dates
- Color-coded due dates (red=overdue, orange=soon, green=upcoming)
- Category-based expense organization
- Pull-to-refresh on home screen
- Form validation and error handling

## Tech Stack

- **Framework**: React Native 0.83.1
- **Language**: TypeScript
- **Navigation**: React Navigation (Bottom Tabs + Stack)
- **State Management**: React Context API
- **Storage**: AsyncStorage
- **Date Handling**: date-fns
- **Charts**: react-native-chart-kit
- **UI**: Custom components with consistent design system

## Installation & Setup

### Prerequisites
- Node.js >= 20
- React Native development environment ([Setup Guide](https://reactnative.dev/docs/environment-setup))
- For iOS: Xcode and CocoaPods
- For Android: Android Studio and SDK

### Install Dependencies
```bash
npm install
```

### iOS Setup
```bash
cd ios
pod install
cd ..
```

### Run the App

**iOS:**
```bash
npm run ios
```

**Android:**
```bash
npm run android
```

## Default Categories

The app comes with 8 pre-configured categories:
1. 🏠 Housing
2. 💡 Utilities
3. 🎬 Entertainment
4. 🚗 Transportation
5. 🛡️ Insurance
6. 📱 Subscriptions
7. 🍔 Food & Dining
8. 📌 Other

## How It Works

### Recurrence Calculation
The app doesn't store individual occurrences. Instead, it calculates them on-the-fly using the recurrence pattern. This approach:
- Saves storage space
- Handles infinite recurrence patterns
- Updates automatically when patterns change
- Handles edge cases (e.g., monthly on 31st, leap years)

### Data Storage
- All expenses: `@ExpTrak:expenses`
- All categories: `@ExpTrak:categories`
- Data persists between app sessions
- No internet connection required


## Future Enhancements

Potential features to add:
- [ ] Custom categories (add/edit/delete)
- [ ] Expense search and filtering
- [ ] Export data (CSV/JSON)
- [ ] Notifications for upcoming expenses
- [ ] Dark mode support
- [ ] Multiple currency support
- [ ] Backup & restore

## License

MIT

