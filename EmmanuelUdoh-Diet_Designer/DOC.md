 # Diet Designer: A Personalized Food Planner Unlock Your Optimal Diet

Diet Designer is an application that allows users to schedule and customize their preferred meals throughout the week.

1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Technical Details](#technical-details)
4. [Getting Started](#getting-started)
5. [Security And Privacy](#security-and-rivacy)
6. [User Authentication](#user-authentication)


## Overview

    Diet Designer is an innovative food planner app that tailors meal plans to your unique needs and goals. By harnessing the power of AI, we empower you to take control of your nutrition and achieve a healthier, happier you.

## Key Features
   - `User Registration`: Sign up securely using Internet Identity
   - `Create a Meal Plan`: After signing up, you can create a personalized meal plan.
   - `Personalized Meal Planning Through Questionnaire`: Answer a series of questions to get customized meal plans based on your dietary preferences.
   - `Generate Meal Plan`: AI-Driven Insights technology analyzes your input to generate unique optimized meal plans.
   - `Diverse Dietary Options`: Catering to various needs, including fitness, weight loss, diabetes, and more.
   <!-- - `Caloric Control`: Set your daily caloric intake and receive tailored meal plans.
   - `Mobile Optimization`: Designed for seamless mobile use.
   - `Telegram Integration`: Coming soon for effortless user experience.
   - `Admin Capabilities`: Doctors and football clubs can manage patients' and players' meal plans. -->


# Technical Details
    To get started, you might want to explore the project directory structure and the default configuration file. Working with this project in your development environment will not affect any production deployment or identity tokens.

- **`Backend`**: Built with `Motoko` programming language 
- **`Libraries`**: Mops
- **`Frontend`**: React and JavaScript
- **`CSS Framework`**: Tailwind CSS
- **`API Service`**: FastAPI Deployment: Fly.io

  - **Node.js** Install the latest node version from the official websit.
  - **IC SDK and Motoko** [Install the latest IC SDK. Refer to this guide](https://internetcomputer.org/docs/current/developer-docs/getting-started/install/)
   - **Clone project** You can now clone the project from the base repo [Diet Designer](https://github.com/DietDesigner/Diet_Designer.git/)
  - **Deploy** You can deploy the project with 
```bash
    dfx start
    dfx deploy
    npm start
  ```


# Getting Started


1. **`User Onboarding`**: Sign up, and set dietary preferences, and goals.
2. **`Meal Planning`**: Receive personalized meal plans and edit as needed. 
<!-- 3. **`Admin Features`**: Manage patients' or players' meal plans. -->


# Security And Privacy

   - ***`Data Protection`***: Secure authentication and authorization measures.
   - ***`Confidentiality`***: Only necessary information is shared with the AI service. Future Developments
   - ***`Global Recipe Access`***: Integration with trained AI for worldwide recipe access. Expanded Options: More dietary needs and preferences.
   ***`Enhanced Admin`***: Improved features for doctors and football clubs.

   ## User Authentication

        User authentication is managed using the AuthClient from the @dfinity/auth-client library, which is a standard method for handling authentication on the Internet Computer. This ensures that user sessions are secure and that data access is properly restricted based on user identity.
