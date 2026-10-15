# ATS Resume Screening Bot

A Python-based Telegram bot that screens candidate resumes against a Job Description (JD), calculates ATS match scores, ranks candidates, identifies skill gaps, and generates downloadable recruitment reports.

## Features

- Upload Job Descriptions in PDF, DOCX, and TXT formats
- Upload and screen multiple candidate resumes
- Calculate ATS match scores out of 100
- Check mandatory requirements
- Rank and compare candidates
- View candidate details and score breakdowns
- Identify strengths and missing skills
- Receive improvement recommendations
- Get certification and course recommendations
- Generate downloadable ATS recruitment PDF reports
- Interact through Telegram bot commands

## Technologies Used

- Python 3
- Telegram Bot API (`python-telegram-bot`)
- PDF text extraction (`pypdf`)
- Word document processing (`python-docx`)
- PDF report generation (`ReportLab`)
- Environment variable management (`python-dotenv`)
- Regular Expressions (Regex)

## Project Structure

```text
ATS-Resume-Chatbot/
├── bot.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/edigamahitha53-cmd/ATS-Resume-Chatbot.git
cd ATS-Resume-Chatbot
```

### 2. Create and activate a virtual environment (optional but recommended)

On Windows:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If ReportLab is not included in the requirements, install it separately:

```bash
pip install reportlab
```

### 4. Configure the Telegram bot token

Create a file named `.env` in the project folder and add your Telegram bot token:

```env
BOT_TOKEN=YOUR_TELEGRAM_BOT_TOKEN
```

Replace `YOUR_TELEGRAM_BOT_TOKEN` with your own token.

**Security:** Never upload your `.env` file or share your Telegram bot token publicly. The `.env` file should remain excluded through `.gitignore`.

### 5. Run the bot

```bash
python bot.py
```

Expected terminal output:

```text
Starting ATS Resume Screening Bot...
ATS Resume Screening Bot is running...
```

## How to Use

1. Open the bot in Telegram and send `/start`.
2. Use `/newjob` to start a recruitment session.
3. Upload the Job Description.
4. Upload one or more candidate resumes.
5. Use `/rank` to rank candidates.
6. Use `/details` to view candidate analysis.
7. Use `/compare` to compare multiple resumes.
8. Use `/gaps` to identify missing skills.
9. Use `/recommendations` to view improvement suggestions.
10. Use `/report` to generate a downloadable recruitment report.

## Available Commands

| Command | Description |
|---|---|
| `/start` | Start the bot |
| `/help` | View help and available commands |
| `/newjob` | Start a new recruitment session |
| `/upload_jd` | Upload a Job Description |
| `/upload_resumes` | Upload candidate resumes |
| `/rank` | Rank candidates by ATS score |
| `/details` | View candidate analysis |
| `/compare` | Compare candidate resumes |
| `/recommendations` | View recommendations |
| `/gaps` | View missing skills |
| `/report` | Download the ATS recruitment report |
| `/clear` | Clear uploaded resumes |
| `/reset` | Reset the recruitment session |

## ATS Scoring Criteria

The bot uses weighted criteria to calculate an ATS match score out of 100.

| Criterion | Maximum Score |
|---|---:|
| Technical Skills Match | 25 |
| Responsibilities Match | 20 |
| Relevant Experience | 15 |
| Years Experience | 10 |
| Domain Experience | 10 |
| Education | 5 |
| Certifications | 5 |
| Tools/Technology Match | 5 |
| Seniority/Role Alignment | 5 |
| **Total** | **100** |

Candidate ranking also considers mandatory requirements, relevant experience, and technical skill match as tie-breakers.

**Note:** ATS scores are automated estimates based on the bot's scoring rules. They should support, not replace, human review.

## Author

**Mahitha**

- GitHub Profile: https://github.com/edigamahitha53-cmd
- Project Repository: https://github.com/edigamahitha53-cmd/ATS-Resume-Chatbot

---

*Built with Python to simplify resume screening and candidate comparison through Telegram.*
