@@ -0,0 +1,145 @@
# Tembo Hotel Project

A comprehensive data analysis and management project for Tembo Hotel, focusing on booking operations, guest management, and hotel services optimization.

## Project Overview

This project contains data analysis and SQL scripts for managing and analyzing hotel booking operations at Tembo Hotel. The project includes data cleaning, validation, and business intelligence insights for improving hotel operations.

## Project Contents

### Files

- **analysis tembo_hotel.sql** - Comprehensive SQL scripts for:
  - Database schema creation for booking management
  - Data cleaning and validation procedures
  - Duplicate detection and removal
  - Data standardization (formatting, trimming, capitalization)
  - Guest information processing
  - Staff and payment method validation
  - Business metrics and reporting queries

- **tembo_hotel_dirty (2).csv** - Raw hotel booking data containing:
  - Booking information (booking ID, dates, nights stayed)
  - Guest details (name, phone, city, nationality)
  - Room information (room number, type, rate)
  - Staff assignments (name, department, salary)
  - Payment details (method, total amount)
  - Service usage and ratings

- **Hotel_Project_Brief (3).docx** - Project documentation and requirements
- **Tembo_Hotel_Analysis.pptx** - Business analysis and insights presentation

## Data Schema

The project manages the following main entity:

### Bookings Staging Table
```sql
booking_id          - Unique booking identifier
guest_name          - Guest's full name
guest_phone         - Guest's contact phone
guest_city          - Guest's city of residence
guest_nationality   - Guest's nationality
room_no             - Assigned room number
room_type           - Type of room (Standard, Deluxe, Suite)
room_rate_per_night - Nightly rate in KES
check_in_date       - Check-in date
check_out_date      - Check-out date
nights_stayed       - Number of nights
staff_name          - Assigned staff member
staff_department    - Staff department (Front Desk, Housekeeping, etc.)
staff_salary        - Staff member's salary
payment_method      - Payment method used (M-Pesa, Cash, Card, Bank Transfer)
booking_status      - Status of booking (Checked Out, Checked In, etc.)
total_amount        - Total booking amount
service_used        - Additional services used (Room Service, Breakfast, etc.)
service_price       - Service charge amount
guest_rating        - Guest satisfaction rating
```

## Data Cleaning Operations

The SQL scripts implement the following data quality improvements:

1. **Duplicate Removal** - Identifies and removes duplicate booking records
2. **Text Formatting** - Standardizes guest names with proper capitalization (INITCAP)
3. **Whitespace Handling** - Removes leading and trailing spaces from all fields
4. **Phone Number Validation** - Standardizes phone number formats
5. **Date Validation** - Ensures date consistency and format compliance
6. **Numerical Validation** - Validates monetary amounts and night counts

## Technologies Used

- **PostgreSQL** - Database management and SQL operations
- **SQL** - Data cleaning, validation, and analysis
- **CSV** - Data import/export format

## Key Metrics

The project enables tracking of:
- Booking occupancy rates
- Revenue per booking and per room type
- Guest satisfaction ratings
- Staff assignment efficiency
- Payment method distribution
- Service utilization rates

## Getting Started

### Prerequisites
- PostgreSQL installed and running
- SQL IDE or command-line tool (psql, pgAdmin, etc.)

### Setup Instructions

1. Create a new database for the hotel project:
```sql
CREATE DATABASE tembo_hotel;
```

2. Import the SQL schema and cleaning scripts:
```bash
psql -U username -d tembo_hotel -f "analysis tembo_hotel.sql"
```

3. Import the CSV data:
```sql
COPY bookings_staging FROM 'tembo_hotel_dirty (2).csv' WITH (FORMAT csv, HEADER true);
```

4. Run the cleaning procedures to ensure data quality

## Usage

The SQL scripts can be used for:
- Loading and validating raw booking data
- Cleaning and standardizing data quality
- Generating business intelligence reports
- Tracking hotel performance metrics
- Managing guest and staff information

## Location

Tembo Hotel is located in Kenya, serving guests from various Kenyan cities including Nairobi, Mombasa, Kisumu, and Eldoret.

## Future Enhancements

Potential improvements to the project:
- Enhanced reporting dashboards
- Automated data validation workflows
- Predictive analytics for occupancy forecasting
- Guest segmentation analysis
- Revenue optimization recommendations

## License

This project is proprietary to Tembo Hotel.

## Contact

For questions or more information about this project, contact user.

---
