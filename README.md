# AI Fashion Search Engine (Lookr.fyi)

[![Azure Cloud](https://img.shields.io/badge/Cloud-Azure-0089D6?logo=microsoft-azure&logoColor=white)]()
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&logoColor=white)]()
[![RAG](https://img.shields.io/badge/Architecture-Hybrid%20RAG%20⚡-F59E0B)]()
[![Multimodal](https://img.shields.io/badge/AI-Multimodal%20Search-6D28D9)]()
[![LLMs](https://img.shields.io/badge/LLMs-OpenAI-0EA5E9)]()

An advanced AI-driven search engine designed to connect fashion suppliers and buyers through intelligent search and conversational interaction. This system leverages Large Language Models (LLMs) and Hybrid Multimodal Retrieval-Augmented Generation (RAG) to find and rank fashion products based on user queries, overcoming challenges related to keyword variations, image mismatches, and customization needs.

## 📁 Repository Details

This repository contains the documentation and architecture overview to showcase the project's functionality.

*Note*: The source code is not publicly available but can be demonstrated upon request.

## 🎯 Problem Statement

Fashion suppliers often use keyword-stuffed titles (e.g., "summer polyester floral casual woman") that do not align with how buyers actually search (e.g., "boho chic dress for a beach wedding"). Additionally, images may not always convey the specific product features a buyer seeks. Our goal was to build a system that understands both the *text* and the *image* pixels to bridge this gap.

## 💡 Solution

We developed a **Multimodal AI Search Engine** on Azure that:

- Allows users to converse with the search engine to refine queries and find the most relevant products.
- Bridges the communication gap between suppliers and buyers by understanding natural language queries and product descriptions.
- Supports multimodal search, integrating text, image, and vector-based search for comprehensive product discovery.
- Enables efficient supplier onboarding, helping them list their products with optimized searchability.

## 🎥 Demo

![Demo Video](demo.gif)

## 🔑 Key Features

- **Hybrid Multi-modal RAG**
  - Keyword + Image + Text Vector search running in parallel
  - Intelligent ranking based on query relevance
  - Conversational interface for refined search

- **Smart Product Discovery**
  - Natural language understanding
  - "Visual-like" search using text queries.
  - Intelligent supplier-buyer matching

- **Technical Implementation**
  - Hybrid retrieval pipeline combining BM25, CLIP text-image similarity, dense text embeddings, and RRF for ranked fusion.
  - Scalable data infrastructure using Cosmos DB (metadata + vectors), Blob Storage (images), and Azure Functions for serverless APIs.
  - Fashion-tuned CLIP embedding models deployment and serving via Azure ML
  - LLM-powered capabilities: query rewriting, attribute extraction (color, fabric, style), and conversational refinement.
  - Azure Promptflow for orchestration with structured logging

- **Microservices-Based Architecture**
    - Azure Functions for handling API logic.
    - Cosmos DB for managing structured product data.
    - Blob Storage for storing and retrieving product images.
    - Vector Search to enhance relevance ranking and retrieval.

- **Seamless Deployment and Performance Optimization**
    - Fully managed on Azure Cloud, ensuring high availability and real-time response.

## 🏗️ Architecture

![Architecture Diagram](Architecture.png)


## 🛠️ Technology Stack

- **Core:** Python, Azure PromptFlow
- **Search & Data:** Azure AI Search, Azure Cosmos DB (NoSQL), Blob Storage
- **ML**: HuggingFace Models, Azure ML, Azure OpenAI
- **Infrastructure:** Azure Functions (Serverless), Docker
## 💫 Impact

- Enhanced product discovery accuracy
- Improved supplier-buyer communication
- Streamlined onboarding process
- Efficient customization requirement matching

## Evaluation Metrics

- **35% increase** in Recall@10 metrics & **15% increase** in NDCG@10 (ranking quality) by choosing CLIP-based fashion embedding models after benchmarking multiple candidates.
- Reduced vector search time from 5.7s -> 3s
- Curated evaluation dataset of text-image and text-text pairs using Labelstudio

## 🚀 Deployment

The system is fully deployed on Azure with:
- Scalable microservices architecture
- Robust logging system
- Efficient vector storage
- Optimized search functionalities

## 🔄 Development Workflow

1. User query processing
2. Multi-modal search execution
3. Result ranking and filtering
4. Conversational response generation
5. Continuous feedback integration

---


*Note: This project was developed as part of a US-based startup initiative where I served as a Machine Learning Engineer.*