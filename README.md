# CRM Chatbot with Order Status and Support Tickets

A customer support chatbot integrated with Zoho CRM that handles order status inquiries and support ticket management.

## Features

- Real-time order status tracking
- Customer information display
- Support ticket creation and management
- Chat history with persistence
- Integration with Zoho CRM
- Modern, responsive UI

## Technologies Used

- Python 3.12
- Flask
- Google Gemini AI
- Zoho CRM API
- HTML/CSS/JavaScript

## Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/chatbot-project-CRM.git
cd chatbot-project-CRM
```

2. Create a virtual environment and activate it:
```bash
python -m venv chatbot-env
source chatbot-env/bin/activate  # For Unix/macOS
chatbot-env\Scripts\activate     # For Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up your API keys:
   - Get Gemini API key from Google AI Studio
   - Get Zoho CRM access token

5. Run the application:
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## Project Structure

- `app.py`: Main Flask application with API endpoints
- `chatbot.py`: Chatbot logic implementation
- `templates/`: HTML templates
- `static/`: Static files (CSS, JS)
- `requirements.txt`: Project dependencies

## API Endpoints

- `GET /`: Home page
- `POST /chat`: Chat endpoint for handling user messages
- `POST /create_ticket`: Create support ticket
- `GET /ticket_status/<ticket_id>`: Get ticket status

## Environment Variables

Required environment variables:
- `GEMINI_API_KEY`: Google Gemini API key
- `ZOHO_ACCESS_TOKEN`: Zoho CRM access token

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.