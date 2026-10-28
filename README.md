
# **AI-Agents-for-Medical-Diagnostics**

## **Project Description**

The **AI-Agents-for-Medical-Diagnostics** project leverages machine learning and artificial intelligence agents to analyze medical reports and generate a **final diagnosis**. The system utilizes three specialized agents:

1. **Cardiologist Agent**: Diagnoses potential cardiovascular conditions, particularly arrhythmia, based on symptoms and reports.
2. **Psychologist Agent**: Analyzes potential psychological conditions, particularly anxiety and panic disorders.
3. **Pulmonologist Agent**: Assesses respiratory issues and evaluates the impact of anxiety-induced panic episodes on pulmonary health.

Each agent processes the provided data and generates a diagnosis, which is combined to produce a **final diagnosis**. This output is saved in a text file for further review.

---

## **Project Requirements**

### **System Requirements**
- **Operating System**: Windows/Linux/Mac
- **Python Version**: Python 3.7+ (Python 3.10+ recommended)

### **Python Libraries**

You will need the following Python libraries to run this project:

- `flask` (for the web framework, if applicable)
- `numpy` (for numerical computations)
- `pandas` (for data processing)
- `scikit-learn` (for machine learning models)
- `tensorflow` or `pytorch` (for AI model processing, depending on which framework you use)
- `openai` (if using OpenAI models for agent responses)
- `matplotlib` (for data visualization, if needed)

---

## 🚀 Project Setup

### 1. Clone the Repository

```bash
git clone https://github.com/KHaritha04/AI-Agents-for-Medical-Diagnostics
```

### 2. Navigate to the Project Directory

```bash
cd AI-Agents-for-Medical-Diagnostics
```

### 3. Set Up a Virtual Environment (Recommended)

```bash
python -m venv venv
```

### 4. Activate the Virtual Environment

- **Windows:**
  ```bash
  .\venv\Scripts\activate
  ```

- **Linux / macOS:**
  ```bash
  source venv/bin/activate
  ```

### 5. Install Required Dependencies

```bash
pip install -r requirements.txt
```

---

## 🗄️ Database Setup

This project requires a database to store agent results and diagnostic data.  
You can use **SQLite** or any SQL-based database like **MySQL** or **PostgreSQL**.

### Database Configuration Steps

1. Ensure **SQLite** or another SQL database is installed on your system.  
   - If you use SQLite, the database file will be created automatically.  
   - For MySQL or PostgreSQL, configure credentials in `config.py`.

2. Update the connection settings in:
   ```bash
   config.py
   ```
   Example:
   ```python
   DATABASE_URI = "sqlite:///diagnostics.db"
   ```

3. **Database Schema Overview:**
   - **Agents Table:** Stores output from each specialized agent (Cardiologist, Psychologist, Pulmonologist).
   - **Final Diagnosis Table:** Stores the combined diagnosis from all agents.

Ensure the application has read/write permissions to the database.

---

## 🧩 How to Run the Project Locally

### 1. Set Up the Database

- For **SQLite** → no setup required.  
- For **MySQL/PostgreSQL** → update credentials in `config.py`.

### 2. Run the Flask Application

If the project includes a Flask web interface, run:

```bash
python app.py
```

Then open your browser and visit:
```
http://127.0.0.1:5000/
```

### 3. Running the AI Agents

This project includes three AI agents that process medical reports:

| Agent | Role |
|--------|------|
| 🫀 Cardiologist | Analyzes heart-related symptoms |
| 🧠 Psychologist | Assesses mental health parameters |
| 🫁 Pulmonologist | Evaluates respiratory conditions |

Each agent independently generates a diagnosis.  
Results are merged into a **final diagnosis**, saved in:

```bash
results/final_diagnosis.txt
```

### 4. Testing the System

- Upload a medical report via UI *(if available)*  
- Or run the test scripts using:
  ```bash
  python agents/test_agents.py
  ```

### 5. Accessing Final Results

- Open the file:
  ```bash
  results/final_diagnosis.txt
  ```
- Review the summarized report from all AI agents.
