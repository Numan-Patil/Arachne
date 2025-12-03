# Arachne Web

Your AI web weaver **by Undrstanding**, extracting info from any URL using Gemini AI.

## Features

- 🔍 Analyze any website URL
- 📊 Extract summaries, images, and key data
- 🛡️ Genuineness & safety checks
- 💾 History of previous analyses
- ❓ Follow-up questions
- 📥 Export results as text file
- 📋 Copy results to clipboard

## Prerequisites

- Node.js (version 18 or higher)
- npm (version 8 or higher)
- Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)

## Installation

1. Clone or download this repository

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add your Gemini API key:
   ```
   GEMINI_API_KEY=your_actual_api_key_here
   ```
   
   You can also optionally set:
   ```
   GEMINI_MODEL=gemini-2.5-flash-preview-09-2025
   PORT=3000
   ```

## Running Locally

Start the server:
```bash
npm start
```

The application will be available at `http://localhost:3000`


## Environment Variables

- `GEMINI_API_KEY` (required): Your Gemini API key from Google AI Studio
- `GEMINI_MODEL` (optional): The model to use (default: `gemini-2.5-flash-preview-09-2025`)
- `PORT` (optional): Server port (default: `3000`)

## Security Notes

- **Never commit your `.env` file** to version control
- The API key is stored securely on the server and never exposed to the client
- All API calls are proxied through the backend server

## Troubleshooting

### API Key Errors
- Make sure your `.env` file exists and contains `GEMINI_API_KEY`
- Verify your API key is valid at [Google AI Studio](https://aistudio.google.com/app/apikey)

### Port Already in Use
- Change the `PORT` in your `.env` file to a different port
- Or kill the process using the port: `lsof -ti:3000 | xargs kill` (Mac/Linux)

### CORS Errors
- The backend server handles CORS automatically
- Make sure you're accessing the app through the backend server, not directly opening the HTML file

## License

MIT

## Credits

Created by **Undrstanding**

# Arachne
