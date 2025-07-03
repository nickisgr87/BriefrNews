# Brief.r - AI-Powered News Compriser

An intelligent news aggregation website that delivers summarized news from trusted sources worldwide, organized into 5 distinct categories.

## Features

- **5 News Categories**: Pop Culture, Global News, Economy & Stocks, Health & Lifestyle, Sports
- **Editorial Section**: Opinion pieces and in-depth analysis
- **AI-Powered Summarization**: Automatically creates concise summaries using OpenAI GPT-4
- **Auto-Updating**: Fetches fresh news every 15 minutes from RSS feeds
- **Responsive Design**: Works perfectly on desktop and mobile
- **Real-time Search**: Find articles instantly across all categories
- **Market Data**: Live stock market information in the Economy section

## Tech Stack

- **Frontend**: React 18 + TypeScript + Tailwind CSS
- **Backend**: Node.js + Express + TypeScript
- **AI**: OpenAI GPT-4 for summarization and categorization
- **Data**: RSS feeds from Reuters, BBC, CNN, Bloomberg
- **UI Components**: Radix UI + shadcn/ui
- **Build**: Vite

## Quick Deploy to Vercel

1. **Fork this repository** to your GitHub account
2. **Sign up at [vercel.com](https://vercel.com)** with your GitHub account
3. **Import your repository** in Vercel dashboard
4. **Add environment variable**:
   - `OPENAI_API_KEY`: Your OpenAI API key
5. **Deploy** - You'll get a URL like `briefr-news.vercel.app`

## Environment Variables

```env
OPENAI_API_KEY=your_openai_api_key_here
NODE_ENV=production
```

## Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## News Sources

- **Reuters**: World news, business, health, sports, technology
- **BBC News**: Global coverage and breaking news
- **CNN**: Health, sports, and general news
- **Bloomberg**: Financial markets and business news

## Created By

**Nikunjan** - 2025

---

Visit the live site: [briefr-news.vercel.app](https://briefr-news.vercel.app)