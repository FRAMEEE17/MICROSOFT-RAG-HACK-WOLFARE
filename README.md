# 🛡️ Cyber Security News Summarizer & Chatbot Project
# 📋 Table of Contents
    - Disclaimer
    - Objective
    - Dataset Description
    - Trained Models
    - Model Performance
    - How to Run (Prototype)
    - How to Deploy the Server (Prototype)
    - Manual
    - Future Work
    
## ⚠️Disclaimer
This project is currently in the development phase. If you encounter any bugs during testing, please feel free to reach out. The project has implemented RAG with cyber security data from various sources, including the Hacker News dataset and cyber security summaries from developers (e.g., SIEM tools manuals).

## 🎯Objective
The goal of this project is to create a tool for Security Operation Centers (SOCs) that enables them to:
- Receive the most recent cyber security news.
- Interact with a personalized chatbot specialized in cyber security.
- Train the chatbot with specific cyber security knowledge.
## 📊Data description
    The project implement RAG approach with a diverse set of cybersecurity-related data sources:

        1.Cyber security news : A curated collection of cybersecurity news articles and discussions from the cyber security News platform (https://thehackernews.com/ ,https://www.darkreading.com/ , https://securityaffairs.com/category/cyber-crime).
        2.Splunk Manuals: Extensive documentation from Splunk, a leading SIEM solution, including Splunk Enterprise Security, Splunk SOAR.
        3.CrowdStrike Global Threat Report 2024: 
                - Comprehensive analysis of global cyber threat trends and emerging attack techniques.
                - Detailed breakdowns of notable adversary groups and their tactics, techniques, and procedures (TTPs).
                - Insights into evolving ransomware trends and supply chain attacks.
                - Predictions for future threat landscapes and recommendations for enhancing cybersecurity postures.
                - Case studies of significant cyber incidents and their implications for various industries.
## 🧠 Large Language Model API use
    Our project utilizes the following models:

        - Solar-1-mini-chat: Implemented with self-RAG and hybrid search (semantic search+ keyword search) methodologies for cybersecurity domain conversations.
        - Solar-embedding-1-large-query: Optimized for query embedding in the cybersecurity context.
        - Solar-embedding-1-large-passage: Specialized for document embedding of cybersecurity content.
        - Solar-1-mini-groundedness-check: Tailored for verifying the groundedness and hallucination of responses in cybersecurity discussions.
        - GPT-4o: Optimized for news summarizer.
## 📈 Model Performance
    Preliminary testing shows promising results:

        Response Accuracy: 62% 
        Average Response Time: 8.91 seconds
        Groundedness Score
        Relevance to Cybersecurity Queries (confidence score)
## 🚀How to Run (Prototype)
0. Prerequisites
Please ensure that python3, python3-pip were installed which enable to be executed via CLI.
1. Clone the project to your machine and navigate to the `src/client_scripts` directory:
```console
$ cd src/client_scripts
```
2. Install the required dependencies:
```console
$ pip3 install -r requirements.txt
```
3. Run the service (controller):
```console
$ python3 wolfare_controller.py
```
4. [Optional] For windows user please run
```console
$ python3 wolfare_controller_win.py
```

## 🖥️ How to deploy the server (Prototype)
0. Prerequisites
Please ensure that python3, python3-pip were installed which enable to be executed via CLI.
1. Clone the project to your machine and navigate to the `src/server_scripts` directory:
```console
$ cd src/client_scripts
```
2. Install the required dependencies:
```console
$ pip3 install -r requirements.txt
```
3. To deploy the server please run
```console
$ python3 api_server.py
 ```
## 📘 Manual 
0. After running the server, To open the GUI press ctrl + h on the keyboard.
1. To close the gui please ctrl + once again.
2. To close the service user can


## 🔮 Future Work
1. Make an agreement with the website owner to officially use their data. 
2. Implement SSL/TLS certificate for the API service to secure the connection in the future. 
3. Provide our own model running on our server to isolate model from the other which will give the privacy to our end user.
4. Improve UI/UX based on the user feedback.
5. Integrate additional cybersecurity news and threat intelligence feeds
6. Develop tools for clients to fine-tune AI models with their own data.
7. Integrate cutting-edge AI technologies and techniques to enhance efficiency such as intent classifier, false-negative reduction, models stacking.
