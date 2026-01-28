# LLM Game Quality Analyzer

The LLM Game Quality Analyzer is an AI-driven system designed to transform scattered, unstructured game reviews into structured, decision-ready insights. The vision of the project is to aggregate player feedback from platforms such as Reddit, YouTube, Twitch, Twitter (X), and Steam, apply NLP and LLM-based analysis, and surface transparent, data-driven scores across key dimensions like gameplay, story, visuals, and action.

The motivation behind this project is simple:

- Gamers are forced to sift through hundreds of biased or fragmented reviews before making a purchase  
- Developers struggle to extract clear, objective signals from noisy, emotional feedback  
- Existing review platforms lack a holistic, data-backed view across sources  

This system cuts through that noise by unifying reviews, extracting sentiment and themes, and presenting them as interpretable scores and summaries.

This repository currently implements the Reddit ingestion, preprocessing, and UI prototype layers of the pipeline.

## What This Repo Contains

The notebooks and scripts in this repository:

- Collect Reddit posts and comments using the Reddit API  
- Normalize and clean raw text using Python (regex, pandas)  
- Filter low-quality or irrelevant content  
- Structure records for downstream storage and analysis  
- Support insertion into MongoDB and PostgreSQL  
- Feed processed data into a lightweight UI layer  

These components form the data engineering foundation of a larger system designed to support:

- Multi-source ingestion (YouTube, Twitch, Steam, Twitter)  
- LLM-based relevance filtering  
- Sentiment analysis and topic modeling  
- Hierarchical summarization using RAG  
- Dimension-wise scoring of games  
- A product-grade frontend for users  

## Frontend (UI Layer)

The project includes an early-stage UI prototype that demonstrates how insights are consumed by end users. The interface is designed to:

- Display game-level scores across gameplay, story, visuals, and action  
- Present AI-generated summaries derived from Reddit discussions  
- Act as the product surface for the ML pipeline  

The UI is implemented as a lightweight Python application (Streamlit-style workflow) that reads processed outputs and renders them in a clean, user-facing format. While the current implementation focuses on Reddit as the primary source, the UI establishes the end goal of the system: turning raw, unstructured community discourse into interpretable, decision-ready signals.

## Use Cases

For Gamers  
- Compare games quickly using objective, data-driven scores  
- Understand strengths and weaknesses without reading hundreds of reviews  
- Make faster, more informed purchase decisions  

For Developers & Publishers  
- Identify recurring pain points and feature requests  
- Track sentiment trends post-launch  
- Inform patch priorities, marketing, and sequel design  

For Platforms & Media  
- Generate AI-driven review content  
- Offer premium analytics and dashboards  
- Monetize insights via subscriptions or partnerships  

## Project Vision

This system is designed as a modular, scalable ML pipeline:

1. Ingest data from multiple platforms  
2. Clean and normalize unstructured text  
3. Filter noise using LLM-based relevance models  
4. Extract sentiment and themes  
5. Summarize long-form discourse using RAG  
6. Convert insights into transparent, dimension-wise scores  
7. Surface results through a simple, product-grade UI  

This repository represents the data ingestion and presentation layers of that architecture, starting with Reddit as the primary source and a prototype interface to demonstrate end-to-end value.