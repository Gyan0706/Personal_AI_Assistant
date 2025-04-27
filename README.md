# 🤖 AI Chat Agent: Gmail & Google Calendar Automation (n8n Workflow)

An intelligent, AI-driven automation built with **n8n** that processes chat messages and manages your **Gmail** and **Google Calendar** seamlessly.

---

## ✨ Features

- **AI Agent (OpenAI powered)**: Smartly interprets and responds to incoming chat messages.
- **Email Automation**:
  - Send emails automatically via Gmail.
  - Fetch emails from Gmail inbox.
- **Calendar Automation**:
  - Create Google Calendar events.
  - Retrieve existing calendar events.
- **Context Awareness**: Maintains conversation memory for smooth interactions.

---

## 🧩 Workflow Structure

```
When Chat Message Received ➔ AI Agent ➔ (Send Email | Get Emails | Create Calendar Event | Get Calendar Events)
```

| Node | Description |
|:-----|:------------|
| `When chat message received` | Triggers the workflow when a new message is received. |
| `AI Agent (Tools Agent)` | Core logic handler using OpenAI and memory management. |
| `OpenAI Chat Model` | Interfaces with OpenAI to generate smart outputs. |
| `Simple Memory` | Stores ongoing conversation memory. |
| `Gmail (send message)` | Sends an email as per AI instructions. |
| `Gmail1 (getAll messages)` | Retrieves emails from the Gmail inbox. |
| `Google Calendar (create event)` | Adds a new calendar event. |
| `Google Calendar1 (getAll events)` | Fetches existing events from Google Calendar. |

---

## 🚀 Getting Started

### 1. Clone this repository
```bash
git clone https://github.com/your-username/your-repo-name.git
```

### 2. Setup n8n
Install n8n if you haven't already:
```bash
npm install n8n -g
```

Start n8n:
```bash
n8n
```

Or use [n8n.cloud](https://n8n.io/cloud) for easy deployment.

### 3. Import the workflow
- Open your n8n editor.
- Import the workflow JSON file (`.json` from this repo).

### 4. Connect your credentials
- **Gmail OAuth2**: Create OAuth credentials and connect Gmail nodes.
- **Google Calendar OAuth2**: Connect your Calendar nodes similarly.
- **OpenAI API Key**: Add your OpenAI credentials to the OpenAI node.

> Make sure your **redirect URIs** match n8n’s expected URL.

---

## ⚙️ Requirements

- n8n v1.0 or later
- OpenAI API Key
- Google Cloud project with OAuth credentials
- Gmail and Google Calendar API enabled

---

## 🛠 Configuration

- Set environment variables if deploying:
  ```
  N8N_BASIC_AUTH_ACTIVE=true
  N8N_BASIC_AUTH_USER=yourusername
  N8N_BASIC_AUTH_PASSWORD=yourpassword
  ```

- Adjust OpenAI model parameters (`temperature`, `max_tokens`) inside the AI Agent node if necessary.

---

## 🐞 Troubleshooting

- **OAuth Authorization Errors**: Reconnect Gmail/Calendar credentials; check if refresh tokens are valid.
- **OpenAI Issues**: Ensure API key is active and billing is set up.
- **n8n Node Failures**: Debug by checking execution history in n8n.

---

## 📈 Future Roadmap

- [ ] Slack/Discord integration
- [ ] User authentication for multi-user support
- [ ] AI-enhanced event suggestions
- [ ] Database integration for persistent memory

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).



