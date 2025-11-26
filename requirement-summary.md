# Requirement summary documentation for the project:



## 1\. Problem Statement Summary



Build an MVP medical chatbot using Retrieval Augmented Generation (RAG) and a custom knowledge base.



Integrate both voice input/output and a “digital twin” visualization.



Use open-source LLM models (Hugging Face, Ollama, Llama, etc.), and showcase Python expertise.



Deliver supporting documents: requirements, HLD/LLD diagrams, database design, data flow and architecture diagrams, with a working demo in 2 days.



## 2\. High-Level Requirements



### Chatbot Functions:



Answer medical queries based on curated articles or datasets (not diagnostics).



Support both text and voice interactions.



Retrieve and reference knowledge base content using RAG.



Display/provide a basic “digital twin” (e.g., health profile visualization).



### Integration/Tech:



Open-source LLM for conversation and generation.



Vector database for knowledge retrieval.



Simple database for user sessions and logs.



Python for all core code, with clear modularization.



### Documentation Needs:



Detailed architecture diagram.



Data flow diagram.



Module/class design (LLD).



Database schema and design.



Rationale for all library/model choices, outlining pros and cons.



### Testing \& Demo:



Unit tests for data retrieval, inference, and pipeline.



### Working demo illustrating:



Text/voice query



Retrieval from knowledge base



LLM-generated response



Digital twin display



## 3\. Assumptions



Medical chatbot is for information only (not diagnostic or emergency use).



Knowledge base will consist of scraped medical articles/summaries.



Demo will cover end-to-end flow with basic UI/CLI, not full production quality.



## 4\. Core Feature List



RAG pipeline for knowledge-augmented responses.



Voice input (SpeechRecognition) and output (gTTS/pyttsx3).



Vector DB (FAISS/ChromaDB/Milvus) for information retrieval.



Digital twin: simulated patient profile visualization.



User/session tracking database (SQLite/PostgreSQL).



Supporting diagrams and documents.



Comprehensive README/setup notes.







NOTE:While the problem statement required both digital twin and voice capabilities, I chose to focus primarily on the digital twin and the core RAG chatbot system for this MVP. My main reason for this decision was time management: within the 2-day (20-hour) window, I prioritized building a robust pipeline—scraping real medical articles, indexing them for semantic search, integrating an open-source LLM, and adding multiple patient profile support through the UI.



I decided not to include live voice input/output features (such as speech-to-text and text-to-speech), mainly because these are best supported in a local Python environment and require additional packages, audio setup, and permissions that are not straightforward in an online notebook or web demo context. Given the complexity and my aim to deliver a working, end-to-end demo that highlights the retrieval, reasoning, and user context features, I felt that investing this time into a more solid RAG pipeline, UI, and multi-profile support would best demonstrate my Python and system design skills.



If more time or a local deployment environment were available, I would next add voice modules using SpeechRecognition and pyttsx3/gTTS so users can interact with the chatbot by speaking and listening. The code is modular and ready for this extension, and I have described the planned approach in my design notes.





