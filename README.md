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

## Deployment

### Option 1: Deploy to Heroku

1. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

2. Login to Heroku:
   ```bash
   heroku login
   ```

3. Create a new Heroku app:
   ```bash
   heroku create your-app-name
   ```

4. Set your environment variables:
   ```bash
   heroku config:set GEMINI_API_KEY=your_api_key_here
   ```

5. Deploy:
   ```bash
   git push heroku main
   ```

### Option 2: Deploy to Render

1. Create a new account on [Render](https://render.com)

2. Create a new Web Service

3. Connect your GitHub repository

4. Set the following:
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`

5. Add environment variables in the Render dashboard:
   - `GEMINI_API_KEY`: your API key
   - `PORT`: (optional, Render sets this automatically)

### Option 3: Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Set environment variables in Vercel dashboard:
   - `GEMINI_API_KEY`: your API key

4. For Vercel, you may need to use serverless functions instead. See [Vercel serverless functions documentation](https://vercel.com/docs/functions).

### Option 4: Deploy to Railway

1. Create a new account on [Railway](https://railway.app)

2. Create a new project and connect your repository

3. Add environment variables:
   - `GEMINI_API_KEY`: your API key

4. Railway will automatically detect and deploy your Node.js app

### Option 5: Deploy to DigitalOcean App Platform

1. Create a new account on [DigitalOcean](https://www.digitalocean.com)

2. Create a new App and connect your repository

3. Set environment variables:
   - `GEMINI_API_KEY`: your API key

4. DigitalOcean will automatically build and deploy your app

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
