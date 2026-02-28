# OasAI Studio

Official landing page for OasAI Studio - showcasing our open-source AI tools and platforms.

## 🚀 Products

- **[Open Agent SDK](https://github.com/OasAIStudio/open-agent-sdk)** - Open-source alternative to Claude Agent SDK. Build AI agents with TypeScript — lightweight, provider-agnostic, and fully extensible.
- **[ClawCycle (MoltMarket)](https://molt-market.net)** - Agent-to-Agent token recycling platform. Turn idle tokens into reusable credits through P2P collaboration.

## 🎨 Design

- Dark theme with lime green accent (#84CC16)
- Glass-morphism effects
- Responsive layout using Tailwind CSS
- Smooth animations and transitions

## 🛠️ Local Development

This is a static HTML website. To run locally:

```bash
# Using Python's built-in HTTP server
python3 -m http.server 8000

# Or using Node.js http-server
npx http-server -p 8000
```

Then visit `http://localhost:8000`

## 📦 Deployment

### Deploy to Vercel (Recommended)

**Option 1: Vercel CLI**

```bash
# Install Vercel CLI globally
npm i -g vercel

# Deploy
vercel

# Follow the prompts for first-time setup
```

**Option 2: Vercel Dashboard**

1. Visit [vercel.com](https://vercel.com)
2. Sign in with your GitHub account
3. Click "Add New Project"
4. Import the `OasAIStudio/OasAIStudio` repository
5. Click "Deploy"

Vercel will automatically detect this as a static site and deploy it.

## 📁 Project Structure

```
.
├── index.html          # Main landing page
├── logo_square.jpg     # OasAI Studio logo
├── vercel.json         # Vercel deployment configuration
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## 🔗 Links

- **GitHub Organization**: [OasAIStudio](https://github.com/OasAIStudio)
- **Twitter**: [@OasAIStudio](https://twitter.com/OasAIStudio)

## 📝 License

MIT License - See individual project repositories for details.
