# KSTREAM: Decentralized Learning Platform

This repository contains the source code for KSTREAM, a decentralized platform for revolutionizing online learning. KSTREAM leverages the power of the Internet Computer (ICP) to provide a secure, scalable, and user-friendly environment for both educators and learners.

## Project Overview

KSTREAM aims to solve the current limitations of traditional online learning platforms by:

* **Empowering Creators:** Providing educators with full control and better monetization options for their educational content.
* **Personalizing Learning:**  Offering real-time AI-powered explanations and personalized learning experiences to enhance learner understanding and engagement.
* **Promoting Decentralization:**  Building a secure and transparent learning ecosystem based on the Internet Computer's technology.

## Key Features

* **Decentralized Hosting:** Secure and scalable video hosting using ICP canisters.
* **AI-Powered Video Insights:** Real-time explanations generated from video transcripts to improve learning outcomes.
* **Tokenized Rewards:** An integrated token economy incentivizes both creators and learners, promoting engagement and retention.
* **No Gas Fees:** Seamless user experience with ICP's reverse gas model, eliminating transaction costs.

## Getting Started

**Prerequisites:**

* **Node.js:**  Version 16 or higher.
* **dfx:**  Internet Computer CLI tool (install using `npm install -g dfx`).

**1. Clone the Repository:**

```bash
git clone <repository-url>
cd kstream
```

**2. Install Dependencies:**

```bash
npm install
```

**3. Configure the Development Environment:**

* **Start DFX:** Run the local replica environment.
    ```bash
    dfx start --clean --background
    ```

* **Build and Deploy:** Build and deploy the canisters to the local DFX environment.
    ```bash
    npm run dfx:build
    ```

**4. Run the Development Server:**

```bash
npm start
```

This will start a development server at `http://localhost:3000`.

## Contact

For any questions, suggestions, or support, please contact us at .

## Acknowledgements

We would like to thank the following individuals and organizations for their support:
