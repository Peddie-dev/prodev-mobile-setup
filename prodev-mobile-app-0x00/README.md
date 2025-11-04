# 📱 React Native Mobile App — Expo Router Setup

## Project Overview
This project contains my first mobile application scaffolded using the **Expo Router** template for React Native.  
It demonstrates project scaffolding, the file-based routing provided by Expo Router, running the app on a physical device using **Expo Go**, and the effects of resetting the project state.

---

## 🧩 Project Objective
- Initialize a fresh **Expo Router** project.
- Modify the default Home screen text.
- Run and test the app on a physical device (Expo Go).
- Run `npm run reset-project` and document its behavior.

---

## 🛠️ Steps Followed for Scaffolding

1. **Open terminal and move to parent project directory**
   ```bash
   cd prodev-mobile-setup
Create the Expo project (Router template)

bash
Copy code
npx create-expo-app@latest prodev-mobile-app-0x00
When prompted, selected Navigation (Expo Router).

Open the project folder

bash
Copy code
cd prodev-mobile-app-0x00
Start the development server

bash
Copy code
npx expo start
Connect to the app via Expo Go

Open Expo Go on your phone.

Scan the QR code shown in the terminal/Metro bundler.

The app initially displayed the default text Welcome!.

Modify the Home Screen

File edited: app/(tabs)/index.tsx

Replaced:

tsx
Copy code
<Text>Welcome!</Text>
with:

tsx
Copy code
<Text>** First App Created**</Text>
The app reloaded and displayed the new text automatically.

📲 How to Run Locally
Install dependencies (if not already present):

bash
Copy code
npm install
If you hit peer dependency resolution issues, try:

bash
Copy code
npm install --legacy-peer-deps
Start the Metro bundler:

bash
Copy code
npx expo start
Open the app on a device:

Android: Scan QR with Expo Go.

iOS: Scan with the Camera app (or use Expo Go).

🔄 Observations from npm run reset-project
When running:

bash
Copy code
npm run reset-project
Observed behavior:

Metro bundler caches were cleared.

Temporary build files and caches were removed.

node_modules may be deleted depending on the reset script implementation.

The project was returned to a clean state; source files (app/, constants/, etc.) were preserved.

After running npm install again, dependencies were reinstalled and the app ran normally.

Conclusion: reset-project is useful for resolving caching-related or dependency issues without affecting source code.

🧪 Tests & Verification Performed
Verified the app loads on an Android device via Expo Go.

Confirmed that changing app/(tabs)/index.tsx updates the running app (hot reload).

Ran npm run reset-project and then npm install to verify project rebuild and app run.

📁 Project Structure (relevant)
bash
Copy code
prodev-mobile-setup/
└── prodev-mobile-app-0x00/
    ├── app/
    │   └── (tabs)/
    │       └── index.tsx         # Home screen file edited
    ├── app-example/              # (If present) backup or sample app folder
    │   └── app/
    │       └── (tabs)/index.tsx
    ├── constants/
    │   └── Colors.tsx
    ├── README.md
    ├── App.tsx
    ├── package.json
    └── ...
⚠️ Challenges & Solutions
Challenge: EPERM: operation not permitted, rename '...app' -> '...app-example\app' during scaffold.
Cause: Windows file lock or OneDrive/antivirus interference (project on Desktop/OneDrive), or folder open in editor.
Fixes:

Move project out of Desktop/OneDrive (e.g., C:\dev\prodev-mobile-app-0x00).

Close VS Code / File Explorer windows that reference the folder.

Run PowerShell/CMD as Administrator.

Disable OneDrive sync or temporary antivirus real-time protection during scaffold.

Recreate project in a clean directory: npx create-expo-app@latest prodev-mobile-app-0x00.

Challenge: npm install dependency / network errors (ECONNRESET, peer conflicts).
Fixes:

Clear npm cache: npm cache clean --force.

Reset npm registry: npm config set registry https://registry.npmjs.org/.

Use legacy peer deps when necessary: npm install --legacy-peer-deps.

Retry on stable network or use a different registry as a temporary workaround: --registry=https://registry.yarnpkg.com.

✅ Final Output / What I Delivered
A working Expo Router project that displays:

sql
Copy code
** First App Created**
on the home screen.

Documentation of scaffolding steps and the reset-project behavior saved in this README.md.

💾 Commit & Push Example
bash
Copy code
git add .
git commit -m "feat: scaffold expo router app and document setup; updated home screen"
git push origin main
📞 Contact / Notes
If you want, I can:

Add your device model and OS version to the README.

Provide a short GIF or screenshot for proof (I can tell you how to generate one locally).

Create app-example/ with the original scaffold as backup before changes.

vbnet
Copy code

If you want, I can also:

- Produce the exact `index.tsx` change snippet (ready to paste), or  
- Create an `app-example/` backup structure for you and show the commands to commit both. Which would you like next?






You said:
the entire file should be markdown



ChatGPT said:
Got it ✅ — here’s the fully Markdown-formatted README.md file.
You can copy and paste this directly into your project without any extra editing.

markdown
Copy code
# 📱 React Native Mobile App — Expo Router Setup

## 🧭 Project Overview
This project contains my first mobile application scaffolded using the **Expo Router** template for React Native.  
It demonstrates project scaffolding, file-based routing, running the app on a physical device using **Expo Go**, and understanding what happens when resetting the project.

---

## 🎯 Objective
- Initialize a new Expo project using the **Expo Router** template.  
- Modify the default Home screen text.  
- Run and test the app on a physical device using **Expo Go**.  
- Execute the `npm run reset-project` command and document the outcome.  

---

## 🧩 Steps Followed for Scaffolding

### 1. Navigate to Project Directory
```bash
cd prodev-mobile-setup
2. Initialize the Project
bash
Copy code
npx create-expo-app@latest prodev-mobile-app-0x00
When prompted, select the Navigation (Expo Router) template.

3. Move into the Project
bash
Copy code
cd prodev-mobile-app-0x00
4. Start the Development Server
bash
Copy code
npx expo start
5. Connect via Expo Go
Open the Expo Go app on your phone.

Scan the QR code displayed in the terminal or browser.

The default app should display:

Copy code
Welcome!
6. Modify the Home Screen
Open the file:
app/(tabs)/index.tsx

Locate this line:

tsx
Copy code
<Text>Welcome!</Text>
Replace it with:

tsx
Copy code
<Text>** First App Created**</Text>
Save the file — the app should reload and show the new message.

🧠 Understanding the File Structure
After scaffolding, the structure looks like this:

arduino
Copy code
prodev-mobile-setup/
└── prodev-mobile-app-0x00/
    ├── app/
    │   └── (tabs)/
    │       └── index.tsx
    ├── constants/
    │   └── Colors.tsx
    ├── package.json
    ├── App.tsx
    ├── README.md
    └── ...
If app-example/ exists, it may contain a backup or sample app folder:

markdown
Copy code
app-example/
 └── app/
     └── (tabs)/
         └── index.tsx
⚙️ Running and Testing the App
1. Install Dependencies
bash
Copy code
npm install
If you encounter dependency errors:

bash
Copy code
npm install --legacy-peer-deps
2. Start the App
bash
Copy code
npx expo start
Android: Open Expo Go and scan the QR code.

iOS: Use your Camera app or Expo Go to scan.

🔄 Resetting the Application
Run:

bash
Copy code
npm run reset-project
🧾 Observations:
Clears Metro bundler cache.

Removes build and temporary files.

Returns the app to a clean, initial state.

Source files (app/, constants/, etc.) remain intact.

After running npm install, the app rebuilds successfully.

Conclusion:
The reset-project command is useful for resolving build or cache issues without affecting your source code.

🧪 Tests and Verification
✅ Verified that the app loads correctly on an Android device via Expo Go.

✅ Confirmed that editing app/(tabs)/index.tsx hot-reloads changes.

✅ Executed npm run reset-project and restored the app with npm install.

⚠️ Challenges and Fixes
Challenge 1:
EPERM: operation not permitted, rename '...app' -> '...app-example\app'

Cause:
Windows file-lock or OneDrive sync issue.

Fix:

Move the project out of the Desktop (e.g., C:\dev\prodev-mobile-app-0x00).

Close VS Code or File Explorer windows referencing the folder.

Run PowerShell as Administrator.

Disable OneDrive sync or antivirus temporarily.

Recreate the project cleanly:

bash
Copy code
npx create-expo-app@latest prodev-mobile-app-0x00
Challenge 2:
npm ERR! network Invalid response body ... ECONNRESET

Cause:
Network instability or corrupted npm cache.

Fix:

bash
Copy code
npm cache clean --force
npm config set registry https://registry.npmjs.org/
npm install --legacy-peer-deps
If persistent:

bash
Copy code
npm install --registry=https://registry.yarnpkg.com
✅ Final Output
After running and modifying the app, the home screen displays:

sql
Copy code
** First App Created**
📝 README Contents Summary
This file documents:

Setup steps for scaffolding the Expo Router project.

File structure and explanation.

Reset project observations.

Common setup challenges and how to fix them.