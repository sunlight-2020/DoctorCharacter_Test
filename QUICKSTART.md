# 🚀 Quick Start Guide - Doctor Know with ChatGPT

## What You Need
1. Node.js installed
2. OpenAI API key
3. 5 minutes

## Installation Steps

### 1. Install Node.js (if not installed)
- Download from: https://nodejs.org
- Install and verify: `node --version`

### 2. Get OpenAI API Key
- Go to: https://platform.openai.com/api-keys
- Sign up/Login
- Click "Create new secret key"
- Copy the key (starts with `sk-...`)
- **Add payment method** at: https://platform.openai.com/account/billing

### 3. Install Dependencies
Open terminal in project folder:
```bash
npm install
```

### 4. Add Your API Key
Open `server.js` and replace line 14:
```javascript
apiKey: 'sk-proj-YOUR_KEY_HERE'  // Put your real key here
```

### 5. Start Backend Server
```bash
npm start
```

You should see:
```
🩺 Doctor Know backend running on http://localhost:3000
```

**Keep this terminal open!**

### 6. Open Frontend
- Open `index.html` in your browser
- Click the microphone button
- Allow microphone access
- Start talking!

## Testing

Say: **"Hello Doctor Know"**

Doctor Know should respond with ChatGPT-powered intelligence!

## How It Works

```
You speak → Browser captures audio → Speech-to-Text
    ↓
ChatGPT generates response (via your backend)
    ↓
ElevenLabs speaks response → Lip sync animation
```

## Costs

- **GPT-3.5-turbo**: ~$0.002 per conversation
- **100 conversations**: ~$0.20
- **Very affordable!**

## Troubleshooting

**"Cannot find module"**
→ Run: `npm install`

**"Invalid API key"**
→ Check your key in server.js

**"Port already in use"**
→ Change PORT in server.js to 3001

**No response when speaking**
→ Check browser console (F12)
→ Make sure backend is running
→ Allow microphone permission

## What's Next?

Your Doctor Know now has:
✅ Real ChatGPT intelligence
✅ Natural conversations
✅ Memory of conversation
✅ Doctor Know personality
✅ Voice with lip sync

Enjoy your AI doctor! 🩺
