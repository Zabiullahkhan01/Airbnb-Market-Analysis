# Data Dictionary - Airbnb Seattle Analysis

## Overview
This document provides detailed descriptions of all data fields used in the Airbnb Seattle Market Analysis project.

## Dataset Information

### Source Files:
- **listings.csv**: Property listing details and specifications
- **calendar.csv**: Daily pricing and availability data
- **reviews.csv**: Customer review and rating information

---

## 📋 Listings Dataset Fields

| Field Name | Data Type | Description | Example Values |
|------------|-----------|-------------|----------------|
| `id` | Integer | Unique identifier for each property listing | 241032, 953595 |
| `name` | Text | Property title/name as listed by host | "Bright and Airy Studio" |
| `host_id` | Integer | Unique identifier for property host | 14266821, 30283594 |
| `host_name` | Text | Name of the property host | "John", "Sarah" |
| `neighbourhood_group` | Text | Borough or district name | Not used in Seattle data |
| `neighbourhood` | Text | Specific neighborhood name | "Capitol Hill", "Ballard" |
| `latitude` | Float | Geographic latitude coordinate | 47.6205, 47.6815 |
| `longitude` | Float | Geographic longitude coordinate | -122.3493, -122.3837 |
| `room_type` | Text | Type of accommodation offered | "Entire home/apt", "Private room" |
| `price` | Currency | Nightly rate in USD | $85.00, $150.00 |
| `minimum_nights` | Integer | Minimum stay requirement | 1, 3, 7 |
| `number_of_reviews` | Integer | Total review count for property | 0, 45, 127 |
| `last_review` | Date | Date of most recent review | 2016-12-25, 2016-08-15 |
| `reviews_per_month` | Float | Average reviews received monthly | 1.5, 3.2 |
| `calculated_host_listings_count` | Integer | Number of listings by same host | 1, 5, 12 |
| `availability_365` | Integer | Days available in next 365 days | 0-365 |
| `zipcode` | Text | Postal zip code | "98102", "98109" |
| `bathrooms` | Float | Number of bathrooms | 1.0, 1.5, 2.0 |
| `bedrooms` | Integer | Number of bedrooms | 0, 1, 2, 3, 4, 5, 6, 7 |
| `beds` | Integer | Number of beds available | 1, 2, 4 |
| `property_type` | Text | Type of property | "House", "Apartment", "Condominium" |
| `weekly_price` | Currency | Price for 7-night stay | $595.00, $1050.00 |
| `monthly_price` | Currency | Price for 30-night stay | $2550.00, $4500.00 |
| `security_deposit` | Currency | Refundable security deposit | $100.00, $300.00 |
| `cleaning_fee` | Currency | One-time cleaning charge | $25.00, $75.00 |

---

## 📅 Calendar Dataset Fields

| Field Name | Data Type | Description | Example Values |
|------------|-----------|-------------|----------------|
| `listing_id` | Integer | Foreign key linking to listings.id | 241032, 953595 |
| `date` | Date | Specific calendar date | 2016-01-01, 2016-12-31 |
| `available` | Boolean | Availability status (t/f) | t, f |
| `price` | Currency | Daily rate for this date | $85.00, $150.00 |

### Key Notes:
- **available = 't'**: Property available for booking
- **available = 'f'**: Property booked or unavailable
- **price**: May vary from base listing price due to seasonal adjustments

---

## 💬 Reviews Dataset Fields

| Field Name | Data Type | Description | Example Values |
|------------|-----------|-------------|----------------|
| `listing_id` | Integer | Foreign key linking to listings.id | 241032, 953595 |
| `id` | Integer | Unique identifier for each review | 362692, 4724140 |
| `date` | Date | Date when review was posted | 2016-01-15, 2016-11-30 |
| `reviewer_id` | Integer | Unique identifier for reviewer | 1014642, 30545421 |
| `reviewer_name` | Text | Name of person who wrote review | "Michael", "Jennifer" |
| `comments` | Text | Full text of customer review | "Great place, highly recommend!" |

---

## 🔗 Data Relationships

### Primary Relationships:
- **listings.id** ↔ **calendar.listing_id** (One-to-Many)
- **listings.id** ↔ **reviews.listing_id** (One-to-Many)

### Key Constraints:
- Each listing can have multiple calendar entries (365 days)
- Each listing can have multiple reviews
- All calendar and review records must have valid listing_id reference

---

## 📊 Calculated Fields Used in Analysis

### Dashboard Metrics:

| Calculated Field | Formula/Logic | Purpose |
|------------------|---------------|---------|
| **Average Price by Zip Code** | AVG([Price]) grouped by [Zipcode] | Identify premium locations |
| **Revenue by Week** | SUM([Price]) grouped by WEEK([Date]) | Seasonal trend analysis |
| **Bedroom Category** | Converted [Bedrooms] to Dimension | Property size segmentation |
| **Competition Index** | COUNT(DISTINCT([Id])) by [Bedrooms] | Market saturation analysis |
| **Geographic Coordinates** | [Latitude], [Longitude] for mapping | Spatial visualization |

### Data Quality Filters:
- **Non-null Zip Codes**: Excludes records without location data
- **Valid Price Range**: Removes $0 prices and extreme outliers
- **Complete Listings**: Requires bedroom and bathroom information
- **2016 Data Only**: Filters to single year for consistency

---

## 🚨 Data Quality Notes

### Known Issues:
1. **Missing Zip Codes**: ~5% of listings lack zip code information
2. **Zero Bedrooms**: Some studio apartments coded as 0 bedrooms
3. **Price Variations**: Calendar prices may differ from listing base price
4. **Incomplete Reviews**: Not all stays result in reviews

### Data Cleaning Applied:
- Removed records with null zip codes for geographic analysis
- Converted bedroom count from measure to dimension
- Filtered out zero-bedroom properties for bedroom analysis
- Standardized price formatting across datasets

---

## 📈 Business Intelligence Context

### Key Performance Indicators (KPIs):
- **Average Nightly Rate**: Primary revenue metric
- **Market Competition**: Listing density by property type
- **Seasonal Variation**: Revenue fluctuation percentages
- **Geographic Premium**: Price differential by location
- **Property Size ROI**: Revenue correlation with bedroom count

### Strategic Metrics:
- **Investment Opportunity Score**: Combination of high price + low competition
- **Seasonal Revenue Index**: Peak vs. off-peak revenue ratios
- **Market Penetration**: Host concentration analysis
- **Location Premium Factor**: Zip code price ranking relative to median

---

*This data dictionary supports the Airbnb Seattle Market Analysis Dashboard and provides essential context for understanding the analytical framework and business insights generated.*