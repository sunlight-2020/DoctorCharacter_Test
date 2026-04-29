# 🩺 Doctor Know - AI Voice Chat Character

An interactive 3D character with real-time voice conversation powered by AI. Talk to Doctor Know, a philosophical AI from the movie "A.I. Artificial Intelligence"!

## ✨ Features

- **Real-time Voice Chat** - Speak and get AI responses with voice synthesis
- **3D Animated Character** - Lip-sync, mustache animation, procedural eyes
- **Movie-Accurate Personality** - Theatrical, philosophical Doctor Know from A.I. movie
- **Holographic Visual Effects** - Dramatic lighting, pulsing colors, atmospheric fog
- **FREE AI Backend** - Uses Hugging Face API (no payment required)
- **Multiple Render Modes** - Mesh, Points, Wireframe
- **Script Playback** - Pre-recorded monologues

## 🚀 Quick Start

### Prerequisites

- Node.js installed
- Python 3 installed
- Modern web browser (Chrome or Edge recommended)

### Step 1: Install Dependencies

```bash
npm install
```

### Step 2: Start Backend Server

Open a terminal and run:

```bash
npm start
```

You should see:
```
🩺 Doctor Know backend running on http://localhost:3000
📡 Using FREE Hugging Face API - No payment needed!
```

**Keep this terminal running!**

### Step 3: Start Frontend Server

Open a **NEW terminal** (keep the backend running) and run:

```bash
py -m http.server 8000
```

### Step 4: Open in Browser

Go to: **http://localhost:8000**

**Important:** Use **Chrome** or **Edge** for best speech recognition support!

## 🎤 How to Use

1. **Click the microphone button** at the bottom center of the screen
2. **Allow microphone access** when prompted by your browser
3. **Speak** when you see "Listening..." status
4. **Wait** for Doctor Know to respond with voice and animation
5. **Continue the conversation** - click the mic button again to speak

## 🎮 Controls

- **Microphone Button** - Start/stop voice chat
- **Play Script Button** - Play pre-recorded monologue
- **Mesh/Points/Wireframe** - Switch render modes
- **Settings Icon** - Add/manage ElevenLabs API keys
- **Mouse Drag** - Rotate camera
- **Mouse Wheel** - Zoom in/out

## 🔧 Configuration

### ElevenLabs API Keys (for voice synthesis)

The app includes embedded API keys. If you need to add your own:

1. Click the settings icon (⚙️)
2. Enter your ElevenLabs API key
3. Get free keys at: https://elevenlabs.io

### AI Backend (FREE)

The backend uses **FREE Hugging Face API** - no payment required!

To use your own API key:
1. Get free token: https://huggingface.co/settings/tokens
2. Edit `server.js` line 13
3. Replace with your token
4. Restart backend: `npm start`

See `FREE_SETUP.md` for detailed instructions.

## 📁 Project Structure

```
├── index.html              # Main frontend application
├── server.js               # AI backend server (Node.js + Express)
├── package.json            # Node.js dependencies
├── Doctor-Character.gltf   # 3D model file
├── logo.png                # Header logo
├── three.module.js         # Three.js library
├── GLTFLoader.js          # GLTF model loader
├── DRACOLoader.js         # DRACO compression loader
├── FREE_SETUP.md          # Free API setup guide
├── QUICKSTART.md          # Quick start guide
└── SETUP_GUIDE.md         # Detailed setup guide
```

## 🛠️ Troubleshooting

### Speech Recognition Not Working

- **Use Chrome or Edge** (best support for Web Speech API)
- **Allow microphone permission** when prompted
- **Use HTTPS or localhost** (required for microphone access)
- Check browser console (F12) for errors

### Backend Not Responding

- Make sure backend is running: `npm start`
- Check if port 3000 is available
- Look for error messages in the backend terminal
- Test backend: open `test-backend.html` in browser

### No Voice Output

- Check ElevenLabs API key status
- Look for TTS errors in browser console (F12)
- API keys may be blocked due to usage limits
- Add a new API key or wait 24 hours

### ElevenLabs API Errors

If you see "Unusual activity detected" or "Free Tier usage disabled":

1. **Get a paid ElevenLabs subscription** ($5/month) - Most reliable
2. **Use a new ElevenLabs account** with fresh API key
3. **Wait 24 hours** - Block may be temporary

**Note:** AI conversation still works without voice! You'll see responses in the console.

## 🎯 Architecture

```
User Speech → Web Speech API (STT)
    ↓
Backend AI (Hugging Face) → Streaming Response
    ↓
ElevenLabs TTS → Audio + Lip Sync
    ↓
3D Character Animation
```

## 🎬 About Doctor Know

This character is inspired by Doctor Know from the 2001 film "A.I. Artificial Intelligence" directed by Steven Spielberg. Doctor Know is a holographic AI oracle with a theatrical, philosophical personality - wise yet tired, mysterious yet entertaining.

## 📝 Console Logging

The app logs conversations to the browser console:

- **👤 USER SAID:** Your speech input
- **🩺 DOCTOR KNOW REPLIED:** AI response
- **🔊 TTS:** Text-to-speech status

Press **F12** to open the console and see the conversation.

## 🌐 Browser Compatibility

- ✅ Chrome (Recommended)
- ✅ Edge (Recommended)
- ⚠️ Firefox (Limited speech recognition)
- ⚠️ Safari (Limited speech recognition)

## 📄 License

MIT License - Free to use and modify

## 🙏 Credits

- Three.js for 3D rendering
- ElevenLabs for voice synthesis
- Hugging Face for AI backend
- Inspired by "A.I. Artificial Intelligence" (2001)

---

**Enjoy talking to Doctor Know!** 🎭
