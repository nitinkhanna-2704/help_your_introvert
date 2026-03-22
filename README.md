# Help Thee Introverts - Communication Assistant

An AI-powered communication assistant designed to help introverted employees showcase their work more effectively using sales psychology principles.

## What Is This?

"Help Thee Introverts" is a single-page web application that analyzes your workplace communications (chats, emails, task updates) and provides personalized advice on how to:

- **Showcase your work** without coming across as boastful
- **Write more effective emails** that highlight your contributions
- **Communicate impact** in meetings and written communication
- **Create weekly summaries** that get you noticed

## How It Works

### 1. Input Your Communication
Paste any of the following into the text area:
- Chat/Slack transcripts
- Email drafts
- Task lists or project updates
- Any custom communication you want to improve

### 2. AI Analysis
The AI analyzes your communication for:
- Missing impact statements
- Understatement of achievements
- Passive language that diminishes your work
- Visibility opportunities you might be missing

### 3. Get Personalized Advice
Receive:
- **Key Insights**: Observations about your communication style
- **Actionable Recommendations**: Specific steps to improve
- **Weekly Email Template**: A ready-to-use template
- **Book References**: Citations from sales psychology books

## The System Prompt

The core of the application is this system prompt that guides the AI:

```
You are a sales psychology and communication expert helping introverted
employees communicate their work more effectively. Your goal is to analyze
the user's communication and provide actionable advice based on principles
from:

1. "How to Win Friends and Influence People" by Dale Carnegie
2. "The Psychology of Selling" by Brian Tracy
3. "To Sell Is Human" by Daniel Pink
4. "Crucial Conversations" by Patterson, Grenny, et al.
5. "The Charisma Myth" by Olivia Cabane

Analyze the input communication type: {inputType}

Provide your response in this exact JSON format:
{
  "insights": ["List of 3-4 key observations about their communication", ...],
  "actions": ["Specific actionable recommendation 1", ...],
  "weeklyTemplate": "A professional weekly update email template",
  "bookReference": "A brief citation from relevant books"
}
```

## Supported AI Models

### Option 1: Claude API (Recommended)
- Uses Claude Opus 4.6
- Requires API key from Anthropic
- More powerful and consistent responses
- Sign up at https://www.anthropic.com

### Option 2: Ollama (Local - Free)
- Runs locally on your machine
- No API costs
- Requires Ollama installed
- Default model: llama3.3

#### Installing Ollama
1. Download from https://ollama.ai
2. Run `ollama pull llama3.3` in terminal
3. Keep Ollama running in background

## Usage

### Running the Application
Simply open `index.html` in any modern web browser. No server required.

### First Time Setup
1. **For Claude API**: Enter your API key in the header field
2. **For Ollama**: Select "Ollama (Local)" from the dropdown and ensure Ollama is running

### Analyzing Your Communication
1. Select input type (Chats/Emails/Tasks/Custom)
2. Paste your communication into the text area
3. Click "Analyze My Communication"
4. Review insights and copy the weekly template

## Example Use Cases

### Example 1: Chat Transcript
**Input:**
```
Team: "Great job on the project everyone!"
[You]: "Thanks"
Manager: "We should highlight this at the all-hands"
[You]: "Oh, it was really a team effort"
```

**AI Advice:**
- You're understating your contribution
- Suggest more specific language: "I led the X portion while Y handled..."
- Template for future responses

### Example 2: Weekly Email
**Input:**
```
Hi [Manager],
Here's what I worked on this week:
- Fixed some bugs
- Attended meetings
- Reviewed code

[Your Name]
```

**AI Advice:**
- Too generic - quantify your impact
- "Fixed 5 critical bugs affecting 200+ users"
- Add metrics and outcomes

## Book References Used

The AI draws from these best-selling books:

| Book | Author | Key Concept |
|------|--------|-------------|
| How to Win Friends... | Dale Carnegie | Make others feel important |
| The Psychology of Selling | Brian Tracy | Sales is helping, not pushing |
| To Sell Is Human | Daniel Pink | New ABCs of selling |
| Crucial Conversations | Patterson et al. | High-stakes communication |
| The Charisma Myth | Olivia Cabane | Charisma is a skill |

## Technical Details

- **Frontend**: Pure HTML/CSS/JavaScript (no build step)
- **API**: Claude Messages API or Ollama Generate API
- **Storage**: localStorage (settings only, no data)
- **Privacy**: All processing happens in-browser; no data sent to external servers except the AI API

## Files

```
help_your_introvert/
├── index.html    # Main application
├── README.md     # This file
└── SPEC.md       # Technical specification
```

## License

MIT License - Feel free to use and modify for your needs.

---

*Helping introverts shine in the workplace* 💡