SU - Chatbot

Introduction

Welcome to SU - Chatbot, a project designed to help students and users learn more about Sitare University effortlessly. The chatbot provides instant answers to queries related to the university, making information easily accessible to everyone, especially students from underprivileged backgrounds who might lack the necessary resources to explore educational opportunities.

Since Sitare University started in 2022, some information is still being gathered, and the chatbot will continue to improve as more data becomes available.

Features

User Authentication: Login/signup functionality to track user interactions.

Admin Access: Password-protected admin dashboard for query analysis.

Interactive Chat Interface: Users can ask questions and receive real-time responses.

Query History: Displays past questions asked in the session.

Feedback Mechanism: Users can rate responses and provide feedback.

Cluster-Based Query Analysis: Assigns queries to clusters based on similarity.

Admin Dashboard: Visualizes user interests using graphs.

Efficient Query Processing: Uses vector embeddings for accurate response retrieval.

LLAMA Integration: Enhances responses using the LLaMA model.

Query Limit: Users can make up to 10 queries per hour.

Data Visualization: Displays query trends and areas for improvement.

Technology Stack

Backend

Flask: Handles API requests and routing.

Psycopg2: Connects to PostgreSQL database.

SentenceTransformers: Generates vector embeddings for queries.

NumPy: Performs numerical computations.

SkLearn.cluster: Clustering of embeddings.

Pandas: Data processing and analysis.

Groq API: Communicates with LLAMA model for enhanced responses.

Matplotlib & Seaborn: Visualizes query distribution and trends.

Frontend

HTML: Structures chatbot interface.

CSS: Enhances UI design.

JavaScript (JS): Handles interactivity (e.g., password toggle, star rating).

Project Structure

├── backend
│   ├── subot.py               # Main chatbot backend logic
│   ├── pgvector_embedding.py  # Handles vector embeddings
│   └── database.sql           # Database schema
│
├── frontend
│   ├── templates
│   │   ├── login_page.html    # User authentication page
│   │   ├── index.html         # Chat interface
│   │   ├── user_data.html     # Admin dashboard
│   ├── static
│   │   ├── styles.css         # Stylesheets
│   │   ├── script.js          # JavaScript functions
│
├── database
│   ├── qa_embeddings.sql      # Stores Q&A embeddings
│   ├── user_data.sql          # Tracks user queries
│   ├── feedback.sql           # Stores feedback
│
├── README.md                  # Project documentation
└── requirements.txt            # Dependencies

Database Tables

qa_embeddings: Stores clusters, questions, answers, and embeddings.

user_data: Tracks user queries and clusters.

feedback: Stores feedback and ratings, marking low-rated responses for improvement.

Installation & Setup

Prerequisites

Python 3.x

PostgreSQL

Node.js (for frontend interactivity)

Setup Instructions

Clone the repository:

git clone <repo-link>
cd su-chatbot

Install dependencies:

pip install -r requirements.txt

Set up the PostgreSQL database:

psql -U <username> -d <database_name> -f database.sql

Run the Flask backend:

python backend/subot.py

Open index.html in a browser to access the chatbot.

Challenges Faced

Setting up Pgvector in PostgreSQL for vector-based similarity search.

Embedding Iterations: Ensuring accurate similarity matching.

LLAMA API Integration: Handling API-related issues.

User Query Limit Implementation: Restricting queries efficiently.

Chat History Management: Maintaining a continuous session-based history.

Feedback Handling: Collecting and categorizing responses for improvement.

Future Improvements

Expand database with more Sitare University-related data.

Integrate additional ML algorithms for better query classification.

Enhance response accuracy using advanced NLP models.

Improve chatbot UI for a more interactive experience.


License

This project is open-source and available under the MIT License.

GitHub Repository

Click here to access the repository

Thank you for exploring SU - Chatbot!

