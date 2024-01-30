AI-Quest
========

**Made by Jingxi Li, Priyansh K. Shah, Leon Ouyang**

Generate, talk, and interact with your own character, powered through AI!

How to Use:
-----------

*   Write into the top text field describing the characteristics you want your character to have.
*   Engage in conversation through the bottom text field input or via microphone.

Technologies Used
-----------------

We built the front-end using HTML, CSS3, React, and Next.js. It takes text and audio prompts and displays output from our back-end. The back-end is powered by the llama\_index (LLM framework) and leverages various AI techniques and models for character generation.

Back-end Technologies:
----------------------

*   **LLM Framework**: Provides the foundation for the back-end AI processing.
*   **Google Gemini Pro**: Enhances character performance through retrieval augmented generation.
*   **ReAct Prompting and Chain-of-Thought Prompting**: Techniques used for generating character responses.
*   **Whisper (Speech to Text AI)**: Converts speech input to text.
*   **ElevenLabs (Text to Speech AI)**: Converts AI-generated text to speech.
*   **Gemini and Wikipedia Dataloaders**: Fetch information from Wikipedia to enrich character knowledge.
*   **ChromaVectorStore and VectorStoreIndex**: Tools for efficient storage and retrieval of character data.

Front-end Technologies:
-----------------------

*   **HTML, CSS3, React, Next.js**: Used to create an interactive user interface for entering prompts and receiving character responses.

How to Run
----------

To run the application, follow these steps:

1.  Install the required Python packages using the command: `pip install -r requirements.txt`
2.  Install the required Node.js packages for the front-end using: `npm install`
3.  Run the FastAPI back-end using: `uvicorn main:app --reload`
4.  Start the front-end development server using: `npm run dev`

Backend Code Snippet
--------------------


`import random from fastapi import FastAPI from fastapi.middleware.cors import CORSMiddleware from pydantic import BaseModel from fastapi import HTTPException, Form from character import Character import io import json import whisper  # Additional code...`

Frontend Setup
--------------

1.  Navigate to the `frontend` directory using the command: `cd frontend`
2.  Install the required Node.js packages: `npm install`
3.  Start the development server: `npm run dev`

**Note:** Ensure you have the required dependencies installed, including the llama\_index and other AI-related packages.

Dependencies
------------


`import llama_index from llama_index.llms import Gemini from dotenv import load_dotenv from llama_index.vector_stores import ChromaVectorStore from llama_index.storage.storage_context import StorageContext import llama_hub from llama_index import download_loader import json from llama_index import ServiceContext from pathlib import Path from llama_index import (     SimpleDirectoryReader,     VectorStoreIndex,     StorageContext,     load_index_from_storage, ) from langchain_google_genai import GoogleGenerativeAIEmbeddings from llama_index.tools import QueryEngineTool, ToolMetadata from llama_index.agent import ReActAgent from llama_index.tools.tool_spec.load_and_search.base import LoadAndSearchToolSpec from llama_hub.tools.wikipedia import WikipediaToolSpec  # Additional dependencies...`

**Important Note:** Make sure to set up the required environment variables and configurations specified in the `.env` file.

Feel free to reach out if you encounter any issues or have questions!