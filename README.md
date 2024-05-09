# Smart Renamer: AI-Powered Screenshot Renaming Tool


https://github.com/syedamaann/smart_renamer/assets/74735966/919af8ad-c969-4d06-8989-ec7e1479682b



**Smart Renamer** automatically organizes and renames macOS screenshots using Automator and OpenAI's GPT-4 Vision API. It detects new screenshots, analyzes content to create descriptive filenames, renames them, and logs each to avoid reprocessing.

## Features
- **Locate Screenshots**: Finds the most recent screenshot in a specified directory.
- **Analyze Content**: Uses AI to generate a concise description of the screenshot.
- **Rename and Log**: Renames screenshots based on AI-generated descriptions and logs them.

## Setup Instructions

### 1. Configure API Key:
```bash
echo "export OPENAI_API_KEY='your-api-key'" >> ~/.zshrc
source ~/.zshrc
```

### 2. Clone the Repository:
```bash
git clone https://github.com/[YourGitHub]/smart_renamer.git
cd smart_renamer
```

### 3. Configure Paths:
Edit `smart_renamer.py` and update the `DIRS` array with paths to your screenshot directory and log file.

### 4. Automator Folder Action Setup:
Open Automator, select "Folder Action" and the screenshot directory.
Add "Run Shell Script" with the command:
```bash
source ~/.zshrc
python3 /path/to/smart_renamer/smart_renamer.py
```
Replace `/path/to/smart_renamer/` with the actual script path and save the action as "RenameScreenshots".

### 5. Testing:
Take a screenshot to see if it automatically renames based on the content.

## Troubleshooting
- **API Key**: Ensure your OPENAI API Key is correctly set in `.zshrc`.
- **Paths and Permissions**: Check the paths in Automator and ensure the script has execution permissions.
