# Code Iterator AI – MVP

This project was originally built as a lightweight AI-powered assistant for game developers, designed to rewrite and optimize selected code snippets based on user prompts. It demonstrates an end-to-end working MVP that connects frontend, backend, and a local AI model.

## Objective

Build a code iterator AI tool (like Cursor) that:
- Accepts game code input from the user
- Accepts a natural-language prompt like "remove left movement" or "optimize for performance"
- Returns AI-modified code + explanation
- Allows users to apply the changes using an "Integrate Code" button


## MVP Features

- Accepts code input and prompt from the user
- Runs a local AI model or rule-based engine
- Generates modified code suggestions with explanation
- Integrates suggestion back into the UI with a click
- Designed to assist with game code workflows


## Tech Stack

    LAYER      STACK                               

  Frontend  -   HTML, CSS, JavaScript                 
  Backend   -  Python (Flask + Flask-CORS)           
  AI Model  -  locally hosted model or rule-based intent engine 

## Limitations of Open-Source Model Usage

While the full architecture was built to support AI-generated transformations, we encountered practical issues:

- Open-source models like CodeGen-2B are not fine-tuned for real instruction-following or prompt intent.
- Larger models (GPT-4, Claude, WizardCoder) were infeasible due to:
  - No available API key access
  - Local hardware resource constraints
- Fallback models (CodeT5, ReplitCoder) gave vague or repetitive output for code transformations


## Final Pivot: Playable Python Game to Simulate Prompt Actions

Since AI-generated suggestions were not consistent enough for submission, we shifted gears to build a functionally equivalent simulation:

- A Python game demo where a character named "GP" performs all the movements and in-game actions described in the prompts.

## GP Action Movement (Python Fallback)

This pygame based demo simulates:

- Left / Right / Up / Down movement  
- Jump, Slide, Crouch, Prone actions  
- Real-time action state detection  
- Color-based visual feedback  
- Console-based state labeling (e.g., “jumping”, “sliding”)

### Controls

  ACTION       KEY               

  Left       - A or ← Arrow     
  Right      - D or → Arrow     
  Up         - W or ↑ Arrow     
  Down       - S or ↓ Arrow     
  Jump       - Space            
  Slide      - Left Shift       
  Crouch     - Ctrl             
  Prone      - Z                


## How to Run the Full Project

 Code Iterator AI Tool (MVP)

 Step 1: Install dependencies
 pip install flask flask-cors transformers torch

 Step 2: Start backend server
 cd backend
 python app.py

 Step 3: Open frontend/index.html in browser
 Double click or open the index file in frontend

 step 4: Paste the original code of the game 
 In the prompt box, specify the changes
 Click Generate suggestion


Done by Pranay Gaddam
