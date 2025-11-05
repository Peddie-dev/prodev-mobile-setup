# 📱 React Native Mobile App — Expo Router Setup

## 🧭 Overview
This project is my first mobile app built using the **Expo Router** template for React Native.  
It demonstrates how to scaffold, edit, and run a React Native app using **Expo Go**, and documents what happens after resetting the project.

---

## 🛠️ Setup & Scaffolding Steps

### 1. Navigate to the Parent Directory
```bash
cd prodev-mobile-setup
```

### 2. Create the Expo Project (Router Template)
```bash
npx create-expo-app@latest prodev-mobile-app-0x00
```
When prompted, select **Navigation (Expo Router)**.

### 3. Open the Project Folder
```bash
cd prodev-mobile-app-0x00
```

### 4. Start the Development Server
```bash
npx expo start
```

### 5. Connect via Expo Go
- Open **Expo Go** on your phone.  
- Scan the **QR code** displayed in the terminal or Metro bundler.

The app should display the default text:
```
Welcome!
```

### 6. Modify the Home Screen
**File:** `app/(tabs)/index.tsx`
```tsx
// Original
<Text>Welcome!</Text>

// Updated
<Text>** First App Created **</Text>
```
The app reloads automatically and displays the new message 🎉

---

## 📁 Project Structure
```pgsql
prodev-mobile-setup/
└── prodev-mobile-app-0x00/
    ├── app/(tabs)/index.tsx
    ├── constants/Colors.tsx
    ├── App.tsx
    ├── package.json
    └── README.md
```

---

## 🔄 Resetting the Project
To reset caches and restore a clean state:
```bash
npm run reset-project
```

### 🧩 Observed Behavior
- Cleared Metro bundler cache  
- Removed temporary build files  
- Preserved source code  

Reinstall dependencies to continue:
```bash
npm install
```

---

## ⚙️ Run the App
```bash
npm install
npx expo start
```

- **Android:** Scan QR with Expo Go  
- **iOS:** Use Camera app or Expo Go  

---

## ⚠️ Common Issue & Fix

**Error:**
```lua
EPERM: operation not permitted, rename '...app' -> '...app-example\app'
```

**Fix:**
- Move project out of **Desktop** or **OneDrive**  
- Close open folders in **VS Code**  
- Run terminal as **Administrator**  
- Or recreate cleanly:
```bash
npx create-expo-app@latest prodev-mobile-app-0x00
```

---

## ✅ Final Output
After modification, the app displays:
```sql
** First App Created **
```

---

## 👤 Author
**Name:** Henry Edwin Omino  
**Framework:** React Native (Expo Router)  
**Platform:** Windows 10  
**Tool:** Expo Go
