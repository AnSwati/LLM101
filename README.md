# LLM101 Course - 

# Step 1: OpenAI API Key Setup Guide

## Overview

An **API Key** is a unique token that allows you to authenticate and access OpenAI's services programmatically. This key is essential for using OpenAI's models (like GPT-4, GPT-3.5) in your applications.

## Prerequisites

Before starting, ensure you have:
- A working internet connection
- A valid email address
- A credit card (for existing accounts) or access to free credits (for new accounts)
- Approximately 5-10 minutes to complete the setup

## What is an API Key?

An **API Key** is:
- A secure authentication token
- Required to make API calls to OpenAI services
- Unique to your account
- Should be kept confidential (never share publicly)
- Can be regenerated at any time if compromised

### Why Do You Need It?

The API key allows you to:
- Access OpenAI models from your code
- Build applications using ChatGPT, GPT-4, etc.
- Make API requests directly without using the web interface
- Integrate AI capabilities into your projects


## Screenshots Reference

| Screenshot File |
|---|
| Screenshots/Platform_Openai_Webpage.png |
| Screenshots/OPENAI_API_KEY.png |
| Screenshots/Open_notebook.png |
| Screenshots/Create_New_Secret_Key_Prompt.png|
| Screenshots/Create_API_Key.png |
| Screenshots/Authorize_Colaboratory.png |
| Screenshots/AfterAuthentication_webpage.png |
| Screenshots/After_Authroization_ColabwithGithub.png|

## Step 1.1: Visit OpenAI Platform

1. Open your web browser
2. Navigate to: https://platform.openai.com/docs/overview
3. You should see the OpenAI platform homepage

[View: platformopenai_webpage.png](./Screenshots/platformopenai_webpage.png)

## Step 1.2: Create or Access Your Account

### Option A: Create a New Account (Recommended)

**Why create a new account?**
- Receive free trial credits (~$5-18)
- Test features without payment concerns
- Separate billing for the workshop

**Steps to Create Account:**

1. Click the **"Sign up"** button
2. Enter your **email address**
3. Create a strong **password**
4. Verify your email by clicking the link sent to your inbox
5. Complete your **profile information**:
   - Full Name
   - Organization (optional)
   - Phone Number
   - Use Case
6. Accept the terms and conditions
7. You're all set! Your account is created with free credits

### Option B: Use Existing Account

1. Click the **"Log in"** button
2. Enter your **email address**
3. Enter your **password**
4. Complete any **two-factor authentication** if enabled
5. You'll be logged into your account

[View: AfterAuthentication_webpage.png](./Screenshots/AfterAuthentication_webpage.png)


## Step 1.3: Verify Your Account Credits

### For New Accounts

New OpenAI accounts receive:
- **Free trial credits**: Usually $5-$18 USD
- **Valid for**: 3 months from account creation
- **Automatic expiration**: After 3 months, credits expire

**Check your credits:**
1. Click the **profile icon** (top-right corner)
2. Select **"Billing"** from the dropdown
3. View your **"Credit balance"**

### For Existing Accounts

**Check available funds:**
1. Click the **profile icon** (top-right corner)
2. Select **"Billing"** from the dropdown
3. Check your **"Credit balance"** or **"Payment method"**

**Note**: If you're using a paid account, ensure you have:
- Valid payment method on file
- Sufficient credits/funds
- Billing alerts configured (optional but recommended)

## Step 1.4: Access Your Profile Settings

1. In the top-right corner, locate the **profile icon** (usually your initials or avatar)
2. Click it to open the dropdown menu
3. You should see several options:
   - Your Profile
   - Settings
   - Billing
   - API keys
4. Select **"Settings"** to access more options

## Step 1.5: Navigate to API Keys Section

1. From the profile dropdown, select **"Settings"**
2. In the left sidebar, click **"API keys"**
3. Or directly go to: https://platform.openai.com/account/api-keys

You should see:
- A list of existing API keys (if any)
- A **"Create new secret key"** button

## Step 1.6: Generate Your API Key

### Create a New Secret Key

1. Click the **"Create new secret key"** button
2. A dialog box will appear with options to configure your key

[View: create_new_secret_key_prompt.png](./Screenshots/create_new_secret_key_prompt.png)

### Configure Your API Key

**Name Field:**
```
OPENAI_API_KEY
```

**Project Field:**
- Leave as default (Personal) for now
- Or select your project if you have multiple

**Other Settings:**
- Keep all other options at their default values

Click **"Create secret key"** button

[View: Create_API_Key.png](./Screenshots/Create_API_Key.png)

---

## Step 1.7: Copy and Save Your API Key

⚠️ **CRITICAL**: This is a one-time display! You will NOT be able to view this key again.

### Immediately Copy Your Key

1. After creating the key, you'll see a dialog with:
   - Your secret key (long string of characters)
   - A **"Copy"** button

[View: OPENAI_API_KEY.png](./Screenshots/OPENAI_API_KEY.png)

2. Click the **"Copy"** button to copy to clipboard

3. **Immediately paste and save** it to:
   - A secure password manager (recommended)
   - A `.env` file in your project (for local development)
   - A secure text file (temporary, not recommended for production)

**Example of an API Key:**
```
sk-proj-abc123xyz789... (typically 48+ characters)
```

### If You Didn't Copy It

If you forgot to copy the key, don't worry:

1. Go to: https://platform.openai.com/account/api-keys
2. Find your API key in the list
3. Click the **"Edit"** button (pencil icon)
4. Click **"Show"** to reveal the key value
5. Copy it now

⚠️ **Note**: You can only see the full key once. After closing, it will show as masked (sk-****).

---

## Step 1.8: Secure Your API Key

### Best Practices

**DO:**
- ✅ Store in a `.env` file (use `.gitignore` to prevent uploading to GitHub)
- ✅ Use environment variables in your application
- ✅ Rotate keys periodically
- ✅ Use a password manager to store securely
- ✅ Create separate keys for different projects

**DON'T:**
- ❌ Share your key publicly
- ❌ Commit your key to version control (Git)
- ❌ Hardcode the key in your source code


### Store in .env File [If testing locally otherwise ignore this step]

**For Local Development:**

1. In your project root folder, create a file named: `.env`

2. Add your key:
```
OPENAI_API_KEY=sk-proj-your-actual-key-here
```

3. Create a `.gitignore` file (if not already exists) and add:
```
.env
.env.local
*.key
```

This prevents accidentally uploading your key to GitHub!

### Store in Environment Variables

**Option 1: Command Line (macOS/Linux)**
```bash
export OPENAI_API_KEY='sk-proj-your-key-here'
```

**Option 2: Windows PowerShell**
```powershell
$env:OPENAI_API_KEY='sk-proj-your-key-here'
```

**Option 3: In Python Code**
```python
import os
from dotenv import load_dotenv

# Load from .env file
load_dotenv()

api_key = os.getenv('OPENAI_API_KEY')
```

## What You Have Now

After completing Step 1, you have:

- ✅ OpenAI account created or accessed
- ✅ Free credits verified (or payment method added)
- ✅ API key generated
- ✅ API key securely stored
- ✅ Ready to use OpenAI's models in code



# Step 2: Google Colab Setup

## Overview

Google Colab is a cloud-based Jupyter notebook environment that allows you to run Python code without local setup. It provides free access to GPUs and is ideal for machine learning and AI development.

## Prerequisites

- Completed Step 1 (OpenAI API Key setup)
- Google account
- Internet connection

## Step 2.1: Access Google Colab

1. Navigate to: https://colab.research.google.com/
2. Click **"Open notebook"** button

[View: Open_notebook.png](./Screenshots/Open_notebook.png)

## Step 2.2: Connect GitHub Repository

1. In the dialog, select **"GitHub"** tab
2. Provide the GitHub URL: `https://github.com/AnSwati/LLM101`
3. Grant necessary authorization for Google Colab to access your GitHub

[View: Authorize_Colaboratory.png](./Screenshots/Authorize_Colaboratory.png)

## Step 2.3: Open Notebook in Colab

1. Once authorization is complete, locate the `Basic_LLM_tutorial_prompt_engineering.ipynb` file
2. Click on it to open directly in Google Colab

## What You Have Now

- ✅ Google Colab environment set up
- ✅ GitHub repository linked to Colab
- ✅ Notebook ready for development

## Next Steps

You're now ready to start working with LLMs in the Colab notebook environment.



# Step 3: Visual Studio Code Setup

## Overview

Run the LLM101 code locally on your machine using Visual Studio Code (VSCode). This option gives you more control and doesn't require Google Colab.

---

## Prerequisites

- Completed Step 1 (OpenAI API Key setup)
- Python installed
- pip (Python package manager) installed
- Visual Studio Code installed

---

## Step 3.1: Clone or Download Repository

### Option A: Clone Repository

1. Open VSCode terminal
2. Run the following command:

```bash
git clone https://github.com/AnSwati/LLM101.git
cd LLM101
```

### Option B: Download as ZIP

1. Visit: https://github.com/AnSwati/LLM101
2. Click **"Code"** → **"Download ZIP"**
3. Extract the ZIP file
4. Open the folder in VSCode: **File** → **Open Folder**

---

## Step 3.2: Verify Prerequisites

Ensure Python and pip are installed:
```bash
python --version
pip --version
```

Both should show version numbers. If not, install Python from: https://www.python.org/

## Step 3.3: Install Dependencies

Navigate to the project directory and install required packages:
```bash
pip install -r requirements.txt
```

Or manually install the required packages:
```bash
pip install openai python-dotenv
```

## Step 3.4: Set Up Environment Variables

1. Create a `.env` file in the project root folder
2. Add your OpenAI API key from Step 1:
```
OPENAI_API_KEY=sk-proj-your-actual-key-here
```

3. Create a `.gitignore` file and add:
```
.env
.env.local
```

This prevents accidentally uploading your API key to GitHub.


## Step 3.5: Run the Code

1. Open the Python script or notebook in VSCode
2. Run the code:
```bash
python script_name.py
```

Or use VSCode's **Run** button (▶️)


## What You Have Now

- ✅ LLM101 repository cloned/downloaded
- ✅ Dependencies installed
- ✅ Environment configured
- ✅ Ready to run LLMs locally

## FAQ

**Q: I get a RateLimit error when running the code**
A: This means you've exceeded your OpenAI API quota or run out of credits. Solutions:
- Create a new OpenAI account with fresh credits
- Use a different account with available credits
- Check your credit balance at: https://platform.openai.com/account/billing/overview

**Q: Can I use Google Colab instead of VSCode?**
A: Yes! Google Colab works well for this course. You can:
- Provide the GitHub URL (as shown in Step 2)
- Upload the full ZIP file
- Upload to Google Drive and connect Colab

**Q: What if I don't have Python installed?**
A: Install Python from https://www.python.org/ ensuring you check "Add Python to PATH" during installation.

**Q: How do I know if my environment is set up correctly?**
A: Run the following commands in terminal:
```bash
python --version
pip --version
python -c "import openai; print(openai.__version__)"
```
**Q: How much do API calls cost?**
A: Pricing varies by model. Check https://openai.com/pricing for current rates. New accounts get free trial credits.

**Q: Can I use one API key for multiple projects?**
A: Yes, but it's recommended to create separate keys for different projects for better tracking and security.

**Q: What if I lose my API key?**
A: Create a new one! Old keys can be revoked from the API keys dashboard.

**Q: Is my API key tied to my account?**
A: Yes, the key authenticates requests as your account. Charges will be billed to your account.

**Q: Can I have multiple API keys?**
A: Yes! You can create as many as needed and manage them from the API keys page.

## Troubleshooting

### Issue: "Free trial credits expired"
**Solution**: 
- Upgrade to a paid account
- Add a payment method in Billing settings
- See current pricing at: https://openai.com/pricing

### Issue: "API key not working / Authentication failed"
**Solution**:
- Verify the key is copied completely (check for missing characters)
- Ensure there are no extra spaces before/after the key
- Check if the key has been revoked (view in API keys page)
- Try creating a new key

### Issue: "Can't find API keys in settings"
**Solution**:
- Log out and log back in
- Try accessing directly: https://platform.openai.com/account/api-keys
- Ensure you have account access (not just team member)
- Clear browser cache and try again

### Issue: "No free credits available"
**Solution**:
- Check if you're using a new or existing account
- View billing details to see payment methods
- Contact OpenAI support if unsure

### Issue: "Rate limit exceeded"
**Solution**:
- You've made too many API calls too quickly
- Wait a few moments before making new requests
- Consider upgrading to a paid plan for higher limits

---

## Useful Links

- OpenAI Platform: https://platform.openai.com
- OpenAI Documentation: https://platform.openai.com/docs/overview
- Pricing Information: https://openai.com/pricing
- API Reference: https://platform.openai.com/docs/api-reference
- Support: https://support.openai.com
- Python Installation: https://www.python.org/
- Visual Studio Code: https://code.visualstudio.com/
- Git: https://git-scm.com/


