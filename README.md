# Spam Detection Challenge

A beginner-friendly machine learning competition built entirely on GitHub.

Participants submit predictions through Pull Requests, and a **live leaderboard updates automatically** after every merged PR.


## Live Leaderboard
[Open Leaderboard](https://vforviolet10.github.io/Spam_Detection_with_live_leaderboard/)


---

## Problem Statement

Classify SMS messages as:

* spam
* ham

Participants submit prediction files for the provided test set.

Submissions are automatically evaluated and ranked on the leaderboard.


---

## Evaluation Metrics

Submissions are scored using:

### Accuracy

```math
Accuracy = Correct Predictions / Total Predictions
```

### Precision

```math
TP / (TP + FP)
```

### Recall

```math
TP / (TP + FN)
```

### F1 Score

```math
2 * Precision * Recall / (Precision + Recall)
```

Leaderboard ranking metric:

```text
Primary Metric: F1 Score
```

---

# How To Participate

## 1 Fork Repository

Click:

```text
Fork
```

---

## 2 Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/spam-detection-challenge.git
cd spam-detection-challenge
```

---

## 3 Create Submission File

Add a CSV inside:

```bash
submissions/
```

Example:

```bash
submissions/team_alpha.csv
```

Format:

```csv
id,label
1,spam
2,ham
3,spam
4,ham
```

Rules:

Column names must be:

```csv
id,label
```

Allowed labels:

```text
spam
ham
```

---

## 4 Commit and Push

```bash
git add .
git commit -m "Add Team Alpha submission"
git push origin main
```

---

## 5 Open Pull Request

PR description example:

```text
Team Name: Team Alpha
Model Used: Naive Bayes
Local F1: 0.91
```

After merge:

- Submission scored

- Leaderboard updates automatically

---

## Sample Submission

```csv
id,label
1,spam
2,ham
3,spam
4,ham
5,spam
```

---

## Run Locally

Install dependencies:

```bash
pip install -r requirements.txt
```

Evaluate a submission:

```bash
python scripts/evaluate_submission.py submissions/team_alpha.csv
```

Example output:

```json
{
 "accuracy":0.90,
 "precision":0.92,
 "recall":0.88,
 "f1":0.90
}
```

---

## 🤖 Automated Workflow

On every merge to main:

GitHub Actions will:

* Validate submissions
* Score all submissions
* Update leaderboard
* Commit updated rankings
* Refresh GitHub Pages

Workflow:

```text
Pull Request
↓
Validation
↓
Scoring
↓
Leaderboard Update
↓
GitHub Pages Refresh
```

---

## 🛠 Tech Stack

* Python
* Pandas
* Scikit-learn
* GitHub Actions
* GitHub Pages
* HTML/CSS/JavaScript

---

## 📊 Example Leaderboard

```text
🥇 Data Wizards    0.95
🥈 Spam Hunters    0.94
🥉 AI Ninjas       0.92
```

---






---

## 📜 License

MIT License

---


## Sample First Submission

```csv
id,label
1,spam
2,ham
3,spam
4,ham
5,spam
```

Open a PR and get ranked 🚀
