## About 
<P>Term: Fall 2025
<P>Team: GenMuse
<P>Students: Veda Prakash Chiliveru, Pavan kumar Sunkara, Shyam Kumar Challa, Sai Siddu Vardhan Reddy Annadi

# GenMuse – StoryForge AI System  
### Comprehensive Project Report

---
<img width="1728" height="2304" alt="Do Your Research (1)" src="https://github.com/user-attachments/assets/7075fc2c-6ff4-48cf-93e7-d01bec6410ae" />



## 1. Introduction.

 The development of complex language models has altered the landscape of creative storytelling, allowing automated systems to produce rich storylines, characters, and worlds with remarkable coherence.  As more creators incorporate AI into literature, filmmaking, game design, and interactive media, the demand for customisable and locally deployable model architectures has increased substantially.

**The StoryForge - Mistral Narrative Generation Package is a comprehensive**, self-contained toolset for implementing a high-performance storytelling AI model.  This package includes all of the necessary components—model weights, tokeniser files, configuration settings, and runtime assets—for running and fine-tuning a Mistral-based Large Language Model for narrative building.
 
---

## 2. Problem Statement

Traditional storytelling tools present several challenges:

- Difficulty in maintaining narrative consistency across long stories  
- Time-consuming process to structure stories into scenes and plots  
- Manual effort involved in world-building and character design  
- Existing generators produce unstructured text that is hard to edit  

There is a need for a system that generates creative content while organizing it into a structured, editable, and context-aware format.

---

## 3. Project Objectives

- Build an intelligent AI engine for high-quality story generation  
- Enable structured, scene-based storytelling  
- Provide tools for character creation, world-building, and timelines  
- Support multimedia outputs in future versions  
- Deliver smooth, real-time editing  
- Help creators turn ideas into complete stories efficiently

---

## System Overview

StoryForge Pro (GenMuse) operates as a fully modular, end-to-end AI storytelling platform designed to support ideation, narrative development, scene-based editing, and long-form story management. Its architecture separates concerns cleanly across frontend, backend, data, and AI orchestration layers—ensuring flexibility, scalability, and ease of integration.

At a high level, the platform consists of the following core components:

### Node.js + Express Backend

The backend serves as the central processing layer that manages prompt construction, AI requests, response handling, and story state management. It orchestrates:

Model invocation via the Mistral API (AI Layer)
Scene creation, rewriting, and expansion pipelines
Story, character, and timeline management utilities
REST API endpoints for frontend interaction
Session and state persistence using in-memory storage

### Mistral API (AI Layer)

The Mistral API functions as the narrative engine responsible for intelligent text generation. It performs:

Scene and story generation based on user prompts
Context-aware dialogue and narrative continuation
Character and world description synthesis
Output formatting into structured text (JSON/TXT)

### React + Vite + TailwindCSS Frontend

The frontend provides an interactive workspace that empowers users to design and refine their stories. It enables:

Scene-by-scene story editing and management
Character and world-building tools
Timeline and structure organization
Output export and preview utilities
API communication through Axios
LocalStorage-based user session handling

### Data Layer (In-Memory + LocalStorage)

The platform uses a lightweight in-memory store on the backend and LocalStorage on the frontend for quick, session-based operations.
This allows for:

Fast story editing and regeneration
Temporary state and scene caching
Seamless story updates without a full database dependency
These components together support smooth story creation, editing, and management.

---

## 5. Methodology

The StoryForge Pro (GenMuse) platform implements a lightweight, modular methodology centered on AI-assisted narrative design, scene-based story management, and Mistral-powered creative generation. Its workflow is optimized for flexibility, transparency, and speed across both frontend and backend layers.

### 5.1 Story Generation Workflow

StoryForge Pro employs an iterative pipeline integrating user intent, contextual retrieval, and AI-driven narrative construction:

1. User Input
Writers initiate a project through the React + Vite interface, providing ideas, themes, or partial scenes for continuation.

2. Backend Processing
The Node.js + Express backend interprets requests, assembles prompt payloads, and manages model parameters. It serves as the orchestration layer between user actions and the AI model.

3. AI Request Handling
Requests are forwarded to the Mistral API (AI Layer) for content generation. The model produces structured scene output, dialogue, and contextual expansion based on supplied prompts.

4. Response Handling & Display
The backend formats AI responses (JSON/TXT) and sends them via REST API calls to the frontend, where the editor updates the scene view dynamically.

5. Session Memory and Storage
For rapid prototyping, session data and short-term results are stored in LocalStorage. A lightweight in-memory store supports runtime coherence; future versions may integrate FAISS or Chroma for persistent vector memory.

### 5.2 Scene-Based Editing

StoryForge Pro structures each narrative as an ordered set of independent scenes, enabling users to edit, rewrite, or regenerate content without disrupting global coherence.
This modular framework allows:

Targeted scene-level iteration
Rapid regeneration or rewriting
Non-linear scene organization
Smooth conversion to screenplay format

### 5.3 Character and World-Building

Dedicated panels in the interface enable creation of:
Character Profiles (traits, goals, relationships)
World Elements (locations, lore, events)
Timelines for tracking narrative continuity

These data elements enrich AI-generated text and maintain consistent tone and context across multiple scenes.

### 5.4 Frontend Interface

Built with React, Vite, and TailwindCSS, the interface provides an intuitive workspace comprising:
Story workspace and editor
Scene list and narrative map
Character and world-building modules
Timeline organizer
Export tools for screenplay and text


---

## 6. System Architecture


<img width="2304" height="1728" alt="image" src="https://github.com/user-attachments/assets/93650cf3-ca62-4b10-9b2d-5aa831b493f9" />


## 7. Tech Stack

- Frontend: React, Vite, TailwindCSS  
- Backend: RestAPI, Python  
- AI Models: OpenAI GPT, LLaMA, Mistral, Phi  
- Vector Database: FAISS or Chroma  
- Database: SQLite or PostgreSQL  
- Additional: WebSockets, Axios, JWT Authentication (optional)

---

## 8. Implementation Details

### 8.1 Backend

Built with Node.js + Express
RESTful API endpoints for scene and story management
Middleware for logging, CORS, and environment configuration (dotenv, morgan)
Modular route handling for story generation, updates, and data retrieval
Communication with Mistral API for text generation and rewriting
Lightweight in-memory session management for active stories

### 8.2 Frontend

Developed using React + Vite + TailwindCSS
Modular React components for scenes, characters, and world-building
Dynamic scene navigation and editing interface
Real-time content updates from API responses
Axios used for REST communication with the backend
LocalStorage support for saving session data and quick reloads

### 8.3 Data Storage

In-Memory Data Store for temporary backend state

LocalStorage for client-side caching and quick session recovery

Optional persistence layer (future upgrade):
SQLite or PostgreSQL for structured story data
FAISS or Chroma for vector-based retrieval


Current storage entities include:

Story – overall narrative metadata
Scene – modular narrative segments
Character – personality traits, relationships
World – environmental and lore information
Timeline – sequence of events or chapters

### 8.4 AI Integration Pipeline

Receive user prompt or scene input from the frontend
Construct and format the request payload in the backend
Send API request to the Mistral model
Receive AI-generated text, structured and formatted (JSON/TXT)
Send formatted response back to the frontend for display and editing

---

## 9. Use Cases

- Scriptwriting for films  
- Novel development  
- Game narrative design  
- World-building for fantasy and sci-fi  
- AI research and creative writing tools  
- Interactive storytelling apps

---

## 10. Future Enhancements

- AI image generation  
- AI voice narration  
- Collaborative multi-user writing  
- Full version history and revision tracking  
- Automated storyboarding  
- Mobile app version  
- Advanced publishing integrations 

---

## 11. Results and Evaluation

GenMuse demonstrates:
- High-quality, coherent narrative generation
- Strong consistency supported by scene- and story-level memory
- Efficient workflows designed for creative writers
- Flexible integration with multiple language models
- A professional, structured interface suitable for writing tasks

Feedback shows that the system reduces time and effort in creating structured narratives and enhances overall creative flow.


---

## 12. Conclusion

GenMuse – StoryForge AI System provides a modern and efficient approach to AI-assisted storytelling. By integrating language models, memory-enhanced workflows, structured scene editors, and creative support tools, the system streamlines the writing process and enables faster, smarter, and more organized narrative creation.

It establishes a strong foundation for future innovations in multimedia story generation and collaborative creative platforms.


### 👩🏻‍💻🧑🏻‍💻 Collaborators

[//]: # ( readme: collaborators -start )
<table>
<tr>
    <td align="center">
        <a href="https://github.com/digitaldiv">
            <img src="https://avatars.githubusercontent.com/u/1842870?v=4" width="100;" alt="Div Pithadia"/>
            <br />
            <sub><b>Div Pithadia</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/chargershub">
            <img src="https://avatars.githubusercontent.com/u/160267476?v=4" width="100;" alt="Chargers hub"/>
            <br />
            <sub><b>Chargers Hub</b></sub>
        </a>
    </td></tr>
</table>

[//]: # ( readme: collaborators -end )











