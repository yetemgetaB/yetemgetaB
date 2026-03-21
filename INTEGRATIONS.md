# 🚀 Working Integrations Setup Guide

## 🎵 Spotify Integration (Novatorem Method)

### Step 1: Fork Novatorem Repository
1. Go to https://github.com/novatorem/novatorem
2. Click "Fork" to create your copy
3. Clone your fork: `git clone https://github.com/yetemgetaB/novatorem.git`

### Step 2: Configure Spotify
1. Go to your forked novatorem repo
2. Go to Settings → Secrets → Actions
3. Add these secrets:
   - `SPOTIFY_CLIENT_ID`: Get from Spotify Developer Dashboard
   - `SPOTIFY_CLIENT_SECRET`: Get from Spotify Developer Dashboard
   - `SPOTIFY_REFRESH_TOKEN`: Get from OAuth flow

### Step 3: Get Spotify Credentials
1. Visit [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create new app
3. Set redirect URI: `https://auth.exerra.io/callback`
4. Get Client ID and Client Secret

### Step 4: Get Refresh Token
1. Visit: `https://auth.exerra.io/spotify?client_id=YOUR_CLIENT_ID`
2. Authorize the app
3. Copy the refresh token from the result

### Step 5: Update README
Replace the Spotify section in your README with:
```markdown
[![Spotify](https://raw.githubusercontent.com/yetemgetaB/novatorem/main/spotify.svg)](https://open.spotify.com/user/yetemgetaB)
```

---

## 🐍 Contribution Snake (Platane Method)

### Step 1: Use Platane Snake Generator
The workflow will automatically:
1. Generate snake SVG from platane/snk
2. Save to output branch
3. Update README references

### Step 2: Manual Trigger (Optional)
1. Go to Actions → "Generate Snake"
2. Click "Run workflow"

### Step 3: Verify Output
Check:
- `https://github.com/yetemgetaB/yetemgetaB/blob/main/output/github-contribution-grid-snake.svg`
- `https://github.com/yetemgetaB/yetemgetaB/blob/main/output/github-contribution-grid-snake-dark.svg`

---

## 📊 WakaTime Integration

### Step 1: Install WakaTime
```bash
# For VS Code
code --install-extension WakaTime.vscode-wakatime

# For other editors: https://wakatime.com/docs/editors
```

### Step 2: Configure
1. Open your editor
2. Enter your API key from wakatime.com
3. Start coding to track time

### Step 3: Make Profile Public
1. Go to https://wakatime.com/settings
2. Enable "Public profile"
3. Set username to "yetemgetaB"

---

## 🔧 GitHub Actions Setup

### Required Permissions
Make sure your repository has:
- ✅ Actions enabled (Settings → Actions)
- ✅ Write permissions for workflows
- ✅ GITHUB_TOKEN with contents: write

### Workflow Files Created
1. `spotify-novatorem.yml` - Spotify updates
2. `snake-generator.yml` - Contribution snake
3. Both will run automatically on schedule

---

## 🎯 Troubleshooting

### Spotify Not Working
- Check secrets in novatorem repo (not this repo)
- Verify Spotify app is correctly configured
- Ensure refresh token is valid
- Check Actions tab in novatorem repo

### Snake Not Generating
- Check Actions tab for errors
- Verify workflow permissions
- Ensure output branch exists
- Check if platane/snk is accessible

### WakaTime Not Showing
- Make sure profile is public
- Verify username spelling
- Check API key is valid
- Ensure you've tracked some coding time

---

## 🚀 Quick Start Checklist

- [ ] Fork novatorem repository
- [ ] Configure Spotify secrets in novatorem repo
- [ ] Install WakaTime in your editor
- [ ] Make WakaTime profile public
- [ ] Push updated README
- [ ] Check Actions tab for workflow status

---

## 📱 Alternative Options

### If Spotify Setup is Too Complex
Use a static badge instead:
```markdown
[![Spotify](https://img.shields.io/badge/Spotify-1DB954?style=flat-square&logo=spotify&logoColor=white)](https://open.spotify.com/user/yetemgetaB)
```

### If Snake Doesn't Work
Use GitHub's built-in activity graph:
```markdown
[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=yetemgetaB&theme=github-dark&hide_border=true&area=true)](https://github.com/ashutosh00710/github-readme-activity-graph)
```

---

## 🎨 Customization

### Spotify Templates
- `classic` (default)
- `compact`
- `minimal`
- `detailed`

### Snake Colors
Edit the workflow to use different themes:
- GitHub dark (default)
- GitHub light
- Monokai
- Dracula
