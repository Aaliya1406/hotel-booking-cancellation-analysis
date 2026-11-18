# Hotel Booking Cancellation Analysis

## Project overview
This project explores hotel booking records to understand reservation cancellation patterns and how they vary by hotel type, arrival month, market segment, lead time, deposit type, and customer type.

The improved notebook preserves the main direction of the original tutorial project while improving data cleaning, reproducibility, chart labels, and interpretation.

## Tools and libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Dataset
The project uses the Hotel Booking Demand dataset (119,390 original rows and 36 columns in the supplied file).

The dataset is **not included in this repository**. The supplied copy contains guest-identifying fields such as names, email addresses, phone numbers, and masked card details. Do not publish the raw file. Download the dataset from its original Kaggle source under its applicable terms, and place the CSV at:

`data/hotel_booking.csv`

The file uploaded for this project was named `hotel_booking.xls`, but its contents are CSV text. If using that exact file locally, rename it to `hotel_booking.csv`.

## Repository structure
```text
hotel-booking-cancellation-analysis/
├── data/
│   └── README.md
├── notebooks/
│   ├── Hotel_Booking_Cancellation_Analysis.ipynb
│   └── original_tutorial_notebook_backup.ipynb
├── images/
│   └── README.md
├── .gitignore
├── requirements.txt
└── README.md
```

## How to run
1. Clone or download this repository.
2. Create and activate a Python virtual environment (recommended).
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the dataset from its original source and place it at `data/hotel_booking.csv`.
5. Open `notebooks/Hotel_Booking_Cancellation_Analysis.ipynb` in Jupyter Notebook or JupyterLab.
6. Run all cells from top to bottom.

## Selected results from the supplied dataset
After the notebook's documented cleaning steps, the supplied data produced these descriptive results:

| Metric | Result |
|---|---:|
| Records retained for analysis | 119,384 |
| Overall cancellation rate | 37.04% |
| City Hotel cancellation rate | 41.72% |
| Resort Hotel cancellation rate | 27.76% |
| Median lead time, cancelled bookings | 113 days |
| Median lead time, non-cancelled bookings | 45 days |

These are descriptive associations, not proof of causation. Results may differ if a different dataset version or cleaning procedure is used.

## Analytical scope
- Overall booking cancellation distribution
- Cancellation rates by hotel type
- Cancellation rates by guest arrival month
- Average recorded ADR by arrival month and hotel type
- Countries with the highest cancellation counts
- Cancellation rates by market segment
- Lead-time comparison by booking status
- Cancellation rates by deposit type and customer type

## Important interpretation notes
- `reservation_status_date` is the date when the reservation status was recorded; it is not the planned arrival date. Arrival-date fields are used for seasonality analysis.
- ADR is a recorded average daily rate and is not, by itself, actual revenue earned.
- Country-level charting ranks cancellation counts, not country-specific cancellation rates.
- Observational patterns do not establish causation.

## Author
Aaliya Shaikh
