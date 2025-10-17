# Islamic Knowledge Agent

An AI-powered conversational agent designed to provide insights into Islamic teachings. It integrates Quran verses (Arabic + English translations), Hadith with references and grades, and LLM-generated explanations. Built with [n8n](https://n8n.io/) using the Google Gemini model, it leverages HTTP requests to fetch data from [alquran.cloud](https://alquran.cloud/) and [hadith-api](https://github.com/fawazahmed0/hadith-api). Ideal for educational purposes, this project offers an interactive chat interface.

# Features
- Fetch Quran verses by reference (e.g., "2:255") with translations.
- Retrieve Hadith with English text, Arabic (if available), and grades (e.g., Sahih).
- Provide LLM-based explanations linking Quran and Hadith.
- Maintain context with memory support for multi-turn conversations.
- Customizable n8n workflow for easy deployment.

# Tech Stack
- **Framework**: n8n (workflow automation)
- **LLM**: Google Gemini
- **APIs**: alquran.cloud, hadith-api
- **Tools**: HTTP Request nodes

# Prerequisites
- n8n instance (cloud or self-hosted)
- Google Gemini API key (from [Google AI Studio](https://aistudio.google.com/app/apikey))
- Node.js environment (for local n8n setup)

# Setup
1. **Install n8n**:
   - Cloud: Sign up at [n8n.io](https://n8n.io/).
   - Self-host: Run `docker run -it --rm --name n8n -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n`.
2. **Add Gemini Credential**:
   - In n8n, go to Credentials > Add Credential > Google Gemini API, and input your API key.
3. **Import Workflow**:
   - Download the workflow JSON (available in this repo) and import it via n8n's Workflow > Import.
4. **Configure Nodes**:
   - Update HTTP Request URLs and test connections to APIs.
5. **Activate**:
   - Toggle the workflow to Active and open the chat interface.

# Usage
- **Chat Interface**: Open the chat (via n8n's Open chat button) and send queries like:
  - "Show Quran 2:255 with a related Hadith."
  - "What does the Quran say about charity?"
- **Response**: Expect formatted output with Quran (Arabic + translation), Hadith (text + reference), and an explanation.

# Contributing
Contributions are welcome! Please:
- Fork the repository.
- Create a feature branch (`git checkout -b feature-name`).
- Commit changes (`git commit -m "Add feature"`).
- Push and open a Pull Request.
- Follow the [n8n community guidelines](https://community.n8n.io/).

# License
[MIT License](LICENSE) - Feel free to use and modify, but check the API terms for usage limits.

## Status
Work in progress as of October 17, 2025. Check back for updates or contribute to enhance features like audio support or additional Hadith collections!
