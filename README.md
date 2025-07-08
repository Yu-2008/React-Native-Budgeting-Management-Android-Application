# Acorn Budgeting App - A React Native Budgeting Android Application

Assignment for UECS3253 Wireless Application Development.

This repository presents a complete budgeting management application called "**Acorn Budgeting App**", developed using React Native and specifically designed for the Android platform. It includes the full source code for key features, including income and expense management, budget categorization, location tracking, and backup and restore by cloud and local storage functionality, and theme customization. Acorn Budgeting App demonstrates the use of modern React Native components and custom components, integration of APIs and cloud service, cloud and local storage solutions, and user-friendly UI design for efficient personal finance management.

## Objective
The objective of this project is to develop a user-centric budgeting app that simplifies financial tracking and encourages better financial habits. This application aims to to provide a clear overview of users' financial activities and a seamless personal finance management by integrating features including category-based income and expenses management, location-aware income and expense tracking, and persistent data storage using both local and cloud solutions with React Native and APIs' services.

## Key Features
### 1. Sign Up
Allows new users to create an account by providing an email address, username, and password. Once registered, users can begin recording and managing their financial activities.
### 2. Sign In
Enables existing users to access their accounts using their registered email and password.
### 3. Forget Password
If a user forgets their password, they can request a password reset link by entering their registered email. The link sent to their inbox allows them to create a new password and regain access.
### 4. Adding Income Transaction Record
Users can record income transactions by selecting a category (e.g., salary, tips) and filling in details such as title, amount, and date. Optional fields include description and location.
### 5. Adding Expenses Transaction Record
Users can record expense transactions by selecting a category (e.g., transportation, education), and filling in details such as title, amount, and date. Optional fields include description and location.
### 6. Editing Transaction Record
Allows users to update certain transaction details such as title, category, date, and description. However, fields like the transaction type (income or expense) and location are not editable.
### 7. Deleting Transaction Record
Enables users to permanently delete any transaction, ensuring clean and accurate financial records.
### 8. Adding Income Category
Users can create custom income categories by entering a title, description, and choosing from a selection of predefined icons.
### 9. Editing Income Category
Allows modification of the title and description of existing income categories.
### 10. Deleting Income Category
Remove income categories that are no longer useful, maintaining a clean category list.
### 11. Adding Expenses Category
Users can create custom expenses categories by entering a title, description, and choosing from a selection of predefined icons.
### 12. Editing Expenses Category
Allows modification of the title and description of existing expenses categories.
### 13. Deleting Expenses Category
Remove expenses categories that are no longer useful, maintaining a clean category list.
### 14. Choosing Theme
Users can personalize their experience by switching between light and dark themes for optimal visual comfort.
### 15. Back Up to Cloud Firestore or local storage and Restore from Cloud Firestore or loca storage
Users can back up all transaction data to Cloud Firestore or local storage for safekeeping and restore previously saved data with the latest backup.
### 16. Sign Out
Safely logs users out of the app while retaining all transaction records and preferences.
### 17. Delete Account
Users can permanently delete their account. Once account is deleted, all associated data from both the local SQLite database and Firebase Authentication are also deleted. This action is unrecoverable.


## Technologies Used
|Tools/Libraries|Description|
|---|---|
|React Native|Used as the main framework to develop the application.|
|JavaScript|Used mainly in styling file.|
|TypeScript|Used as the main programming language for source code.|
|Visual Studio Code|Primary code editor used for writing and managing the codebase.|
|Android Studio|Used for running and testing the application on Android emulator.|
|AbstractAPI - Email Validation and Verification API|Used to check if the entered email is valid in both format and Mail Exchange (MX) record during sign-up and sign-in.|
|Firebase API - Authentication and Cloud Firestore| Firebase Authentication used for user sign-up, sign-in, and account management while Cloud Firestore used for backup and restore of transaction data on cloud.|
|SQLite|Used as local storage for users' data, including transaction and categories details.|
|AsyncStorage|Used for storing key-values pair data.|
|Geolocation|Used for tracking location in latitude and longitude format.|
|OpenCage Geocoding API|Used to convert latitude and longitude into meaningful and human-understandable location name.|
|PubNub Real-Time API|Used for real-time data sync.|

***Remark:*** Please refers to "package.json" file for all used dependencies.


## Methodology
1. Analyzing requirement
2. Developing an UI/UX prototype
3. Designing overall system architecture
4. Testing and debugging



## Getting Started

This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

>**Note**: Make sure you have completed the [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup) instructions till "Creating a new application" step, before proceeding.

## Step 1: Start the Metro Server

First, you will need to start **Metro**, the JavaScript _bundler_ that ships _with_ React Native.

To start Metro, run the following command from the _root_ of your React Native project:

```bash
# using npm
npm start

# OR using Yarn
yarn start
```

## Step 2: Start your Application

Let Metro Bundler run in its _own_ terminal. Open a _new_ terminal from the _root_ of your React Native project. Run the following command to start your _Android_ or _iOS_ app:

### For Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android
```

### For iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios
```

If everything is set up _correctly_, you should see your new app running in your _Android Emulator_ or _iOS Simulator_ shortly provided you have set up your emulator/simulator correctly.

This is one way to run your app — you can also run it directly from within Android Studio and Xcode respectively.

## Step 3: Modifying your App

Now that you have successfully run the app, let's modify it.

1. Open `App.tsx` in your text editor of choice and edit some lines.
2. For **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Developer Menu** (<kbd>Ctrl</kbd> + <kbd>M</kbd> (on Window and Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (on macOS)) to see your changes!

   For **iOS**: Hit <kbd>Cmd ⌘</kbd> + <kbd>R</kbd> in your iOS Simulator to reload the app and see your changes!

## Step 4: Download all folders and files (except "package.json") from this repository

If everything goes well, let's installing the dependencies. Please enter your React Native root directory by using terminal or CMD and run the following command:

 ```bash
# using npm
npm install 
```

If you want to uninstall some package, please run the command:

 ```bash
# using npm
npm uninstall package-name
```
***Tips:*** If you encounter any error, try to uninstall pubnub's packages ("pubnub-react" and "pubnub") first and install the other packages again. After all the other dependencies installed, then only reinstall pubnub's packages ("pubnub-react" and "pubnub") .

***Remark:*** Always not manually edit your "package.json" and "package-lock.json" files.

## Step 5: Setup configuration files

**Important Note**: All configuration files containing sensitive information (such as API keys, Firebase credentials, and other private settings) have been **intentionally excluded** from this repository for security reasons.

To run this project locally, you’ll need to create your own config files based on the required structure. Please create a folder with named "config" inside "src" and follow the instruction below:
### Firebase API
1. Register a free account at Firebase website at https://console.firebase.google.com/u/0/.
2.	Create a Firebase project on the website and get the unique API key.
3.	Create a configuration file with name “FirebaseConfig.ts” in “src/config” folder for the usage of Firebase. Copy the API key gets from Firebase website and then paste into the configuration file. The details of the configuration file are shown at below:
```bash
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "YOUR-API-KEY",
  authDomain: "YOUR-DOMAIN",
  projectId: "YOUR-PROJECT-ID",
  storageBucket: "YOUR-STORAGE-BUCKET",
  messagingSenderId: "YOUR-SENDER-ID",
  appId: "YOUR-APP-ID",
  measurementId: "YOUR-MEASUREMENT-ID"
};

// Initialize Firebase
export const FIREBASE_APP = initializeApp(firebaseConfig);
export const FIREBASE_AUTH = getAuth(FIREBASE_APP);
export const FIREBASE_DB = getFirestore(FIREBASE_APP);
```
### Abstract API
1.	Register a free account at https://www.abstractapi.com/.
2.	Access to the https://www.abstractapi.com/api/email-verification-validation-api and get the unique API key.
3.	Create a configuration file with name “abstractEmailConfig.ts” in “src/config” folder for the usage of Abstract API. Copy the API key gets from Abstract API website and then paste into the configuration file. The details of the configuration file are shown at below:
```bash
export const ABSTRACT_EMAIL_API_KEY = 'YOUR-API-KEY';
export const ABSTRACT_EMAIL_BASE_URL = 'YOUR-BASE-URL';
```
### OpenCage Geocoding API
1.	Register a free account at https://opencagedata.com/.
2.	Access to the https://opencagedata.com/dashboard#geocoding and get the unique API key.
3.	Create a configuration file with name “openCageConfig.ts” in “src/config” for the usage of OpenCage Geocoding API. Copy the API key gets from OpenCage website and then paste into the configuration file. The details of the configuration file are shown at below.
4.	Create a new file with name “emailValidation.ts” in “src/services” folder for the access service of Abstract API. The details of the service file are shown at below:
```bash
export const OPEN_CAGE_API_KEY = 'YOUR-API-KEY';
export const OPEN_CAGE_BASE_URL = 'YOUR-BASE-URL';
```
### PubNub Real-Time API
1.	Register a free account at Pubnub website at https://www.pubnub.com/.
2.	Create a Pubnub project on the website and get the unique API key.
3.	Create a configuration file with name “pubnubConfig.ts” in “src/config” for the usage of PubNub Real-Time API. Copy the API key gets from PubNub website and then paste into the configuration file. The details of the configuration file are shown at below:
```bash
import PubNub from 'pubnub';

const PUBNUB_PUBLISH_KEY = 'pub-c-cf0b55ea-29d2-4169-96ec-90dbc6245c27';
const PUBNUB_SUBSCRIBE_KEY = 'sub-c-249e82b7-53f8-4399-b070-8fbea7f745c2';

export const pubnub = new PubNub({
  publishKey: PUBNUB_PUBLISH_KEY,
  subscribeKey: PUBNUB_SUBSCRIBE_KEY,
  uuid: PubNub.generateUUID(),
});
```

## Congratulations! :tada:

You've successfully done the setup for Acorn Budgeting App. Please enjoy the service! :partying_face:


## Authors
- [@Yu-2008] (https://github.com/Yu-2008)
- [@Jacqueline-Lim] (https://github.com/Jacqueline-Lim)
- [@LIOWKEHAN] (https://github.com/LIOWKEHAN)


## Contributing

Contributions are always welcome!

To get started:

1. **Fork** the repository to your GitHub account.
2. **Create a new branch** for your feature or fix:  
   `git checkout -b your-feature-name`
3. **Make your changes** and commit them with a clear message:  
   `git commit -m "Add: Description of your change"`
4. **Push** your branch to your forked repository:  
   `git push origin your-feature-name`
5. **Open a Pull Request** from your branch to the main project.

Feel free to open an issue first if you'd like to discuss your idea before implementing it.

