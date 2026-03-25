## 🚀 Features

- 📊 **Dashboard Overview**: Real-time stats showing monthly/annual spending
- 💰 **Subscription Management**: Track all your subscriptions in one place with logos
- 📅 **Calendar View**: Visual calendar showing all subscription renewal dates with iCal export and subscription URL
- 📈 **Analytics**: Visualize spending by category and track savings
- 🔔 **Email Notifications**: Get reminders before subscriptions renew
- 📱 **Pushover Notifications**: Receive push notifications on your mobile device
- 📤 **Data Export**: Export your data as CSV, JSON, or iCal format
- 🎨 **Beautiful Themes**: 5 stunning themes including a festive Christmas theme with snowfall animation
- 🌍 **Multi-Currency Support**: Support for USD, EUR, GBP, JPY, RUB, SEK, PLN, INR, CHF, BRL, COP, BDT, and CNY (with optional real-time conversion)
- 🤖 **MCP Server**: AI integration via Model Context Protocol for Claude and other AI assistants
- 🐳 **Docker Ready**: Easy deployment with Docker
- 🔒 **Self-Hosted**: Your data stays on your server
- 📱 **Mobile Responsive**: Optimized mobile experience with hamburger menu navigation

## 🏗️ Tech Stack

- **Backend**: Go with Gin framework
- **Database**: SQLite (no external database needed!)
- **Frontend**: HTMX + Tailwind CSS
- **Deployment**: Docker & Docker Compose

## 🚀 Quick Start

SubTrackr is available as a multi-platform Docker image supporting both AMD64 and ARM64 architectures (including Apple Silicon).

**Note:** SubTrackr works fully out-of-the-box with no external dependencies. The Fixer.io API key is completely optional for currency conversion features.

### Option 1: Docker Compose (Recommended)

1. **Create docker-compose.yml**:

```yaml
version: '3.8'

services:
  subtrackr:
    image: ghcr.io/bscott/subtrackr:latest
    container_name: subtrackr
    ports:
      - "8080:8080"
    volumes:
      - ./data:/app/data
    environment:
      - GIN_MODE=release
      - DATABASE_PATH=/app/data/subtrackr.db
      # Optional: Enable automatic currency conversion (requires Fixer.io API key)
      # - FIXER_API_KEY=your_fixer_api_key_here
    restart: unless-stopped
```

2. **Start the container**:

```bash
docker-compose up -d
```

3. **Access SubTrackr**: Open http://localhost:8080







---

Made with ❤️ by me and Vibing 
