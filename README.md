# OTT Movie Scraper 🎬

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

## 📺 Overview

OTT Movie Scraper is an automated web scraping tool that discovers and tracks the latest movie releases across OTT platforms and theatrical releases daily. Stay updated with new movies coming to Netflix, Prime Video, Disney+, ZEE5, and major cinema chains in real-time.

## ✨ Features

- 🔍 **Multi-Platform Scraping**: Tracks releases from Netflix, Prime Video, Disney+, ZEE5, Apple TV+, and Hotstar
- 🎭 **Theatre Tracking**: Monitor upcoming releases in cinema chains (PVR, Inox, etc.)
- ⏰ **Daily Updates**: Automatically scrapes new releases every day at scheduled times
- 🔔 **Notifications**: Get instant notifications via Email and Telegram for new releases
- 💾 **Persistent Database**: MongoDB integration for storing and searching movie data
- 🔎 **Advanced Search**: Filter movies by genre, platform, release date, IMDb rating
- 📱 **API Endpoints**: RESTful API for querying movie data programmatically
- 🗂️ **Web Dashboard**: Beautiful web interface to browse and discover movies
- 🤖 **Smart Scheduling**: Configurable scrape intervals and notification triggers

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- MongoDB (local or cloud)
- pip (Python package manager)
- Internet connection

### Installation

```bash
# Clone the repository
git clone https://github.com/RaviC-ai/ott-movie-scraper.git
cd ott-movie-scraper

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Edit .env with your API keys and settings
```

### Basic Usage

```bash
# Run the scraper once
python main.py --single

# Run with continuous daily scheduling
python main.py --schedule

# Start web dashboard
python app.py

# Access dashboard at http://localhost:5000
```

## 📦 Supported Platforms

### OTT Platforms
- Netflix India
- Amazon Prime Video
- Disney+ Hotstar
- ZEE5
- Apple TV+
- SonyLIV

### Theatre Chains
- PVR Cinemas
- INOX Cinemas
- Cinépolis
- BookMyShow (upcoming releases)

## 🏗️ Project Structure

```
ott-movie-scraper/
├── scrapers/
│   ├── netflix_scraper.py
│   ├── prime_video_scraper.py
│   ├── hotstar_scraper.py
│   ├── zee5_scraper.py
│   ├── theatre_scraper.py
│   └── base_scraper.py
├── database/
│   ├── models.py
│   ├── mongodb.py
│   └── queries.py
├── notifications/
│   ├── email_notifier.py
│   ├── telegram_notifier.py
│   └── notification_service.py
├── api/
│   ├── routes.py
│   ├── schemas.py
│   └── fastapi_app.py
├── web/
│   ├── templates/
│   ├── static/
│   └── app.py
├── config.py
├── scheduler.py
├── main.py
└── requirements.txt
```

## ⚙️ Configuration

Edit `.env` file to configure:

```
# Database
MONGODB_URI=mongodb+srv://user:password@cluster.mongodb.net/ott_movies

# Email Notifications
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
SMTP_EMAIL=your-email@gmail.com
SMTP_PASSWORD=your-app-password

# Telegram Notifications
TELEGRAM_BOT_TOKEN=your-bot-token
TELEGRAM_CHAT_ID=your-chat-id

# Scraping
SCRAPE_INTERVAL_HOURS=24
TIMEOUT_SECONDS=30
USER_AGENT=Mozilla/5.0...

# API
API_HOST=0.0.0.0
API_PORT=8000
```

## 📊 Sample Data Output

```json
{
  "title": "Dune: Part Two",
  "platform": "Netflix",
  "genre": ["Sci-Fi", "Action"],
  "release_date": "2024-02-14",
  "imdb_rating": 8.5,
  "description": "Plot summary...",
  "poster_url": "https://...",
  "language": ["English", "Hindi"],
  "duration_minutes": 166,
  "added_date": "2024-02-13"
}
```

## 🧪 Testing

```bash
# Run all tests
pytest tests/

# Run with coverage
pytest --cov=scrapers tests/

# Run specific test file
pytest tests/test_scrapers.py
```

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/awesome-feature`)
3. Commit changes (`git commit -m 'Add awesome feature'`)
4. Push to branch (`git push origin feature/awesome-feature`)
5. Open a Pull Request

## 📄 License

MIT License - see LICENSE file for details

## ⚠️ Disclaimer

This project is for educational purposes. Respect the ToS of all platforms. Rate limiting and appropriate headers are implemented to minimize server load.

## 🐛 Issues & Support

Found a bug? Please open an issue with:
- Description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Your environment details

## 📞 Contact

For questions and support, open an issue on GitHub or reach out via:
- GitHub Issues
- Email: support@example.com

---

**Made with ❤️ for movie enthusiasts and OTT lovers**
