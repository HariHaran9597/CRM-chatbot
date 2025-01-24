# AI Customer Support Chatbot with CRM Integration

A modern customer support chatbot that integrates with Zoho CRM, powered by Google's Gemini AI, and features a ticket management system. This application provides a seamless interface for customer support with real-time CRM data integration.

## Features

### 1. Interactive Chatbot
- Real-time chat interface with AI-powered responses
- Context-aware conversations using customer information
- Support for order status queries and ticket management
- Persistent chat history using local storage

### 2. Ticket Management System
- Create and track support tickets
- Real-time ticket status updates
- Integration with CRM for ticket logging
- Email-based ticket association

### 3. CRM Integration (Zoho)
- Real-time customer data fetching
- Automatic logging of chat interactions
- Customer information display during conversations
- Ticket creation with CRM synchronization

### 4. User Interface
- Clean, modern design with responsive layout
- Real-time loading indicators
- Easy-to-use ticket creation form
- Chat history management
- Mobile-friendly interface

## Technical Stack

- **Backend**: Python Flask
- **Frontend**: HTML5, CSS3, JavaScript
- **AI**: Google Gemini AI
- **CRM**: Zoho CRM API
- **Database**: In-memory storage (can be extended to persistent storage)
- **Deployment**: Render

## Setup and Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd chatbot-project-CRM
```

2. Create a virtual environment:
```bash
python -m venv chatbot-env
source chatbot-env/bin/activate  # On Windows: .\chatbot-env\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
GEMINI_API_KEY=your_gemini_api_key
ZOHO_ACCESS_TOKEN=your_zoho_access_token
```

5. Run the application:
```bash
python app.py
```

## API Endpoints

### 1. Chat Endpoint
```
POST /chat
```
Request body:
```json
{
    "message": "user message",
    "email": "user@example.com"
}
```

### 2. Ticket Management
```
POST /create_ticket
```
Request body:
```json
{
    "subject": "ticket subject",
    "description": "ticket description",
    "email": "user@example.com"
}
```

```
GET /ticket_status/<ticket_id>
```

## Environment Variables

- `GEMINI_API_KEY`: Google Gemini AI API key
- `ZOHO_ACCESS_TOKEN`: Zoho CRM access token
- `ZOHO_CRM_URL`: Zoho CRM API URL (default: https://www.zohoapis.com/crm/v2)

## Local Development

1. Set up environment variables in a `.env` file
2. Run the Flask development server:
```bash
python app.py
```
3. Access the application at `http://localhost:5000`

## Deployment to Render

1. Push your code to a GitHub repository

2. On Render Dashboard:
   - Create a new Web Service
   - Connect your GitHub repository
   - Set environment variables:
     - GEMINI_API_KEY
     - ZOHO_ACCESS_TOKEN
     - PYTHON_VERSION: 3.9.18

3. Configuration (already set in render.yaml):
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn wsgi:application`

## Project Structure

```
chatbot-project-CRM/
├── app.py              # Main application file
├── chatbot.py         # Chatbot logic
├── requirements.txt   # Python dependencies
├── runtime.txt       # Python version specification
├── render.yaml       # Render deployment configuration
├── wsgi.py          # WSGI entry point
├── static/          # Static files
└── templates/       # HTML templates
    └── index.html   # Main chat interface
```

## Features to Add

1. Persistent database storage
2. User authentication
3. Multiple CRM platform support
4. Analytics dashboard
5. Customizable chatbot responses
6. File attachment support for tickets

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Security Notes

- Store sensitive API keys in environment variables
- Implement rate limiting for production
- Add input validation and sanitization
- Implement proper authentication
- Use HTTPS in production

## License

This project is licensed under the MIT License - see the LICENSE file for details.