# ✈️ Airline Analysis Dashboard

An interactive Excel dashboard built on Indian domestic airline data, allowing users to filter and analyze flight pricing, timing, and stop patterns across airlines, routes, and travel class.

# Dataset Used 
- <a href="https://github.com/prathamgaikwad735-png/Airline-Analysis-Dashboard/blob/main/Indian%20Airlines26.xlsx">Dataset & Dashboard<a/>

# Presentation 
- <a href="https://github.com/prathamgaikwad735-png/Airline-Analysis-Dashboard/blob/main/Airline_Analysis_Dashboard.pdf">Dashboard presentation<a/a>

---

## 📑 Table of Contents

- [Key Business Questions (KPIs)](#-key-business-questions-kpis)
- [Process & Methodology](#-process--methodology)
- [Dashboard Overview](#-dashboard-overview)
- [Insights](#-insights)
- [Conclusion](#-conclusion)

---

## 🎯 Key Business Questions (KPIs)

This dashboard is designed to answer the following business questions:

- **Pricing:** What is the minimum and maximum ticket price charged by each airline, and how does it vary by travel class?
- **Route Comparison:** How do fares and flight volume differ across source–destination city pairs (e.g., Bangalore–Hyderabad, Delhi–Kolkata, Mumbai–Kolkata)?
- **Booking Timing:** How does average ticket price change as the number of days left before departure decreases? Is there a clear "book early vs. book late" pattern?
- **Flight Volume:** Which airlines and routes have the highest number of departures/arrivals?
- **Stops:** Do zero-stop, one-stop, or two-plus-stop flights dominate the market, and how does that affect price?
- **Class-wise Behavior:** How does flight availability, airline presence, and pricing differ between **Business** and **Economy** class?

# Dashboard Overview
<img width="1362" height="710" alt="01_overview" src="https://github.com/user-attachments/assets/6cf0d916-e098-40c7-bbfd-5e9704f53a46" />


---

## 🔄 Process & Methodology

1. **Data Collection**
   - Sourced raw Indian domestic airline flight data (airline, source/destination city, class, price, duration, stops, departure/arrival time, days left before departure).

2. **Data Cleaning**
   - Removed duplicate and inconsistent records.
   - Standardized city names, airline names, and class labels (Business/Economy).
   - Handled missing values in price, duration, and stops fields.
   - Verified data types (numeric fields for price/duration, categorical for airline/city/class).

3. **Pivot Table Analysis**
   - Built pivot tables to calculate:
     - Airline-wise **Min/Max Price**
     - **Total Flights** by Departure & Arrival time per airline
     - **Days-Left-wise Average Price** (trend over 7 days before departure)
     - **Stop-wise Total Flights** (Zero / One / Two-or-more stops)
   - Cross-tabulated pivots by **Class**, **Source City**, and **Destination City** to enable slicer-based filtering.

4. **Dashboard Design**
   - Converted pivot tables into visuals:
     - **Column Chart** — Airline's Max & Min Price
     - **Clustered Bar Chart** — Departure & Arrival Times (Total Flights)
     - **Line Chart** — Days Left Wise Avg Price (up to 7 days)
     - **Pie Chart** — Stops-wise Total Flights
   - Added **3 Slicers** — Class, Source City, Destination City — for interactive filtering.
   - Included summary KPI cards: Total Flights, Average Price, Average Duration.

5. **Insight Generation**
   - Filtered the dashboard route-by-route and class-by-class.
   - Compared airline pricing, flight volume, and stop patterns for each combination.
   - Documented observations into structured, route-wise insights (see below).

---

## 📊 Dashboard Overview

The dashboard consists of:

| Component | Description |
|---|---|
| **Slicers** | Class, Source City, Destination City |
| **KPI Cards** | Total Flights, Average Price, Average Duration |
| **Column Chart** | Airline's Max & Min Price |
| **Clustered Bar Chart** | Departure & Arrival Times — Total Flights per Airline |
| **Line Chart** | Days Left Wise Avg Price (7-day trend) |
| **Pie Chart** | Stop's Total Flights (Zero / One / Two-or-more) |

**Airlines covered:** Air India, Vistara (Business Class) | Air India, AirAsia, GO_FIRST, Indigo, SpiceJet, Vistara (Economy Class)
**Cities covered:** Bangalore, Chennai, Delhi, Hyderabad, Kolkata, Mumbai

---

## 💡 Insights

### Business Class
- Only **Air India** and **Vistara** operate Business Class flights across all routes.
- **Bangalore → Hyderabad:** 3,014 flights; Air India max ₹61,212 vs Vistara max ₹83,239; zero-stop flights dominate (2,966).
- **Bangalore → Delhi:** Vistara's min & max price consistently higher than Air India; price fluctuates day-to-day instead of following a stable trend.
- **Bangalore → Kolkata:** Vistara pricing crosses ~₹1 lakh; sharp price spike at 5 days left before departure; zero-stop flights dominate.
- **Chennai → Mumbai:** Large price gap between airlines at the top end (Vistara max ₹1,14,704) but minimum prices are nearly identical (~₹23,000); price movement stabilizes after 2 days left.
- **Delhi → Kolkata:** Most expensive Business Class route overall; price consistently spikes at 1 day left across all routes originating from Delhi.
- **Hyderabad → Mumbai:** Most expensive Hyderabad-origin route (Vistara); zero-stop flights are highest among all Hyderabad routes.
- **Mumbai-origin routes:** Ticket prices are almost uniformly close to ₹1 lakh (Business Class) regardless of destination; Mumbai → Kolkata has the highest flight volume among Mumbai routes.

### Economy Class
- **6 airlines** compete in Economy: Air India, AirAsia, GO_FIRST, Indigo, SpiceJet, Vistara.
- **Bangalore → Delhi:** SpiceJet has the highest fares; price increases sharply at 4 days left.
- **Bangalore → Mumbai:** Air India has the highest fares; same 4-day-left price spike pattern observed.
- **Chennai routes:** Air India & Vistara are priciest; nearly all airlines show a price jump starting at 4 days left. Chennai → Mumbai has the highest zero-stop flight count.
- **Delhi routes:** Air India is the costliest; prices dip at 2 days left after peaking at 3 days left — a recurring pattern across most airlines.
- **Hyderabad → Mumbai:** GO_FIRST is notably expensive with a price spike at 4 days left; zero-stop flights dominate this route.
- **Kolkata routes:** Vistara and GO_FIRST dominate flight volume; zero-stop flights are highest on the Kolkata → Mumbai route.

### Cross-Cutting Patterns
- **Zero-stop flights consistently outnumber one-stop and multi-stop flights** across almost every route and class.
- **The "days-left" pricing trend** shows a common pattern: prices tend to spike sharply as departure approaches (typically within the last 1–5 days), rather than rising steadily and linearly.
- **Vistara is consistently priced higher than Air India** in Business Class across nearly every route.

---

## ✅ Conclusion

The Airline Analysis Dashboard reveals that airline pricing is heavily influenced by **how close the booking date is to departure**, with sharp price increases typically occurring within the final 1–5 days rather than a gradual daily rise. **Vistara commands a consistent price premium over Air India** in Business Class, while in Economy, pricing leadership shifts route-by-route among Air India, SpiceJet, and GO_FIRST. Across nearly all routes and classes, **zero-stop flights are the most common choice**, indicating strong traveler preference for direct connections. These insights can help travelers identify optimal booking windows and help airlines/analysts benchmark competitive pricing strategies by route and class.
