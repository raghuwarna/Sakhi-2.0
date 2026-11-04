metadata
title: Sakhi 2.0
emoji: 🤝
colorFrom: green
colorTo: blue
sdk: docker
pinned: false
Sakhi 2.0 – AI-Powered Government Scheme Assistant
Making Indian Government Schemes Easier to Understand.

Sakhi 2.0 is an independent AI research project developed by Raghuwarna Erugurala. It aims to make information about Indian government schemes easier to discover and understand through natural-language interactions.

The project uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from government scheme documents and generate answers grounded in the available sources.

🌐 Live Application
Try Sakhi 2.0:
https://huggingface.co/spaces/ergurala-raghuwarna07/sakhi-2-0

Current Release: Public English-language prototype.

✨ Key Features
Natural-language question answering about Indian government schemes.
Retrieval from a collection of government scheme documents.
Source references accompanying generated answers.
Insufficient-evidence handling to reduce unsupported answers.
Off-topic question handling.
Voice input through browser speech recognition.
Read-aloud functionality for assistant responses.
Local chat history stored in the user's browser.
🏗️ Project Architecture
Sakhi 2.0 follows a frontend–backend architecture.

Component	Technology
Frontend Hosting	Hugging Face Spaces
Backend API	Cloudflare Workers
Database	Cloudflare D1
Retrieval	D1 Full-Text Search (FTS5)
Frontend	HTML, CSS, JavaScript
AI Architecture	Retrieval-Augmented Generation (RAG)
How It Works
The user submits a question through the Sakhi interface.
The frontend sends the question to the backend API.
The backend retrieves relevant passages from the scheme database.
Retrieved information is used to generate an answer.
The response and available source references are returned to the frontend.
If sufficient evidence is unavailable, Sakhi can return an insufficient-evidence response.
📚 Dataset and Knowledge Base
The research dataset was prepared from Indian government scheme PDF documents.

Dataset Statistics
Description	Count
Original PDF collection	2,876
Unique document contents	2,066
Extracted pages	2,894
Final processed chunks	11,023
Chunking Configuration:

Maximum chunk size: 500 tokens
Chunk overlap: 75 tokens
The project also explored multilingual embedding-based retrieval using intfloat/multilingual-e5-small.

The current deployed backend uses Cloudflare D1 Full-Text Search. The embedding-based experiments are not currently part of the deployed retrieval pipeline.

🛡️ Responsible Answering
Sakhi 2.0 is designed to:

Ground responses in retrieved government scheme information.
Provide source references where available.
Avoid presenting unsupported information as verified facts.
Return an insufficient-evidence response when relevant information cannot be found.
Handle unrelated questions appropriately.
⚠️ Current Release Limitations
The currently deployed application supports English responses.
Hindi, Telugu, Tamil, Kannada, Malayalam and Marathi support are planned research directions, not completed deployed features.
Answer quality depends on the availability and accuracy of indexed documents.
Sakhi is an informational assistant, not an official government service.
Users should verify important eligibility conditions, financial benefits and application procedures using official government sources.
Chat history is stored locally in the browser and is not server-side conversational memory.
🚀 Future Development
Planned research and development directions include:

Multilingual support for Indian languages.
Cross-language information retrieval.
Multilingual voice-based interactions.
Improved retrieval relevance and multi-scheme discovery.
Expanded evaluation of answer accuracy and citation coverage.
Further improvements to accessibility and usability.
🧰 Technology Stack
Python
Retrieval-Augmented Generation (RAG)
Natural Language Processing (NLP)
Hugging Face
Cloudflare Workers
Cloudflare D1
HTML, CSS and JavaScript
FAISS
Sentence Transformers
👨‍💻 Developer
Raghuwarna Erugurala

Independent AI Research Project

GitHub: https://github.com/raghuwarna
LinkedIn: https://www.linkedin.com/in/ergurala-raghuwarna/
Building accessible AI-powered solutions for public information discovery.
## Documentation

- [System Architecture](docs/architecture.md) – Understand Sakhi 2.0's architecture, components, database, AI model, and request workflow.
## License

Copyright © 2026 Raghuwarna Erugurala. All rights reserved.

This repository is publicly available for viewing and educational reference. No permission is granted to copy, modify, redistribute, or use this project commercially without prior written permission from the author.
