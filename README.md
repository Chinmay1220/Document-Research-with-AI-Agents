# Automated Research Workflow with AI Agents

**Project Overview :** 
The goal of this project is to create a cutting-edge, automated pipeline for document parsing, vector storage, and AI-powered research capabilities, providing an integrated solution for efficient document analysis and dynamic knowledge retrieval. This system utilizes Docling for sophisticated document parsing, Pinecone for scalable vector storage and fast, similarity-based search, and Langraph for building an intelligent multi-agent research ecosystem. A user-friendly interface, powered by Streamlit or Coagents, enables seamless interaction with the system, allowing users to conduct in-depth research, ask context-specific queries, and receive real-time, AI-enhanced responses. The system aims to revolutionize the research workflow by offering both speed and accuracy, delivering tailored insights while supporting advanced retrieval-augmented generation (RAG) for more meaningful and contextually rich interactions. This solution is designed to handle large-scale datasets and provide a scalable, interactive research platform, optimizing the way users search and explore complex information.


**Key Technologies :**

Python, VS code, Streamlit, OpenAI, CodeLabs, Git, Copilot, Airflow, Docling, Pinecone, Langraph, AWS, Docker, Git


**Desired Outcome or Solution :**

Automated Document Parsing: Used tools like Docling to parse raw documents into structured formats automatically.
Efficient Vector Storage: Stored the parsed document vectors in a scalable and high-speed storage system, such as Pinecone, to enable similarity-based search.
Multi-Agent Research System: Leveraged Langraph to build a research system with agents for document querying, external web searches, retrieval-augmented generation (RAG), and more. These agents will work collaboratively to provide well-rounded insights.
Interactive Interface: Developd a user-friendly platform using Streamlit or Coagents that allows users to interact with the data, ask questions, and save findings.
Professional Output: Enabled the export of research results into templated professional PDF reports and structured formats like Codelabs for future reference.

Components Overview:

Document Parsing and Vector Storage
Multi-Agent Research System
Interactive Research Interface
Pipeline Automation and Deployment

Tools and Technologies:

AWS S3: Storage for images and PDFs from CFA publications.
Airflow: Pipeline automation and scheduling.
FastAPI and Streamlit/Coagents: Frontend for user interactions.
Docker and Docker Compose: For containerization.
Python and Dependencies (TOML managed): Backend scripting and AI integrations.
NVIDIA Embeddings and OpenAI: For summaries and document embeddings.
FAISS and Llama Index: For vector storage and indexing.
Docling: For document parsing and structured data extraction.
Pinecone: Vector database for scalable and fast similarity search.
Langraph: Multi-agent system for document retrieval, web search, and query answering.
OpenAI Models: For question-answering and retrieval-augmented generation (RAG)

Client-Facing Application

Code and Components
Document Parsing, Vector Storage, and Pipeline Setup

Defines the Airflow pipeline for automating document parsing using Docling and vector storage in Pinecone.
Automates the extraction of text and structured information from the dataset and stores it in Pinecone for fast retrieval.

Script that uses Docling to parse the documents and extracts structured text for storage.

Script to upload parsed document vectors to Pinecone for scalable vector-based search.

Defines the workflow in Airflow for scheduling and triggering document parsing, vector storage, and indexing processes.
Research Agent with Pinecone and Langraph


Configures the use of Pinecone for vector storage and retrieval, and Langraph to build the multi-agent system.

Agent Functions:
Search for relevant research papers from Arxiv.
Conducts online research for broader context and context expansion.
Retrieves answers to queries based on document content from Pinecone using Langraph.
Research Interface and Q/A Interaction

Streamlit Interface:
A Streamlit-based interface for user interaction. Users can ask questions on documents, and the results from Pinecone and Langraph agents are displayed.
Allows users to ask 5-6 questions per document and saves the session results.

Export Results:
Generates a professional PDF report based on the user's session, including the answers to their questions and insights.
codelabs_export.py: Structures research findings in a Codelabs format for instructional clarity.

Client-Facing Application

Components

Pinecone Endpoints:
Users interact with the Pinecone vector database to search and retrieve documents or document segments.
Langraph Multi-Agent Setup:
Allows multiple agents (such as Arxiv Agent, Web Search Agent, and RAG Agent) to query documents stored in Pinecone and interact with the user for research.
Code and Modules

Handles API calls related to the agent system, processing questions, querying Pinecone, and retrieving answers using Langraph.
Contains the core logic for interacting with users, processing their input, and managing agent responses.
The frontend interface that allows users to browse, select documents, ask questions, and view answers. Provides a streamlined interface for interacting with the agents.

Research Notes Indexing and Search
Functionality

Incremental Indexing and Storage:

Research notes are generated through the RAG Agent based on user input and indexed using Pinecone for fast and efficient similarity search.
Search Capabilities:

Users can search the documents and research notes for detailed insights. Query results include both full documents and indexed research notes, offering enhanced relevance.
Approach

Pinecone for Vector Search:
A highly efficient search engine that enables similarity search using vectors.
Langraph for Managing Agents:
Manages indexing and agent-based research queries. Each agent helps to search and extract information from documents.
Deployment and Accessibility
Setup

Containerization:

Docker containers are used to deploy the FastAPI backend and Streamlit frontend, ensuring easy scalability and maintenance.
Docker Compose:

docker-compose.yml: Defines multi-container deployment for managing communication between backend services (FastAPI) and frontend services (Streamlit).
Cloud Deployment on AWS EC2:

Hosted on AWS EC2 for scalable cloud-based access to the API and the user interface.

Docker Configuration

Dockerfile for FastAPI: Builds the container image for FastAPI backend.
Dockerfile for Streamlit: Builds the container image for the Streamlit frontend.
docker-compose.yml: Manages the deployment and orchestration of multiple services, ensuring they run and communicate effectively.

Access and Testing
Access URL

Streamlit Interface: http://<ec2-ip>:8501
FastAPI Documentation: http://<ec2-ip>:8000/docs
Coagents : http://<ec2-ip>:3000

Testing Scenarios

Verify Data Ingestion: Test the process of data scraping, document parsing, and vector upload to Pinecone. Ensure that all documents are indexed correctly.

Interactive Querying and Summarization: Validate that the Streamlit app properly handles user input for questions and that Pinecone and Langraph agents are retrieving relevant information.

Search Accuracy: Test the precision and recall of searches in Pinecone for indexed research notes and document content.

Challenges and Future Enhancements

Handling Large-Scale Data

Scaling Pinecone and Docling for larger document datasets.
Optimizing Langraph agents for large-scale, multi-agent environments.
Enhanced Question-Answering (QA) Capabilities

Improving the contextual understanding and relevance of the answers by refining the RAG Agent with more advanced embeddings and retrieval techniques.
User Authentication

Implementing secure access control and authentication to ensure only authorized users can access sensitive research data and documents.
Performance Optimization

Optimizing vector search and retrieval times as the dataset grows in size and complexity.

**Architecture diagram :**

![image](https://github.com/user-attachments/assets/74ab661c-9878-4c81-8453-e8df3956dac1)


**Contribution :**

WE ATTEST THAT WE HAVEN’T USED ANY OTHER STUDENTS’ WORK IN OUR 
ASSIGNMENT AND ABIDE BY THE POLICIES LISTED IN THE STUDENT HANDBOOK


**Documentation files Team_9** 

**Code labs** - https://codelabs-preview.appspot.com/?file_id=1L8iGLikZFFtgpO4CdBcP4Ngjyye7NBj-hNxbv665eo0#0

**Google Doc** - https://docs.google.com/document/d/1L8iGLikZFFtgpO4CdBcP4Ngjyye7NBj-hNxbv665eo0/edit?tab=t.0

**Video** - https://drive.google.com/drive/folders/1lrJaOTC_vUS99GX806M4zyhHooGAdQDF?usp=drive_link

**Web Link** - http://10.110.71.35:8502

