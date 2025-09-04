# Airbnb Seattle Market Analysis Dashboard

[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)](https://public.tableau.com/profile/yourprofile)
[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourusername)

> **Interactive Business Intelligence Dashboard analyzing Seattle's Airbnb market to guide property investment decisions through data-driven insights.**

## 📊 Project Overview

This project demonstrates end-to-end data analysis capabilities by transforming Seattle Airbnb market data into actionable business intelligence. Created for potential property investors seeking optimal investment opportunities, the dashboard combines multiple datasets to reveal pricing patterns, seasonal trends, and market competition dynamics.

### 🎯 Business Problem
**Objective:** Help potential Airbnb investors identify the most profitable property investment opportunities in Seattle's competitive short-term rental market.

**Key Questions Addressed:**
- Which neighborhoods generate the highest rental rates?
- What are the seasonal revenue patterns throughout the year?
- How does property size impact pricing and market demand?
- Where is the competition density across different property types?

## 🛠️ Technical Stack

| **Category** | **Tools & Technologies** |
|--------------|-------------------------|
| **Data Visualization** | Tableau Desktop, Tableau Public |
| **Data Processing** | Microsoft Excel, CSV handling |
| **Data Management** | Multi-table joins, Data validation |
| **Analytics** | Statistical analysis, Trend analysis |
| **Business Intelligence** | KPI development, Interactive dashboards |

## 📁 Repository Structure

```
airbnb-seattle-analysis/
├── documentation/
│   ├── data_dictionary.md         # Data field descriptions
│   ├── methodology.md             # Analysis methodology
│   └── business_recommendations.md # Key findings and recommendations
|
├── Airbnb market analysis dashboard.twb      #Tableau dashboard
│
├── Airbnb-Seattle-Dataset.xlsx            #raw dataset
│
├── Dashboard Screenshot.png           # Screenshot of final dashboard
|
├── README.md                      # readme file
└── LICENSE                       # MIT License
```

## 🔍 Data Overview

### **Dataset Details**
- **Source:** Seattle Airbnb Open Data (2016)
- **Size:** 23+ million data points across 3 datasets
- **Records:** 3,600+ unique property listings
- **Geographic Coverage:** 100+ Seattle zip codes

### **Data Sources:**
1. **Listings Dataset** (3,600+ records)
   - Property details, location, amenities
   - Pricing structure, property specifications
   - Host information and property types

2. **Calendar Dataset** (1.4M+ records)
   - Daily pricing and availability
   - Booking status and seasonal patterns
   - Revenue tracking over time

3. **Reviews Dataset** (84K+ records)
   - Customer feedback and ratings
   - Review dates and guest experiences
   - Quality indicators

## 🎨 Dashboard Features

### **Interactive Visualizations:**

1. **📍 Price by Zip Code Bar Chart**
   - Horizontal bar chart ranking neighborhoods by average nightly rate
   - Color-coded for easy identification of premium markets
   - Shows price range from $68 to $206 per night

2. **🗺️ Geographic Price Distribution Map**
   - Interactive Seattle map with color-coded zip codes
   - Hover functionality showing exact prices and locations
   - Visual correlation between location and pricing

3. **📈 Seasonal Revenue Analysis**
   - Time-series line chart showing weekly revenue trends
   - Identifies peak seasons (summer and holidays)
   - Reveals 40-60% revenue fluctuations throughout the year

4. **🏠 Bedroom Count vs. Average Price**
   - Comparative analysis showing pricing by property size
   - Demonstrates 3x revenue potential for larger properties
   - Clear market segmentation insights

5. **📊 Market Competition Analysis**
   - Bar chart showing listing density by bedroom count
   - Reveals opportunity gaps in larger property segments
   - Competitive landscape overview

## 🔑 Key Findings

### **💰 Premium Market Identification**
- **Zip Code 98134** commands highest rates at **$206/night** (50% premium)
- **Top 5 zip codes** generate 40% higher revenue than market average
- **Waterfront and downtown locations** show consistent premium pricing

### **📅 Seasonal Patterns**
- **Summer months (June-August):** 60% higher revenue
- **Holiday seasons:** 40-50% revenue spike
- **January-February:** Lowest demand period (optimal for maintenance)

### **🏘️ Property Size ROI Analysis**
- **5-6 bedroom properties:** Generate 3x higher nightly rates
- **Large properties:** Face minimal competition (20 vs 1,800 listings)
- **Sweet spot:** 4+ bedrooms for optimal ROI

### **🎯 Investment Recommendations**
1. **Target premium zip codes** (98134, 98121, 98101) for location advantage
2. **Invest in 4-6 bedroom properties** for maximum revenue potential
3. **Focus on summer/holiday rental strategy** for peak profitability
4. **Consider larger properties** to avoid market saturation

## 🚀 Technical Implementation

### **Data Processing Workflow:**
1. **Data Integration:** Successfully joined 3 disparate CSV files
2. **Quality Control:** Handled null values, data type conversions, duplicates
3. **Performance Optimization:** Reduced dataset from 23M to <15M rows
4. **Relationship Modeling:** Proper foreign key relationships established

### **Advanced Tableau Techniques:**
- **Calculated Fields:** Custom metrics and KPI calculations
- **Parameters:** Interactive filtering and dynamic analysis
- **Dashboard Actions:** Cross-filtering between visualizations
- **Geographic Mapping:** Custom geocoding and spatial analysis
- **Color Coordination:** Consistent color schemes across all views

## 📊 Live Dashboard

**🔗 [View Interactive Dashboard on Tableau Public]([https://public.tableau.com/profile/yourprofile](https://public.tableau.com/app/profile/zabiullah.khan6526/viz/Airbnbmarketanalysisdashboard/Dashboard3?publish=yes))**

### Dashboard Screenshots:

![Dashboard Overview](Dashboard-Screenshot.png)
*Main dashboard showing all key visualizations*

## 🎯 Business Impact

### **Strategic Value Delivered:**
- **Investment Framework:** Clear criteria for property selection
- **Risk Mitigation:** Seasonal revenue planning and market timing
- **Competitive Intelligence:** Market gap identification and opportunity assessment
- **ROI Optimization:** Data-driven pricing and property type recommendations

### **Stakeholder Benefits:**
- **Investors:** Reduced investment risk through data-driven decisions
- **Real Estate Agents:** Market insights for client advisory
- **Property Managers:** Pricing optimization strategies
- **Urban Planners:** Market demand understanding

## 🔧 How to Use This Repository

### **Prerequisites:**
- Tableau Desktop (for .twbx files) or Tableau Public account
- Microsoft Excel (for data files)
- Basic understanding of data analysis concepts

### **Getting Started:**

1. **Clone the Repository:**
```bash
git clone https://github.com/yourusername/airbnb-seattle-analysis.git
cd airbnb-seattle-analysis
```


3. **Open Tableau Dashboard:**
- Launch Tableau Desktop
- Open `tableau/airbnb_dashboard.twbx`
- Explore interactive features and filters

4. **Review Documentation:**
- Read `documentation/methodology.md` for analysis approach
- Check `documentation/data_dictionary.md` for field definitions
- Review `documentation/business_recommendations.md` for insights

## 🎓 Skills Demonstrated

### **Data Analysis:**
- Multi-source data integration and joining
- Statistical analysis and trend identification
- Geographic data analysis and mapping
- Time-series analysis and seasonal pattern recognition

### **Business Intelligence:**
- KPI development and metric definition
- Market analysis and competitive intelligence
- Strategic recommendation development
- Stakeholder communication through visualization

### **Technical Proficiency:**
- Advanced Tableau dashboard development
- Data modeling and relationship management
- Performance optimization for large datasets
- Interactive visualization design

### **Project Management:**
- End-to-end project execution
- Documentation and reproducibility
- Version control and collaboration
- Professional presentation and communication

## 📈 Future Enhancements

### **Potential Improvements:**
- [ ] **Real-time Data Integration:** Connect to live Airbnb API
- [ ] **Predictive Analytics:** Implement revenue forecasting models
- [ ] **Competitor Analysis:** Add competitive property comparison
- [ ] **Customer Segmentation:** Analyze guest demographics and preferences
- [ ] **ROI Calculator:** Build interactive investment return calculator
- [ ] **Mobile Optimization:** Responsive dashboard design
- [ ] **Advanced Analytics:** Machine learning price prediction models

### **Scalability Options:**
- Extend analysis to other cities (Portland, Vancouver)
- Include additional data sources (walk scores, crime data, transportation)
- Implement automated data refresh and monitoring
- Create executive summary and detailed analytical reports

## 📝 Methodology

### **Analysis Approach:**
1. **Business Understanding:** Defined investment decision framework
2. **Data Preparation:** Cleaned and integrated multiple data sources
3. **Exploratory Analysis:** Identified key patterns and relationships
4. **Visualization Design:** Created intuitive and actionable dashboard
5. **Insight Generation:** Developed strategic recommendations
6. **Validation:** Cross-verified findings across multiple dimensions

### **Quality Assurance:**
- Data validation and consistency checks
- Cross-referencing between different visualizations
- Business logic verification with domain knowledge
- User testing for dashboard functionality

## 🤝 Contributing

This is a portfolio project, but suggestions and feedback are welcome! If you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Data Source:** [Inside Airbnb](http://insideairbnb.com/) for providing open Seattle Airbnb data
- **Inspiration:** Data-driven real estate investment analysis community
- **Tools:** Tableau Public for free dashboard hosting platform

## 📞 Contact & Connect

### **Professional Links:**
- **LinkedIn:** [Your LinkedIn Profile](https://www.linkedin.com/in/zabiullah-khan-2852702ba)
- **Tableau Public:** [Your Tableau Profile]([https://public.tableau.com/profile/yourprofile](https://public.tableau.com/app/profile/zabiullah.khan6526/vizzes))
- **Email:** zabiullah.khan2002@gmail.com

---

**💡 "Transforming data into actionable business insights through professional visualization and strategic analysis."**

---

### 📊 Repository Statistics

![GitHub Stars](https://img.shields.io/github/stars/yourusername/airbnb-seattle-analysis?style=social)
![GitHub Forks](https://img.shields.io/github/forks/yourusername/airbnb-seattle-analysis?style=social)
![GitHub Issues](https://img.shields.io/github/issues/yourusername/airbnb-seattle-analysis)
![Last Commit](https://img.shields.io/github/last-commit/yourusername/airbnb-seattle-analysis)

*Last Updated: September 2024*
