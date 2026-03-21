# 🚀 README Integration Setup Guide

## 🎵 Spotify Integration Setup

### Step 1: Get Spotify Credentials
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Get `Client ID` and `Client Secret`
4. Add `http://localhost:3000` to redirect URIs

### Step 2: Get Refresh Token
1. Visit: `https://accounts.spotify.com/authorize?client_id=YOUR_CLIENT_ID&response_type=code&scope=user-read-currently-playing user-read-recently-played&redirect_uri=http://localhost:3000&state=123`
2. Copy the `code` from URL
3. Get refresh token using curl:
```bash
curl -X POST "https://accounts.spotify.com/api/token" \
     -H "Authorization: Basic BASE64(CLIENT_ID:CLIENT_SECRET)" \
     -d "grant_type=authorization_code&code=CODE&redirect_uri=http://localhost:3000"
```

### Step 3: Add to GitHub Secrets
- `SPOTIFY_CLIENT_ID`
- `SPOTIFY_CLIENT_SECRET` 
- `SPOTIFY_REFRESH_TOKEN`

### Step 4: Update README
Replace `your_spotify_id` with your actual Spotify User ID

---

## 🐍 Contribution Snake Setup

### Automatic Setup
The GitHub Actions will automatically:
1. Generate snake SVG daily
2. Push to `output` branch
3. Update README references

### Manual Trigger
Go to Actions → "Generate Snake" → "Run workflow"

---

## 📊 WakaTime Integration

### Step 1: Install WakaTime
```bash
pip install wakatime
```

### Step 2: Configure IDE
- VS Code: Install WakaTime extension
- Enter your API key from [wakatime.com](https://wakatime.com)

### Step 3: Make Profile Public
1. Go to [WakaTime Settings](https://wakatime.com/settings)
2. Enable "Public profile"
3. Your username should be `yetemgetaB`

---

## 🔧 Customization Options

### Spotify Themes
- `novatorem` (default)
- `default`
- `dracula`
- `ocean`

### Snake Colors
Edit the workflow to change colors:
```yaml
palette: github-dark  # or github-light, monokai, etc.
```

### Update Frequency
- Spotify: Every hour
- Snake: Every 24 hours
- Stats: Real-time

---

## 🚀 Advanced Features

### Add More Badges
```markdown
![Custom Badge](https://img.shields.io/badge/TEXT-COLOR?style=flat-square&logo=ICON)
```

### Add Blog Feed
```markdown
[![Blog](https://img.shields.io/badge/Blog-Your%20Blog%20Name-blue)](https://yourblog.com)
```

### Add Project Carousel
```markdown
[![Project 1](https://github-readme-stats.vercel.app/api/pin/?username=USERNAME&repo=REPO1&theme=github_dark)](LINK1)
[![Project 2](https://github-readme-stats.vercel.app/api/pin/?username=USERNAME&repo=REPO2&theme=github_dark)](LINK2)
```

---

## 📱 Mobile Optimization

All components are responsive and will work on mobile devices.

---

## 🎯 Performance Tips

1. Use `lazy` loading for heavy images
2. Cache external API calls
3. Optimize image sizes
4. Use CDN for static assets

---

## 🔄 Troubleshooting

### Spotify Not Working
- Check secrets are correct
- Verify refresh token is valid
- Ensure Spotify account is active

### Snake Not Generating
- Check Actions tab for errors
- Verify workflow permissions
- Ensure `output` branch exists

### Stats Not Loading
- Verify WakaTime profile is public
- Check username spelling
- Ensure API key is valid
