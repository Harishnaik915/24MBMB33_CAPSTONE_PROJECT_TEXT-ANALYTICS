Overview

This project applies Text Analytics and NLP techniques to analyze player-generated text from video games and identify risky behavioural patterns such as emotional stress, compulsive play, addiction signals, and harmful social pressure.

Instead of using AI to increase engagement or monetization, this project focuses on promoting healthy gaming, early risk detection, and well-being-driven interventions.

The system analyzes:

In-game chat logs

Community forum conversations

Support ticket messages

And generates meaningful insights using classification models, topic modeling, and intent detection.

🎯 Project Objectives

Detect harmful emotional patterns in player chats

Discover compulsive play drivers using unsupervised NLP

Identify early signs of gaming addiction from linguistic cues

Detect harmful social pressure from teammates and groups

Recommend supportive actions and time-based warnings

Promote responsible gameplay through AI-driven interventions

⭐ Use Cases Implemented
1️⃣ Harmful Emotional Pattern Detection

Detects emotionally intense or harmful chat messages such as anger, frustration, and emotional burnout.
Model: TF-IDF + Logistic Regression
Output: Harmful / Not Harmful

2️⃣ Detecting Compulsive Play Drivers (Topic Modeling)

Uncovers hidden themes that push players into compulsive gaming such as:

Grinding

FOMO

Event pressure

Clan obligations

Season pass pressure

Model: TF-IDF + K-Means (4 topics)

3️⃣ Early Addiction Detection Through Linguistic Markers

Identifies early addiction risk from phrases like:
“I can’t stop”, “I skipped sleep”, “playing all night”.
Output: Low / Moderate / High Risk

4️⃣ Harmful Social Pressure Detection

Classifies multiplayer social pressure types:

Direct Pressure

Guilt Inducing

Team Dependency

Competitive Pressure

No Pressure

Model: Weak supervision + Multi-class classifier

5️⃣ Support & Time-Based Well-Being Interventions

Suggests supportive actions like break reminders, rest suggestions, hydration alerts, and detects extended session duration for time-on-task warnings.

📂 Repository Structure
│── data/
│   ├── gaming_text_analytics_dataset.csv
│   ├── gaming_community_forum_dataset.csv
│   ├── gaming_support_ticket_dataset.csv
│
│── notebooks/
│   ├── usecase_1_harmful_emotion.ipynb
│   ├── usecase_2_topic_modeling.ipynb
│   ├── usecase_4_social_pressure.ipynb
│   ├── combined_pipeline.ipynb
│
│── models/
│   ├── harmful_emotion_model.joblib
│   ├── social_pressure_model.joblib
│
│── README.md
│── requirements.txt

📊 Datasets Used
Dataset	Rows	Purpose
gaming_text_analytics_dataset.csv	600	Chat messages for emotional detection
gaming_community_forum_dataset.csv	700	Topic modeling & compulsive play drivers
gaming_support_ticket_dataset.csv	550	Player fatigue & well-being signals

All datasets contain:

Message text

Associated labels (weak/synthetic)

Preprocessed versions

🛠️ Technologies & Libraries

Python

Pandas, NumPy

Scikit-Learn

TF-IDF Vectorizer

K-Means Clustering

Logistic Regression

t-SNE Visualization

Jupyter Notebook

⚙️ Installation
git clone https://github.com/<your-username>/<project-repo>.git
cd <project-repo>
pip install -r requirements.txt

▶️ How To Run the Project
Run Use Case 1 (Harmful Emotional Patterns)
jupyter notebook notebooks/usecase_1_harmful_emotion.ipynb

Run Use Case 2 (Topic Modeling)
jupyter notebook notebooks/usecase_2_topic_modeling.ipynb

Run Social Pressure Classification
jupyter notebook notebooks/usecase_4_social_pressure.ipynb


Models will automatically:

Load data

Preprocess text

Train ML model

Display metrics

Save trained models

📈 Key Results
🔥 Use Case 1

High accuracy for harmful emotion detection

Able to detect anger, frustration, emotional burnout

🔥 Use Case 2

Discovered 4 major compulsive play topics:

Grind/FOMO

No-sleep culture

Clan pressure

Season-pass pressure

🔥 Use Case 4

Multiclass classifier trained to detect social pressure types

🔥 Use Case 5

Time-on-task thresholds + intent detection for supportive actions

💡 Insights & Impact

Players often experience hidden psychological pressure from events, clans, and season passes

Community culture sometimes normalizes unhealthy behaviour (e.g., no-sleep raids)

Emotional burnout is detectable from simple chat patterns

Early interventions can significantly reduce addictive tendencies

This framework promotes ethical gameplay and supports healthy gaming habits

🚀 Future Enhancements

Use transformers like BERT / RoBERTa for better context detection

Incorporate voice chat transcription

Build a real-time dashboard

Deploy as an API for game developers

Use active learning for continuous improvement

 Author

Harish D. Naik
MBA – Business Analytics
University of Hyderabad
