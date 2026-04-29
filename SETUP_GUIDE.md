# Doctor Know - ChatGPT Integration Setup Guide

## Prerequisites
- Node.js installed (v16 or higher) - Download from https://nodejs.org
- OpenAI API key - Get from https://platform.openai.com/api-keys

## Step-by-Step Installation

### 1. Get Your OpenAI API Key

1. Go to https://platform.openai.com/signup
2. Create an account (or sign in)
3. Go to https://platform.openai.com/api-keys
4. Click "Create new secret key"
5. Copy the key (starts with `sk-...`)
6. **Important:** Add payment method at https://platform.openai.com/account/billing

### 2. Install Backend Dependencies

Open terminal/command prompt in your project folder and run:

```bash
npm install
```

This will install:
- express (web server)
- cors (allow frontend to connect)
- openai (ChatGPT API client)

### 3. Configure Your API Key

Open `server.js` and replace this line:

```javascript
apiKey: 'YOUR_OPENAI_API_KEY_HERE'
```

With your actual API key:

```javascript
apiKey: 'sk-proj-...' // Your real key here
```

### 4. Start the Backend Server

```bash
npm start
```

You should see:
```
🩺 Doctor Know backend running on http://localhost:3000
📡 API endpoint: http://localhost:3000/api/chat
```

### 5. Test the Backend

Open a new terminal and test:

```bash
curl -X POST http://localhost:3000/api/chat \
  -H "Content-Type: application/json" \
  -d "{\"message\":\"Hello Doctor Know\"}"
```

You should get a JSON response with Doctor Know's reply.

### 6. Update Frontend to Use Backend

The frontend code will be updated to call your backend instead of using the rule-based system.

## Troubleshooting

### "Cannot find module 'express'"
Run: `npm install`

### "Invalid API key"
- Check your API key in server.js
- Make sure you copied the full key
- Verify at https://platform.openai.com/api-keys

### "Port 3000 already in use"
Change PORT in server.js to 3001 or another number

### "Insufficient quota"
- Add payment method at https://platform.openai.com/account/billing
- Check usage at https://platform.openai.com/usage

## Cost Estimate

- GPT-3.5-turbo: ~$0.002 per conversation
- GPT-4: ~$0.03 per conversation
- 100 conversations/day with GPT-3.5: ~$6/month

## Next Steps

Once the backend is running:
1. Keep this terminal open (server must run)
2. Open your index.html in browser
3. Click the microphone and start talking
4. Doctor Know will respond using ChatGPT!

## Production Deployment (Optional)

For production, consider:
- Deploy to Heroku, Railway, or Render
- Use environment variables for API key
- Add rate limiting
- Use a database for conversation history
- Add user authentication

## Support

If you encounter issues:
1. Check the terminal for error messages
2. Verify your API key is correct
3. Ensure Node.js is installed: `node --version`
4. Check OpenAI status: https://status.openai.com
