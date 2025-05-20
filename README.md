# 🧠 Project 3: Creating an Autonomous Agent for Email Management

**Team Member**: Ranran Hu  
**Course**: Artificial Intelligence  
**Platform**: macOS  

---

## 📌 Task 1: Install Auto-GPT on Local Computer

### 1.1 Installation

**Steps Followed**:

1. Cloned the Auto-GPT repository from GitHub:  
   🔗 https://github.com/Significant-Gravitas/Auto-GPT
2. Followed the official macOS installation guide video:  
   🎥 https://www.youtube.com/watch?v=uPODYPmYKVw
3. Installed dependencies:
   - Installed Python 3.11 via Anaconda
   - Installed required packages with:  
     `pip install -r requirements.txt`
4. Created a `.env` file containing my OpenAI API key (paid account with $5 credit).
5. Edited `config.yaml` to disable browser mode by setting:
   ```yaml
   browser:
     name: "none"
6. Launched Auto-GPT with the following command:
     python -m autogpt

 Installation Testing:
     Auto-GPT launched successfully.
     Verified interaction in both manual mode and autonomous task setup.


### 1.2 Issues Encountered and Solutions

 First isuue: Pydantic version incompatibility with SpaCy.
 Solution:  Downgraded pydantic to 1.10.22 using: "pip install "pydantic<2.0.0" --force-reinstall"

 Second isuue:  Stuck on "Thinking..."
 Solution:  Disabled browser mode in "config.yaml" ; added API funds


### 1.3 Summary

 Successfully installed Auto-GPT on macOS, resolved environment compatibility issues, and confirmed local functionality. 

## 📌 Task 2: Add the Email Plugin and Evaluate
### 2.1  Plugin Installation
Steps:
1. Downloaded Auto-GPT Plugins from:
    🔗 https://github.com/Significant-Gravitas/Auto-GPT-Plugins
2. Placed email plugin files into the "plugins/" folder.
3. Edited .env file to allowlist the plugin:
     "ALLOWLISTED_PLUGINS=AutoGPTEmailPlugin"
4. Configured email in .env:
     "EMAIL_ADDRESS=your-email@gmail.com
      EMAIL_PASSWORD=your-app-password
      EMAIL_SMTP_HOST=smtp.gmail.com
      EMAIL_SMTP_PORT=587
      EMAIL_IMAP_SERVER=imap.gmail.com"

### 2.2 Testing and Confirmation
✅ Sending Test:
     Auto-GPT successfully drafted and sent an invitation email.

⚠️ Receiving Test:
     * Encountered IMAP access error:
     "SEARCH illegal in state AUTH"
    
    * Per project guidelines, receiving is optional.

### 2.3 Issues Encountered and Solutions
First issue: Gmail login blocked.
Solution: Enabled 2FA and used Gmail App Password

Second issue: Email plugin error with "attachment" field.
Solution: Removed the "attachment" field from the email command

Third isuue:  IMAP read error.
Solution: Focused on sending functionality only, as receiving is not mandatory


### 2.4 Summary
Successfully configured and tested the Auto-GPT Email Plugin to send emails. Debugged common security and API integration issues.


## ✅ Final Conclusion

I successfully:
     * Installed Auto-GPT on a Mac.
     * Resolved key environment and dependency conflicts.
     * Integrated and tested the Email Plugin.
     * Demonstrated the ability to draft and send emails via an AI agent.

Major issues such as package incompatibility, Gmail security, and plugin errors were addressed effectively through targeted debugging and research.


## 🔒 Notes on Security
The OpenAI API Key was never exposed publicly.

Sensitive information (email, password) is excluded from this repo.

A .env.example file is provided for configuration reference.

