# Hotel-Booking-Analysis-PowerBI
Interactive Power BI dashboard analyzing hotel bookings, cancellations, and guests across Egypt

An interactive Power BI dashboard analyzing about 9,000 bookings across 8 Egyptian hotels (January 2023 to February 2024): revenue, cancellations and no-shows, booking channels, guests, and booking behavior.

## Business question
Where does the hotel group earn its revenue, and why are roughly 1 in 5 bookings lost to cancellations and no-shows?

## Tools
Power BI, Power Query, DAX, star-schema data modeling

## Data
Dataset: generated for practice.
- `fact_bookings`: 9,000 unique bookings (9,050 raw rows)
- `dim_hotel`: 8 hotels with city, star rating, and rooms
- `dim_room_type`: room types with base price and occupancy
- `dim_guest`: 400 guests with country, loyalty tier, and signup date

## Data cleaning
- Removed blank rows, duplicate rows (50 duplicate bookings), and rows with errors
- Standardized text capitalization in every column
- Standardized the date columns, which mixed several formats
- Validated every primary key: each ID is unique, has no blanks, and matches between tables

## Dashboard pages
1. **Home:** revenue, bookings, average booking value, and lost revenue
2. **Revenue and performance:** hotels, cities, and room types
3. **Cancellations and no-shows:** where bookings are lost, including the effect of lead time
4. **Channels and payments:** channel mix and payment methods
5. **Guests:** countries, loyalty tiers, and spend per guest
6. **Booking behavior:** lead time, length of stay, check-in days, and peak months

## Key findings
- About 22.5% of bookings were lost: 14.8% cancelled and 7.7% no-shows.
- Cancellation rates were similar across channels (14.5% to 15.6%) and lead-time groups (14.6% to 15.4%), which suggests a property-wide issue rather than one channel.

## Recommendations
1. Introduce deposits or partly non-refundable rates across all channels.
2. Send reminders before check-in to reduce no-shows.
3. Track cancellations hotel by hotel to find the biggest losses.

## Assumptions
Completed and Confirmed bookings were treated as realized stays, and Cancelled and No-show bookings as lost. The data has no cost information, so the analysis covers revenue, not profit.
