# Data Preparation

To improve our model's ability to capture seasonality and trends, we engineered several features from the raw Datum column.

Variables:
Year, Month, Day: Extracted to capture annual growth and monthly seasonality.
Weekday: Integer values were assigned (0=Monday, 6=Sunday) to capture weekly cycles.
IsWeekend: Boolean flag (True for Saturday/Sunday) to capture the high traffic on weekends.
KielerWoche: Binary flag (1 during the event, 0 otherwise). Accounts for the massive influx of visitors during the festival.

