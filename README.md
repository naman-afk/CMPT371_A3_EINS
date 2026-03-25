# CMPT371_A3_Eins(One)

- Course: CMPT371 - Data Communications & Networking
- Instructor: Mirza Zaeem Baig
- Semester: Spring 2026

Team Members
| Name | Student No. | Email |
|--------|-------------|-----|
| Cheng Yang Lai| 301550876 | cyl74@sfu.ca |
| Namandeep Kaur | 301553233 | nka87@sfu.ca |


## 1. Project Overview

### 1.1 Description
This project is a terminal-based multiplayer card game inspired by UNO, built using Python sockets.

The client handles user input, renders the interface, and communicates with the server using a simple JSON protocol.  
The server is responsible for managing turns, enforcing card rules, and controlling the overall game flow.

---

### 1.2 Architecture

#### Server
- Accepts player connections  
- Tracks and maintains game state  
- Validates player moves  
- Broadcasts updates to all connected clients  

#### Client
- Connects to the server over TCP  
- Renders the game interface using the Rich library  
- Sends player actions to the server  
- Handles card selection and wildcard suit selection  
- Displays end-of-game messages  

#### UI Layer
- Built using Rich Layout, Panels, and Text  
- Footer displays:
  - Player hand  
  - Wildcard suit selector  
- Displays win/lose game states  

---

### 1.3 Limitations

| Limitation | Suggested Solution |
|-----------|------------------|
| Each game starts fresh | Start playing to progress the game state |
| Cannot handle cases where the deck and discard pile are empty | Avoid excessive drawing and continue playing cards |
| Supports only 2–5 players (no AI support) | Rotate turns among players if more than 5 participants |
| Server continues running after a player quits or wins | Manually terminate the server when finished |

---

## 2. Demo Video

[Watch Demo on YouTube](https://www.youtube.com/watch?v=2-cLr3RGzUo)

---

## 3. How to Run

### 3.1 Prerequisites
- Python 3.10 or higher  
- Install dependencies:

```bash
pip install -r requirements.txt
````

---

### 3.2 Step-by-Step Guide

Ensure you are in the correct project directory before running commands.

#### 1. Start the Server

```bash
python server.py
```

* Enter the number of players when prompted

#### 2. Start the Clients

```bash
python client.py
```

* The game starts automatically once all players have joined

#### 3. Gameplay

* The current turn and top card are displayed and updated after each move

#### 4. Controls (During Your Turn)

* Up/Down Arrow Keys: Select a card
* Enter: Play selected card
* D: Draw a card
* Q: Quit the game

#### 5. Waiting

* If it is not your turn, wait for updates from the server

#### 6. Game End

* A win/lose message is displayed
* The game exits automatically

---

## 4. Academic Integrity & References
UI layout, rendering and Readme formatting, used ChatGPT. 
