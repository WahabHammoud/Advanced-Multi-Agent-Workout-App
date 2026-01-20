# Advanced-Multi-Agent-Workout-App
This project is a sophisticated multi-agent AI application developed to serve as a personalized fitness and nutrition assistant. It integrates multiple Large Language Models (LLMs) to handle specialized tasks, including routing, mathematical calculations, and personalized coaching.
Core Features
• Multi-Agent Routing: The system utilizes a conditional router to analyze user queries. If a question involves mathematics (such as calorie calculations), the router directs it to a specialized tool-calling agent equipped with a calculator to ensure precision. General inquiries are routed to an expert personal trainer persona.
• Retrieval-Augmented Generation (RAG): Using Astra DB as a vector database, the application stores and retrieves personal user notes—such as injury history or equipment limitations. This allows the AI to provide context-aware responses, like suggesting workout routines that specifically accommodate a user's unique physical constraints.
• AI-Powered Macro Recommendations: The assistant can dynamically generate nutritional targets (protein, calories, fats, and carbs) based on the user's biometric data (age, weight, height) and specific fitness goals, such as muscle gain or fat loss.
• Automated Vectorization: Leveraging the Astra Vectorize feature, the application automatically converts plain-text personal notes into vector embeddings during ingestion, streamlining the search and retrieval process.
Technical Stack
• Frontend: Streamlit provides an interactive Python-based UI for profile management and real-time AI interaction.
• AI Orchestration: Langflow is used as a low-code visual editor to design complex AI workflows and manage API endpoints.
• Database: Astra DB (by Data Stacks) serves as the serverless vector-capable database for high-performance data storage and similarity search.
• Models: Built with support for OpenAI (e.g., GPT-4) and flexible enough to integrate local models via Ollama.
• Backend Logic: Fully implemented in Python, utilizing environment variables for secure management of API tokens and database credentials.
How It Works
The application bridges a Streamlit frontend with a Langflow backend. When a user asks a question, the system searches Astra DB for contextually relevant notes, combines them with the user’s biometric profile, and routes the data through the optimal AI agent to generate a precise, personalized response
