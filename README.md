# SU - Chatbot

## Introduction

We’re excited to introduce our new project, the **"SU - Chatbot"**!

This chatbot is designed to help anyone who wants to learn more about Sitare University. Whether you have questions or need information, SU-Chatbot is here to make it easy for you. We can’t wait for you to try it out!

### Purpose
The idea behind the **SU-Chatbot** is to assist people with their queries about Sitare University. Many students, especially those from underprivileged backgrounds, miss out on opportunities due to a lack of information. This chatbot aims to bridge that gap by providing easy access to university-related information.

> **Note:** Since Sitare University started in 2022, some details are still evolving, and the chatbot will improve as more data becomes available.

---

## Methodology

### Python Libraries Used

| Library              | Purpose  |
|----------------------|----------|
| **Flask**           | Backend framework for handling user requests, routing, and rendering templates. |
| **Psycopg2**        | Manages storing and retrieving data (embeddings, questions, answers) from a PostgreSQL database. |
| **SentenceTransformers** | Generates vector embeddings from text for clustering and similarity matching. |
| **NumPy**           | Performs numerical computations, including clustering and similarity calculations. |
| **SkLearn.cluster** | Used for clustering data. |
| **Pandas**         | Reads and analyzes data. |
| **Groq**            | API client for interacting with the LLaMA model, generating advanced natural language responses. |
| **Time**            | Implements user query limits, such as restricting attempts per account within a specified timeframe. |
| **Matplotlib**      | Visualizes graphs to show clusters based on user queries. |
| **Seaborn**         | Enhances graphs with better color schemes and professional visualization (built on Matplotlib). |

### Frontend Technologies

| Technology          | Purpose  |
|---------------------|----------|
| **HTML**           | Creates the structure and layout of the chatbot interface. |
| **CSS**            | Styles the chatbot for better visual appeal. |
| **JavaScript (JS)** | Used for interactive elements, such as password protection and star ratings. |

---

## Implementation Details

### **Frontend**

#### `Login_page.html`:
- Collects user data (ID and name) during login or signup.
- Includes a password-protected Admin button redirecting to `User_data.html` to display query-based graphs.

#### `Index.html`:
- Chat interface where users can ask questions.
- Displays query history and collects optional feedback on chatbot responses.

#### `User_data.html` (Admin Dashboard):
- Displays graphs of user query clusters, highlighting areas of interest or improvement.

### **Backend**

#### `pgvector_embedding.py`:
- Processes CSV files to generate vector embeddings and clusters.
- Stores embeddings and cluster data in the database for efficient similarity searches.

#### `subot.py`:
- Main file integrating all functionalities.
- Processes user queries by converting them into embeddings, finding similar clusters, and retrieving relevant answers.
- Sends responses to LLAMA for summarization before displaying to users.
- Implements query limits (10 queries/hour per user).

### **Database Tables**

| Table Name         | Purpose  |
|--------------------|----------|
| **qa_embeddings**  | Stores clusters, questions, answers, and embeddings for similarity-based searches. |
| **user_data**      | Tracks user queries and assigned clusters. |
| **Feedback**       | Records user feedback and star ratings. Responses with < 3 stars are flagged as false (`F`) and others as true (`T`) for database improvement using Naive Bayes classification. |

---

## Features

- **User Authentication:** 
  - Login/signup to collect and store user ID and name.
  - Password-protected Admin access to manage user data and view query analysis.

- **Interactive Chat Interface:** 
  - Users can ask questions and receive real-time responses.
  - Displays query history for the session.

- **Feedback Mechanism:** 
  - Users can like/dislike responses or provide feedback on suggested clusters.

- **Cluster-Based Query Analysis:** 
  - Each user query is assigned to a cluster based on vector similarity.
  - Helps identify user interests and areas for improvement.

- **Admin Dashboard:** 
  - Dedicated page for admins to view graphical representations of user queries.
  - Shows which clusters receive the most queries.

- **Efficient Query Processing:** 
  - Queries are converted into vector embeddings and matched with the nearest cluster.

- **LLAMA Integration:** 
  - Summarizes and refines chatbot responses using LLAMA (via Groq API).

- **User Query Limit:** 
  - Limits each user to **10 queries per hour**.

- **Data Visualization:** 
  - Graphs show the distribution of user queries across clusters to help improve chatbot knowledge.

---

## Results
- Graphs help identify user interest areas for improvement.
- User feedback helps refine chatbot responses.

---


## Challenges Faced

1. **Setting up Vector Extension in PostgreSQL** – Installed and configured `Pgvector` for efficient similarity searches.
2. **Handling Embedding Iterations** – Ensured accurate similarity matching.
3. **Integrating LLAMA API** – Faced API issues while implementing and fine-tuning.
4. **Implementing Limited User Attempts** – Required multiple trials to limit queries.
5. **Displaying Continuous Chat History** – Maintaining real-time chat history.
6. **Storing and Using User Data** – Mapping user queries to clusters and using feedback effectively.
7. **Debugging and Error Handling** – Fixed issues across frontend, backend, and database.

---

## Conclusion
This project demonstrates how **SU-Chatbot** can assist in answering queries related to Sitare University. By leveraging **LLaMA API** and structured data, it provides meaningful and helpful responses.

With continuous data collection and enhancements, **SU-Chatbot** will improve over time. Future updates may include additional ML algorithms and expanded datasets to refine its performance.

---

Thank you!!

