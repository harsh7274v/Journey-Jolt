JourneyJolt is an AI-based travel planning application designed to make trip planning easier and more efficient. This project leverages artificial intelligence to analyze user preferences and provide personalized recommendations for destinations, accommodations, and activities.

Key features of JourneyJolt include:

Personalized Recommendations: The AI suggests ideal destinations, hotels, and activities tailored to the traveler's preferences.
Automated Itinerary Generation: The app automatically creates a full itinerary that considers factors like travel time and user preferences.
JourneyJolt aims to enhance the travel experience by providing a streamlined, easy-to-use platform for trip planning, designed for both casual travelers and frequent explorers alike.

Built With
This project is built with the following major frameworks, libraries, and services:

React
Vite
Tailwind CSS
Google Cloud
Gemini AI
Firebase
Auth0
React Hot Toast
Getting Started
Setting up JourneyJolt is simple — just configure your .env file, and you're ready to go!

To get started with JourneyJolt, follow these instructions to set up the project locally on your machine for development and testing.

Prerequisites
Before you begin, ensure you have the following installed:

Node.js (v16.0 or above) - Download Node.js
VS Code (Code Editor) - Download VS Code
Services & API Keys Setup
To fully integrate JourneyJolt with third-party services, you'll need to sign up for the following services, configure the required settings, and obtain API keys. Below are the steps for each service:

Google Cloud Setup
Follow these steps to set up Google Cloud for your project:
Create an account on Google Cloud.
As a new user, you will receive a free trial with 90 days and ₹25,000 in free credits, which you can use for your project.
After setting up your account, go to the APIs & Services section to create an API key.
Next, enable the following APIs:
Maps JavaScript API
Maps Embed API
Geolocation API
Geocoding API
Places API
Places API (New)
The "Places API (New)" may require you to set up a billing account. Don't worry, your free credits are more than enough to cover the cost!
Once everything is set up, you will have your Google API key ready to use.
Paste the API key in your environment file:
VITE_GOOGLE_MAP_API_KEY="YOUR_GOOGLE_API_KEY"
Gemini API Setup
Follow these steps to set up the Gemini API:
Go to the Gemini AI website.
Create an account if you don't have one, or sign in with your existing account.
The Gemini API is free, meaning there are no charges associated with using it for your project.
Once your account is set up, you can start using the Gemini API for your project.
Paste the API key in your environment file:
VITE_GEMINI_API_KEY="YOUR_GEMINI_API_KEY"
Auth0 Setup
Follow these steps to set up Auth0 for your project:

Go to the Auth0 website.
Create a free account. The free plan supports up to 25,000 monthly active users, which is more than enough for our project.
After signing up, select the type of project you are creating. Choose "Single Page Application" as we are building a React app.
Once your account is set up, create a new application within Auth0.
Go to the settings of the created application to get the authentication credentials.
You'll need the following credentials:
Domain Name
Client ID
Paste the credentials into your environment file:
VITE_DOMAIN_NAME="your-auth0-domain"
VITE_AUTH0_CLIENT_ID="your-client-id"
Important Note: After running the project, you will need to configure the callback URL and logout URL in the Auth0 application settings. The callback URL should be the hosted URL of your React app when it is running locally or deployed. (generally: http://localhost:5173/)

Firebase Setup
Visit the Firebase website and create an account or log in if you already have one.
Once logged in, create a new project by clicking on "Add Project". Follow the prompts for setting up the project. Choose the "Test mode" option for the database so you can easily set up read and write permissions.
After the project is created, click on the "Web" icon to create a new web app within the Firebase project.
Follow the prompts to register your app. Firebase will provide you with the necessary configuration details during this step.
Once the web app is created, go to your Firebase Console, and select the project you just created.
Create Firestore Databse, this will be the actaul database where we will store everything
In Firestore Databse, go to the "Rules" tab and edit the read and write rules so that you can save data
allow read, write: if request.time < timestamp.date(2099, 8, 18);
Navigate to the "Project settings" by clicking on the gear icon near the top left corner.
In the "General" tab, you will find the credentials for your Firebase project. These credentials are needed to set up Firebase in your React project.
Copy the credentials provided by Firebase (e.g., API key, auth domain, etc.) and paste them into your `.env` file with the following format:
    VITE_FIREBASE_API_KEY = "your-api-key-here"
    VITE_FIREBASE_AUTH_DOMAIN = "your-auth-domain-here"
    VITE_FIREBASE_PROJECT_ID = "your-project-id-here"
    VITE_FIREBASE_STORAGE_BUCKET = "your-storage-bucket-here"
    VITE_FIREBASE_MESSAGING_SENDER_ID = "your-messaging-sender-id-here"
    VITE_FIREBASE_APP_ID = "your-app-id-here"
    VITE_MEASUREMENT_ID = "your-measurement-id-here"
  

Installation
The installation process is straightforward. You can either clone the repository or download the zip file of the code.

Steps to Install and Set Up:
Clone the repository or download the ZIP file

To clone the repo, run the following command:
 you can download the ZIP file from the repository page and extract it.
Open the project folder in a code editor
Open the folder in your preferred code editor (e.g., VS Code).

Set up the .env file
The main objective is to set up your .env file with the necessary API keys.

Follow the steps in the Setup and API Keys section to get the required API keys for Google Cloud, Gemini API, Auth0, and Firebase.
After getting the keys, create a .env file in the root of the project and add the required keys like so:
VITE_GOOGLE_MAP_API_KEY = "your-google-api-key"
VITE_GEMINI_API_KEY = "your-gemini-api-key"
VITE_AUTH0_CLIENT_ID = "your-auth0-client-id"
VITE_DOMAIN_NAME = "your-auth0-domain-name"
VITE_FIREBASE_API_KEY = "your-firebase-api-key"
VITE_FIREBASE_AUTH_DOMAIN = "your-firebase-auth-domain"
VITE_FIREBASE_PROJECT_ID = "your-firebase-project-id"
VITE_FIREBASE_STORAGE_BUCKET = "your-firebase-storage-bucket"
VITE_FIREBASE_MESSAGING_SENDER_ID = "your-firebase-messaging-sender-id"
VITE_FIREBASE_APP_ID = "your-firebase-app-id"
VITE_MEASUREMENT_ID = "your-firebase-measurement-id"
Install required NPM packages
Once the .env file is set up, install the required NPM packages:

npm install
Run the Project
After the packages are installed, you can start the development server by running:

npm run dev
This will run the project locally and you can access it at http://localhost:5173.

By following these simple steps, you'll have the project up and running in no time!

Roadmap
The roadmap represents the challenges and updates that I plan to implement in the future. As I continue to enhance the project, I encourage you to try completing these tasks as well and contribute to the project. Collaboration is welcome, and feel free to open pull requests with improvements or fixes. Here's what's coming next:

 Set up project environment with API keys
 Add Google Cloud API integration for Maps, Geolocation, and Places
 Add Gemini AI API integration for AI-based content generation
 Set up Auth0 authentication for secure login (including Callback URL setup)
 Add Firebase integration for real-time data storage
 Implement a more user-friendly UI for API Key setup
 Implement additional functionality for Google Maps (e.g., custom markers)
 Optimize app for mobile devices
 Implement unit testing for all components
 Add better error handling for API integrations
 Multi-language Support
 Hindi
 Deploy the project to a cloud platform (e.g., Firebase Hosting, Vercel)
 Add detailed logging for API requests and responses
 Implement automatic configuration of environment variables from the UI
