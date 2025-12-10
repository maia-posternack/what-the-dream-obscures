# 🚀 Ready to Deploy to Railway!

## ✅ Everything is Configured

Your project is fully configured and ready to deploy with the **complete 158,822 artwork dataset**!

### What's Set Up:
- ✅ Git LFS tracking large files (450MB of data)
- ✅ Railway configuration (`Procfile`, `railway.json`)
- ✅ All dependencies in `requirements.txt`
- ✅ Dynamic port configuration for Railway
- ✅ Full latent space dataset included

### Large Files Being Tracked by Git LFS:
```
embeddings_full.npy      - 233MB
artworks.json            - 121MB
descriptions.json        - 62MB
embeddings_reduced.npy   - 30MB
```

---

## 📤 Step 1: Push to GitHub

### Create GitHub Repository:
1. Go to https://github.com/new
2. Name it: `what-the-dream-obscures` (or any name you like)
3. **DO NOT** initialize with README
4. Click **"Create repository"**

### Push Your Code:
```bash
cd "/Users/maiaposternack/Desktop/afvs 222/CascadeProjects/windsurf-project"

# Add your GitHub repo as remote (replace with YOUR username and repo name)
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub (Git LFS will automatically upload large files)
git push -u origin main
```

**Note:** The push will take 2-5 minutes because Git LFS uploads the 450MB of data to LFS storage.

---

## 🚂 Step 2: Deploy on Railway

### Method A: Deploy via Web (Easiest)

1. Go to https://railway.app/new

2. Click **"Deploy from GitHub repo"**

3. Authorize Railway to access your GitHub (if first time)

4. Select your repository: `what-the-dream-obscures`

5. Railway will automatically:
   - ✅ Detect Python/Flask
   - ✅ Install from `requirements.txt`
   - ✅ Run `python app.py` from `Procfile`
   - ✅ Download Git LFS files
   - ✅ Assign a public URL

6. **Add Environment Variable:**
   - In Railway dashboard, click your service
   - Go to **"Variables"** tab
   - Click **"New Variable"**
   - Add: 
     - Name: `REPLICATE_API_TOKEN`
     - Value: `your_replicate_api_token_here`
   - Click **"Deploy"** to restart with the new variable

7. **Wait for Build (5-10 minutes):**
   - Installing dependencies: ~5 min
   - Downloading LFS files: ~2 min
   - Starting app: ~1 min

8. **Get Your Live URL:**
   - Click **"Settings"** → **"Networking"**
   - You'll see something like: `https://windsurf-project-production.up.railway.app`

### Method B: Deploy via CLI

```bash
# Login (opens browser)
railway login

# Link to new project
railway init

# Deploy
railway up

# Add environment variable
railway variables add REPLICATE_API_TOKEN=your_token_here

# Open in browser
railway open
```

---

## 🎯 After Deployment

Your app will be live at: `https://your-project.up.railway.app`

### Features Working:
- ✅ Browse 158,822 artworks from MoMA
- ✅ Navigate latent space with full dataset
- ✅ Generate AI visualizations with Replicate
- ✅ All interactive features enabled

### Railway Free Tier:
- **Hours:** 500 hours/month (enough for hobby projects)
- **Memory:** 8GB RAM (perfect for your app)
- **Storage:** Includes your 450MB dataset
- **Cost:** $0/month on free tier, ~$5/month if you exceed limits

---

## 📊 Expected Performance

- **Build time:** 5-10 minutes (first deploy only)
- **Cold start:** 2-3 seconds
- **Warm response:** <100ms
- **Memory usage:** ~2GB (with dataset loaded)
- **Deploy size:** ~1.5GB (with dependencies)

---

## 🐛 Troubleshooting

### Build Fails
- Check Railway logs in dashboard
- Common issue: Missing `REPLICATE_API_TOKEN` → add in Variables tab

### "Out of Memory" Error
- Free tier: 8GB RAM (should work)
- If needed: Upgrade to Hobby plan ($5/month, 16GB RAM)

### Git LFS Push Fails
- Make sure you have LFS bandwidth (GitHub: 1GB/month free)
- Alternative: Deploy without pushing to GitHub (see Method B above)

### Railway Can't Download LFS Files
- Railway should auto-detect and download LFS files
- If not, you can manually upload via Railway CLI

---

## 🎉 You're Ready!

**Next Action:** Create your GitHub repo and run the push command above!

Your full dataset is ready to go live on Railway. 🚂

