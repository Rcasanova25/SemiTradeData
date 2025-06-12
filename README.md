# SemiTradeData# 📊 Semiconductor Trade Analysis Dashboard

A comprehensive Streamlit dashboard for analyzing US semiconductor trade data using official government sources.

## 🚀 Live Demo

**[View Dashboard](https://your-dashboard-name.streamlit.app)** *(Replace with your actual URL after deployment)*

## 📖 Overview

This dashboard provides in-depth analysis of US semiconductor trade flows using:

- **Census Bureau International Trade API** - Real-time trade statistics
- **HS Classification System** - Product-based trade codes (8541, 8542)
- **NAICS Classification System** - Industry-based manufacturing codes (334413)
- **USITC DataWeb Validation** - Cross-referenced with official totals

### Key Features

✅ **Real-time Data** - Live API connections to Census Bureau  
✅ **Dual Classification** - Compare HS (products) vs NAICS (industries)  
✅ **Trade Flow Analysis** - Separate exports and imports analysis  
✅ **Geographic Breakdown** - Country-level trade partner analysis  
✅ **Official Validation** - Cross-validated with USITC DataWeb  
✅ **Interactive Charts** - Dynamic visualizations and trends  
✅ **Data Download** - Export analysis results to CSV  

## 🔧 Installation & Setup

### Prerequisites

- Python 3.8+
- Census Bureau API Key (free from [api.census.gov](https://api.census.gov/data/key_signup.html))

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/semiconductor-dashboard.git
   cd semiconductor-dashboard
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   ```bash
   # Option 1: Environment variable
   export CENSUS_API_KEY="your_api_key_here"
   
   # Option 2: Streamlit secrets (recommended)
   # Create .streamlit/secrets.toml and add:
   # CENSUS_API_KEY = "your_api_key_here"
   ```

4. **Run locally:**
   ```bash
   streamlit run dashboard1.py
   ```

## 🌐 Deployment

### Streamlit Community Cloud (Recommended)

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Deploy on Streamlit Cloud:**
   - Go to [share.streamlit.io](https://share.streamlit.io)
   - Connect your GitHub account
   - Select this repository
   - Add your API key in the secrets section:
     ```toml
     CENSUS_API_KEY = "your_actual_api_key"
     ```

3. **Your app will be live at:**
   `https://your-app-name.streamlit.app`

### Alternative Deployment Options

- **Heroku**: See deployment guide in `/docs/heroku-deployment.md`
- **Railway**: See deployment guide in `/docs/railway-deployment.md`
- **Google Cloud**: See deployment guide in `/docs/gcp-deployment.md`

## 📊 Data Sources

### Primary Sources
- **Census Bureau API** - Official US trade statistics
- **USITC DataWeb** - Validated trade totals  
- **USA Trade Online** - NAICS manufacturing data

### Classification Systems
- **HS 8541** - Diodes, transistors, semiconductors
- **HS 8542** - Electronic integrated circuits  
- **NAICS 334413** - Semiconductor manufacturing

### Coverage
- **Time Period**: 2013-2024
- **Geographic Coverage**: 205+ countries
- **Update Frequency**: Monthly (API), Annual (validation)

## 🔍 Key Analyses

### Trade Flow Comparison
Compare semiconductor products (HS) vs manufacturing (NAICS):
- Export flows: US → World
- Import flows: World → US  
- Trade balance trends
- Year-over-year analysis

### Geographic Analysis
- Top trading partners by volume
- Country-level trade relationships
- Regional trade patterns
- Market concentration analysis

### Data Validation
- Census API vs USITC DataWeb comparison
- HS vs NAICS correlation analysis
- Official benchmark validation
- Data quality assessment

## 📈 Dashboard Sections

1. **Data Source Selection** - Choose HS, NAICS, or both
2. **Parameter Configuration** - Set years, trade types, filters
3. **Real-time Data Fetch** - Live API data retrieval
4. **Trade Trend Analysis** - Interactive charts and visualizations
5. **Geographic Breakdown** - Country-level analysis
6. **Cross-Validation** - Official data comparison
7. **Data Export** - Download results for further analysis

## 🛠️ Technical Architecture

### Backend
- **Streamlit** - Web application framework
- **Pandas** - Data manipulation and analysis
- **Requests** - API client for Census Bureau
- **Matplotlib** - Data visualization

### API Integration
- **Rate Limiting** - Prevents API quota issues
- **Caching** - 1-hour TTL for improved performance
- **Error Handling** - Robust API failure recovery
- **Progress Tracking** - Real-time fetch status

### Performance Optimizations
- **@st.cache_data** - Function-level caching
- **Rate limiting** - API request throttling
- **Lazy loading** - On-demand data fetching
- **Progress indicators** - User experience optimization

## 📚 Usage Guide

### Basic Analysis
1. Select "HS Codes" for product analysis
2. Choose 2021-2023 for recent trends
3. Include both exports and imports
4. Click "Fetch Complete Trade Data"

### Advanced Comparison
1. Select "Both HS and NAICS"
2. Compare product vs manufacturing data
3. Analyze correlation patterns
4. Validate against official benchmarks

### Geographic Deep Dive
1. Set "Top Countries" to 20
2. Review country breakdown tables
3. Download country summary data
4. Analyze regional patterns

## 🐛 Troubleshooting

### Common Issues

**API Key Errors:**
- Verify key at [api.census.gov](https://api.census.gov/data/key_signup.html)
- Check secrets configuration
- Ensure key has proper permissions

**No Data Returned:**
- Try different year ranges (2020-2022)
- Start with exports only
- Check API rate limits
- Verify internet connectivity

**Performance Issues:**
- Clear Streamlit cache
- Reduce year range
- Limit number of countries
- Check system resources

### Debug Mode
Enable debug mode in the sidebar to see:
- API response details
- Column structure information
- Data processing steps
- Missing country codes

## 🤝 Contributing

Contributions welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

### Reporting Issues
- Use GitHub Issues
- Include error messages
- Provide reproduction steps
- Attach screenshots if helpful

## 📄 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **US Census Bureau** - Trade statistics API
- **USITC** - Official trade validation data
- **Streamlit** - Application framework
- **US Trade Representative** - Classification guidance

## 📞 Support

- **Documentation**: [GitHub Wiki](https://github.com/yourusername/semiconductor-dashboard/wiki)
- **Issues**: [GitHub Issues](https://github.com/yourusername/semiconductor-dashboard/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/semiconductor-dashboard/discussions)

---

**Built with ❤️ for semiconductor trade analysis**
