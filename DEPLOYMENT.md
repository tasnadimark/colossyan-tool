# Deployment Guide

## Deploy Backend to Railway.app (Recommended - Free Tier Available)

### Step 1: Sign Up & Create Project
1. Go to [railway.app](https://railway.app)
2. Sign up with GitHub
3. Click "New Project"
4. Select "Deploy from GitHub repo"
5. Choose `tasnadimark/colossyan-tool`

### Step 2: Configure Environment Variables
1. In Railway dashboard, click on your service
2. Go to "Variables" tab
3. Add environment variable:
   - **Key**: `OPENAI_API_KEY`
   - **Value**: `sk-proj-XS_IFspQeHWMwpOVyBV5a...` (your API key)
4. Add another variable:
   - **Key**: `PORT`
   - **Value**: `3000` (Railway will override this automatically, but good to have)

### Step 3: Deploy
1. Railway will automatically deploy your app
2. Wait for deployment to complete (2-3 minutes)
3. Click "Settings" → "Generate Domain" to get a public URL
4. Your backend URL will be something like: `https://colossyan-tool-production.up.railway.app`

### Step 4: Update Frontend
1. Copy your Railway backend URL
2. Open `index.html`
3. Find line ~599 and replace:
   ```javascript
   : 'https://your-backend-url-here.com';
   ```
   with your Railway URL:
   ```javascript
   : 'https://colossyan-tool-production.up.railway.app';
   ```
4. Save, commit, and push to GitHub:
   ```bash
   git add index.html
   git commit -m "Update backend URL for production"
   git push
   ```

### Step 5: Test
1. Wait 1-2 minutes for GitHub Pages to update
2. Visit https://tasnadimark.github.io/colossyan-tool/
3. Go to Transcript Generator tab
4. Upload a video/audio file
5. Generate transcript - it should work! 🎉

---

## Alternative: Deploy to Render.com

1. Go to [render.com](https://render.com)
2. Sign up and click "New +" → "Web Service"
3. Connect GitHub and select `tasnadimark/colossyan-tool`
4. Configure:
   - **Name**: colossyan-tool
   - **Environment**: Node
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
5. Add environment variable `OPENAI_API_KEY` with your key
6. Click "Create Web Service"
7. Copy the URL and update `index.html` as described above

---

## Alternative: Deploy to Heroku

1. Install Heroku CLI: `brew install heroku` (on Mac)
2. Login: `heroku login`
3. Create app:
   ```bash
   heroku create colossyan-tool
   ```
4. Set environment variable:
   ```bash
   heroku config:set OPENAI_API_KEY=your_api_key_here
   ```
5. Deploy:
   ```bash
   git push heroku main
   ```
6. Get URL: `heroku open`
7. Update `index.html` with the Heroku URL

---

## Testing Locally

Your backend is running locally at http://localhost:3001

The frontend automatically detects localhost and uses the local backend.

## Security Note

- Never commit your `.env` file to Git (it's already in `.gitignore`)
- Use environment variables in production hosting platforms
- Your API key is only stored on the backend server, never exposed to users

