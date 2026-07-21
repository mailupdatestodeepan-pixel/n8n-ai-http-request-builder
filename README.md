# 🤖 AI-Powered HTTP Request Builder for n8n

Turn plain English into executable HTTP API requests using AI.

This workflow combines an **OpenAI GPT-4.1 Mini** chat model, an **AI Agent**, and n8n's native **HTTP Request Tool** to automatically generate and execute REST API requests from natural-language instructions.

---

## ✨ Features

- ✅ Supports GET requests
- ✅ Supports POST requests
- ✅ Supports PUT requests
- ✅ Supports PATCH requests
- ✅ Supports DELETE requests
- ✅ Automatically generates request URLs
- ✅ Builds request headers
- ✅ Creates query parameters
- ✅ Generates JSON request bodies
- ✅ Supports authenticated APIs
- ✅ Returns the complete HTTP response
- ✅ Built entirely with native n8n nodes

---

# Workflow Overview

```
Manual Trigger
      │
      ▼
User Request
      │
      ▼
AI Request Planning Agent
     │          │
     │          ▼
     │     GPT-4.1 Mini
     │
     ▼
HTTP Request Tool
      │
      ▼
API Response
```

---

# Use Cases

This workflow is useful for:

- API testing
- REST API exploration
- Backend development
- Learning HTTP APIs
- Rapid API prototyping
- Internal automation
- AI-powered developer tools

---

# Requirements

Before running the workflow you'll need:

- n8n (latest version recommended)
- OpenAI API credentials
- Internet access
- Credentials for any API you want to call

---

# Setup

## 1. Configure OpenAI

Open the **OpenAI GPT-4.1 Mini** node and add your OpenAI credentials.

---

## 2. Configure API Credentials

If the target API requires authentication:

- API Key
- Bearer Token
- Basic Authentication
- Custom Headers

provide those credentials before executing the workflow.

---

## 3. Edit the Request

Open the **Set User Request Field** node.

Replace the sample text with your own request.

Example:

```
Get current weather in Tokyo using OpenWeather API.
```

or

```
Create a GitHub issue in my repository.
```

or

```
Search Wikipedia for Albert Einstein.
```

---

## 4. Execute

Click **Execute Workflow**.

The AI Agent will:

1. Understand your request
2. Determine the correct HTTP method
3. Build the URL
4. Generate headers
5. Generate query parameters
6. Generate the JSON body (if required)
7. Execute the HTTP request
8. Return the complete API response

---

# Example Requests

### Weather API

```
Get current weather in Tokyo using OpenWeather API.
```

---

### GitHub

```
Get the latest 5 commits from a GitHub repository.
```

---

### Wikipedia

```
Search Wikipedia for Albert Einstein.
```

---

### Notion

```
Create a page in my Notion database.
```

---

### JSONPlaceholder

```
Create a new post with title "Hello" and body "Testing API".
```

---

# Security

This workflow intentionally **does not invent credentials**.

If an API requires authentication, the AI asks for the required credentials instead of generating fake API keys or placeholder values.

---

# Customization

You can easily extend this workflow by adding:

- Validation nodes
- Rate limiting
- Retry logic
- Error handling
- Logging
- Approval workflows
- Response formatting
- Database storage

---

# Built With

- n8n
- OpenAI GPT-4.1 Mini
- AI Agent
- HTTP Request Tool

---

# License

This project is released under the MIT License.

---

# Author

**NodeFlow Studio**

Building practical AI-powered automations with n8n.
