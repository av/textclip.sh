# textclip.sh

A simple static webpage that displays text from a URL parameter with a copy-to-clipboard button.

## Usage

`https://textclip.sh?text=your_text_here`

## Local Development

Open `index.html` in your browser, or run a local server:

```bash
python3 -m http.server 8000
```

Then visit: `http://localhost:8000?text=hello`

## Deploy to Cloudflare Pages

1. Create a GitHub repository and push this code
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → Workers & Pages
3. Click "Create application" → "Pages" → "Connect to Git"
4. Select your repository
5. Configure build settings:
   - **Build command**: `exit 0`
   - **Build output directory**: `/`
6. Click "Save and Deploy"
7. Add custom domain `textclip.sh` in project settings
