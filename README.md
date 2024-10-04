# Flipkart Chatbot

A Retrieval-Augmented Generation (RAG) based chatbot that provides product recommendations and answers customer queries using product reviews from the Flipkart platform.

![Architecture diagram](image_url_or_path)


## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Components](#components)
- [Contributing](#contributing)
## Overview

This project aims to develop an intelligent chatbot that leverages product reviews to answer customer queries and recommend products effectively. It utilizes LangChain for embedding generation, AstraDB for vector storage, and ChatGroq for natural language processing.

## Architecture

The architecture of the Flipkart Chatbot consists of several key components that interact to provide an efficient user experience. Here’s a conceptual flow of how the components work together:

1. **Data Ingestion**: Load the Flipkart reviews dataset, dropping unnecessary columns.
2. **Document Conversion**: Convert reviews into a structured document format.
3. **Embedding Generation**: Generate vector embeddings using the HuggingFace model.
4. **Vector Store**: Store embeddings in AstraDB for efficient retrieval.
5. **Model Setup**: Use ChatGroq for generating responses based on user queries.
6. **Retrieval and Question Processing**: Fetch relevant documents and contextualize user questions.
7. **Question-Answer Chain**: Generate responses based on retrieved documents and user input.
8. **Chat History Management**: Manage session-based chat history for dynamic interactions.

   
## Installation

To set up the project, follow these steps:

1. Clone the repository and install the required dependencies:

   ```bash
   git clone https://github.com/VivekSuryavanshi03/Flipkart-Chatbot.git && cd flipkart-chatbot && pip install -q langchain langchain-community langchain-astradb langchain-groq pypdf sentence_transformers

## Usage
-ingtration with flask

## Components

- **Data Processing**: Load and preprocess the Flipkart reviews dataset.
- **Document Management**: Convert reviews into the `Document` format suitable for RAG.
- **Embedding Generation**: Utilize HuggingFace embeddings for semantic understanding.
- **Database Integration**: Use AstraDB for storing and retrieving vector embeddings.
- **Natural Language Processing**: Implement ChatGroq to handle user queries and generate responses.
- **Session Management**: Keep track of user sessions and chat history for context-aware responses.


## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please submit a pull request or open an issue to discuss your ideas. Your input is valuable to the project!




### Visual Representation

```plaintext
            +-----------------------+
            |  User Input (Query)   |
            +----------+------------+
                       |
                       v
            +-----------------------+
            |  Session Management    |
            +----------+------------+
                       |
                       v
            +-----------------------+
            |  Retrieve Relevant     |
            |   Documents (Vector    |
            |        Store)          |
            +----------+------------+
                       |
                       v
            +-----------------------+
            |   Question Processing   |
            |   (Contextualization)  |
            +----------+------------+
                       |
                       v
            +-----------------------+
            |   Response Generation   |
            |   (Question-Answer     |
            |        Chain)          |
            +----------+------------+
                       |
                       v
            +-----------------------+
            |     User Response      |
            +-----------------------+

