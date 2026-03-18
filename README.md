# DIC2 — Grid World Value Iteration

An interactive reinforcement learning visualization tool focused on the **Value Iteration** algorithm. This project demonstrates finding the optimal policy in a stochastic Markov Decision Process (MDP) setting within a grid-based environment.

## 🚀 Overview

This application provides a visual representation of how the Value Iteration algorithm calculates state values ($V$) and derives the optimal policy ($\pi^*$). It is pre-configured with a specific scenario for demonstration purposes.

## 🛠️ Key Features

- **Algorithm Focus**: High-fidelity implementation of the **Value Iteration** algorithm.
- **Fixed Configuration**:
  - **Grid Size**: 5 × 5.
  - **Start Point**: Cell (0,0) (Top-Left).
  - **End/Goal State**: Cell (4,4) (Bottom-Right) with reward +1.0.
  - **Obstacles**: Strategically placed at (1,1), (2,2), and (3,3) to block the diagonal path.
- **Real-time Visualization**:
  - **Value Functions ($V$)**: Displays the calculated value for each state.
  - **Optimal Policy**: Displays arrows representing the best action to take in each cell.
  - **Optimal Path**: Distinctly highlights the best path from start to goal.
- **Dynamic Parameters**:
  - **Noise/Risk**: Adjust the probability of the agent sliding into unintended directions.
  - **Discount Factor ($\gamma$)**: Tune how much future rewards are valued.
  - **Step Cost**: Define the penalty for each movement to observe changes in behavior.
- **Premium UI/UX**:
  - Sleek, modern design with smooth transitions.
  - **Dark / Light Mode**: Easily switch themes via the button in the top-right corner.
  - Fully responsive layout.

## 💻 Tech Stack

- **Backend**: Python with Flask
- **Frontend**: Vanilla JavaScript, HTML5, Modern CSS (Glassmorphism & Flexbox)
- **Math**: Value Iteration (Bellman Optimality Equation)
- **Deployment**: Vercel ready

## 🏃 Getting Started Locally

### 1. Prerequisites
Ensure you have Python installed. Install the dependencies:
```bash
pip install flask gunicorn
```

### 2. Run the Application
Navigate to the project directory and run:
```bash
python api/index.py
```

### 3. Access the Grid
Open your browser and go to:
[http://127.0.0.1:5000](http://127.0.0.1:5000)

## ☁️ Vercel Deployment

This project is optimized for deployment on **Vercel**. 

1.  Push the code to GitHub.
2.  Import the project into Vercel.
3.  Vercel will automatically detect the `vercel.json` and `api/index.py` files.
4.  Standard Python 3 serverless environment is used.

## 📖 How It Works

1.  **Initialization**: Upon loading, the system pre-fills the 5x5 grid with specified start, end, and obstacle points.
2.  **Calculation**: The backend runs the Value Iteration algorithm until convergence.
3.  **Policy Extraction**: The optimal policy is extracted from the converged value function.
4.  **Path Tracing**: A path-tracing algorithm identifies the sequence of states from start to goal following the optimal policy.
5.  **Interactive Updates**: Adjusting the sliders in the UI will trigger an immediate re-evaluation on the server, allowing you to see how environment parameters affect the agent's strategy.
