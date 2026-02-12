## 🧠 Core Features & Logic

### 1. The ML Brain (Decision Tree)

The app uses a **Decision Tree Classifier** to analyze lifestyle patterns. Unlike simple formulas, this algorithm "learns" from the CSV data. It creates a hierarchy of importance—for example, it might prioritize **Mental_Health_History** and **Days_Indoors** as the strongest indicators of current wellbeing. By splitting data into "branches," it predicts a base health **Grade** from 1 to 10.
While the ML handles historical patterns, the **JavaScript Sentiment Engine** handles the "now." It parses user text against a library of 200+ keywords.
* **Positive Boost:** Words like *resilient* or *grateful* increase the score.
* **Stress Penalty:** Words like *suffocated* or *fatigue* decrease it.

### 2. Feature Set

The model focuses on high-impact markers identified in the CSV:

* **Physical Isolation:** Tracking `Days_Indoors` to measure social withdrawal.
* **Clinical Markers:** `Mood_Swings` and `Mental_Health_History`.
* **Behavioral Shifts:** `Changes_Habits` to detect routine disruptions.

---
## 📁 Project Structure

```text
mindcore-app/
├── app.py                # Flask Backend & ML Logic
├── Mental Health.csv     # Dataset for Training
├── requirements.txt      # Python Dependencies
└── templates/
    └── index.html        # UI & Sentiment Logic

```
## Previews

<p align="center">
  <img src="previews/preview1.png" alt="Preview 1" width="400" style="border: 2px solid #ccc; margin-right: 10px;" />
  <img src="previews/preview2.png" alt="Preview 2" width="400" style="border: 2px solid #ccc;" />
</p>

<p align="center">
  <b>Preview 1</b> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <b>Preview 2</b>
</p>



---

## 🚀 Easy Run Steps (Local)

1. **Install Python:** Ensure Python 3.9+ is installed.
2. **Install Libraries:** Run `pip install flask pandas scikit-learn gunicorn`.
3. **Add Data:** Place your `Mental Health.csv` in the root folder.
4. **Launch:** Run `python app.py`.
5. **View:** Open `http://127.0.0.1:5000` in your browser.

---
