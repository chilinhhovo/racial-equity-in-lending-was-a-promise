# Quick Start Guide: HMDA Thesis Analysis

## 🚀 Getting Started in 5 Minutes

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/hmda-thesis-github.git
cd hmda-thesis-github
```

### 2. View the Interactive Thesis
- Open `index.html` in your web browser
- No server setup required - works locally!
- All charts and visualizations are interactive

### 3. Explore the Data
- **CSV Files**: Located in `data/` directory
- **Key Datasets**: 
  - `race_approval_rates_by_state_year.csv` - State-level approval rates
  - `bank_race_summary.csv` - Bank-specific disparities
  - `bank_nonbank_interest_rate_by_race_year.csv` - Interest rate analysis
  - `bloomberg_scraped_structured.csv` - Bloomberg financial data

### 4. Run the Analysis Notebooks
```bash
# Install Python dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/
```

## 📊 What You'll Find

### Interactive Visualizations
- **Bank Approval Rate Charts**: White vs Black approval gaps over time
- **State Comparison Maps**: Geographic lending disparities
- **Interest Rate Analysis**: Bank vs non-bank lending costs
- **Temporal Trends**: Year-over-year changes in commitments

### Key Findings
- **JPMorgan Chase**: 6 percentage point approval gap
- **Geographic Patterns**: Highest gaps in Mississippi, Louisiana, Arkansas
- **Policy Impact**: Executive order rollback of diversity programs
- **Lender Shifts**: Non-banks filling gaps but charging higher fees

## 🔧 Development Setup

### Prerequisites
- **Python 3.8+**: For data analysis and notebooks
- **Modern Browser**: Chrome, Firefox, Safari, Edge
- **Git**: For version control

### Local Development
```bash
# Install dependencies
pip install -r requirements.txt

# Start local server (optional)
python -m http.server 8000
# Then visit http://localhost:8000
```

### Data Updates
1. Replace CSV files in `data/` directory
2. Update file paths in `index.html` if needed
3. Test all visualizations with new data

## 📁 Project Structure

```
hmda-thesis-github/
├── index.html                 # 🎯 Main interactive thesis
├── assets/                    # 🖼️  Images, charts, maps
├── data/                      # 📊 All CSV data files
├── notebooks/                 # 📓 Jupyter analysis notebooks
├── docs/                      # 📚 Documentation
├── README.md                  # 📖 Project overview
└── requirements.txt           # 🐍 Python dependencies
```

## 🎯 Key Features

### Responsive Design
- Works on all devices (desktop, tablet, mobile)
- Touch-friendly interactions
- Adaptive layouts

### Interactive Elements
- Hover tooltips with detailed information
- Zoom and pan on maps
- Responsive charts that resize

### Data-Driven
- Real HMDA data (15+ million records)
- Live CSV loading
- Fallback data for offline use

## 🚨 Troubleshooting

### Charts Not Loading?
- Check browser console for errors
- Ensure CSV files are in `data/` directory
- Verify file paths in `index.html`

### Data Not Displaying?
- Check CSV file format (should have headers)
- Verify column names match expected format
- Look for console error messages

### Mobile Issues?
- Use modern mobile browser
- Check responsive design settings
- Test with different screen sizes

## 📚 Next Steps

### For Researchers
1. Review methodology in `docs/METHODOLOGY.md`
2. Examine Jupyter notebooks for analysis details
3. Use data for your own research projects

### For Developers
1. Customize charts and visualizations
2. Add new interactive features
3. Integrate with other data sources

### For Educators
1. Use as case study in courses
2. Adapt visualizations for classroom use
3. Create assignments based on the data

## 🤝 Contributing

### How to Help
- Report bugs or issues
- Suggest improvements to visualizations
- Add new data sources or analysis
- Improve documentation

### Code Standards
- Clean, readable HTML/CSS/JavaScript
- Comprehensive commenting
- Error handling for data loading
- Responsive design principles

## 📞 Support

### Getting Help
- Check the documentation in `docs/`
- Review Jupyter notebooks for analysis details
- Look at browser console for error messages
- Examine the README for project overview

### Reporting Issues
- Use GitHub Issues for bug reports
- Include browser and device information
- Provide steps to reproduce problems
- Share relevant error messages

---

**Ready to explore?** Open `index.html` in your browser and start exploring the interactive thesis on racial equity in lending!
