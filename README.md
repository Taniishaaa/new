### Building Money Minor: A Finance Analysis App with AI-Powered Insights

## <Introduction | Overview>

# Problem Statement
In an age of fast-changing markets and abundant data, staying on top of financial trends while managing personal investments can be daunting. Users need a solution that not only provides real-time stock updates but also offers actionable financial insights through advanced AI capabilities. Money Minor was developed to address these challenges by combining live stock data, an AI-powered chatbot, and automated report generation into a single, intuitive app.
# Target Audience
This blog is tailored for fintech enthusiasts with an intermediate understanding of web development and AI integration.

## <Design>
Money Minor's architecture integrates multiple modern technologies:
Frontend: Built with React.js, offering an intuitive user interface.
Backend: Powered by Node.js for server-side logic.
AI Integration: Gemini AI for personalized chatbot responses.
Live Stock Data: API'S like DHAN API for real-time stock market updates.
Google Cloud : Cloud Storage, Vertex AI Agent Builder

## <Prerequisites>
Readers should be familiar with technologies like React, Node.js, and basic Google Cloud Platform services. Prior experience with REST APIs and databases (like Firestore) will be beneficial but not mandatory.

# Tools Required:
Node.js installed on your system.
A code editor (e.g., VS Code).
Git for version control.

## <Step-by-step instructions>
 
# 1. Setting Up the Development Environment
 1. Install Node.js: Download and install the latest stable version of Node.js from Node.js Official Website.
 2. Set Up Your Code Editor: Install VS Code or any preferred editor.
 3. Install Git: Set up Git for version control (Git Installation Guide).
   
 4. Create a Project Folder:
>> mkdir money-minor
>> cd money-minor

5. Initialize the Project and Install Required Packages:
>> npm init -y
>> npm install react react-dom react-scripts express body-parser dotenv axios firebase

# 2. Building the Frontend with React.js
Initialize a React App:

>> npx create-react-app client
>> cd client
>> npm start

2. Create Key Components:
 • Dashboard: Displays live stock data.
 • Chatbot: Integrates Gemini AI responses.
 • Analytics: Visualizes user's financial performance.

 3. Integrate API for Live Stock Data:
 • Use Dhan API to fetch real-time short chart. 
 
3. Backend Setup with Node.js
Create an express Server
>> npm install express body-parser cors
4. Setup ChatBot using Gemini API :
>> const response = await axios({
        url: `API_URL`,
        method: "post",
        data: {
          contents: [{ parts: [{ text: currentQuestion }] }],

## Steps to Get Gemini API :
Go to Google AI studio for developers :

Sign in
Edit descriptionaistudio.google.com
2. Create API Key :
3. Use the curl command to test the AI using your API key that was generated.
5. Agent Builder (Not integrated to the webApp)
Step 1: Set Up GCP Project
1. Log in to GCP Console:
 • Navigate to Google Cloud Console.
 2. Create a New Project:
 • Click on the project dropdown (top-left corner) and select "New Project."
 • Name the project and click Create.
 3. Enable Billing (if not already enabled):
 • Go to Billing and attach a billing account to the project.
Step 2: Enable Dialogflow API
Navigate to APIs & Services > Library.
Search for Dialogflow API and click Enable.

Step 3: Access Dialogflow Console
1. Open the Dialogflow Console.
 2. Ensure the correct GCP project is selected (top-left corner).
Step 4: Create an Agent
Create New Agent:
 • Click Create Agent.
 • Provide:
 • Agent Name (e.g., "Customer Support Bot").
 • Default Language (e.g., English).
 • Time Zone.
 • Google Project (select the project you created earlier).
 • Click Create.
 2. Choose Dialogflow CX for advanced agents or Dialogflow ES for simpler needs:


Step 5: Design the Agent
1. Define Intents:
 • Navigate to the Intents section.
 • Click Create Intent to define possible user inputs and expected responses.
 2. Train the Agent:
 • Provide training phrases for each intent (examples of what users might say).
 • Define responses for the bot to provide.
 3. Set Up Entities (optional):
 • Use entities to extract specific data from user inputs (e.g., dates, locations, names).
 4. Create Flows and Pages (Dialogflow CX only):
 • Design conversation paths using flows and pages.
 • Use the visual editor to manage transitions.
Step 6: Integrate Fulfillment (Optional)
1. Enable webhook fulfillment for dynamic responses:
 • Navigate to Fulfillment.
 • Add a webhook URL (your backend service) to process user input and generate responses dynamically.
 2. Deploy a webhook backend (e.g., on Cloud Functions or App Engine).
Step 7: Test the Agent
1. Use the Simulator in the Dialogflow console to test the agent.
 2. Debug intents, entities, and responses.
Step 8: Integrate with Platforms
1. Navigate to Integrations in the Dialogflow console.
 2. Choose platforms to connect with:
 • Google Assistant
 • Facebook Messenger
 • Slack
 • Webhooks (for custom applications)
Step 9: Deploy the Agent
1. Deploy your agent by connecting it to your application.
 2. Use Dialogflow APIs for programmatic integration.
Step 10: Monitor and Improve
1. Use the Analytics section in the Dialogflow console to track usage.
 2. Continuously update intents and responses based on user feedback.

### GITHUB REPOSITORY : 
GitHub - Taniishaaa/Money-miner-new
Contribute to Taniishaaa/Money-miner-new development by creating an account on GitHub.github.com
{ use "npm i" to install all the required dependencies }

## <Result / Demo>
1.Live Markets view (currently available for only 6 stocks):
2. AI-powered chat Bot :
3. Agent Builder : 
(Currently not integrated into the webapp, but separate file is available in github repo named as new.html)
<What's next?>
Future Add on features in the money miner app :
1.1 Use of python script to read automated chart screen shots given by user of provide analysis on the data set provided. 
1.2 Use of python to access user to put in reports , portfolio link , dashboards and get the best provided guidance & analysis by the moneyMiner.
   
## <Call to action>
  
To learn more about Google Cloud services and to create impact for the work you do, get around to these steps right away:
Register for Code Vipassana sessions
Join the meetup group Datapreneur Social
Sign up to become Google Cloud Innovator
