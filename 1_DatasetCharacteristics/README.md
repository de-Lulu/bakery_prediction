# Dataset Characteristics

The weather dataset and Kieler Woche contained missing entries.

Imputation Strategy:

KielerWoche & Wettercode Dataset: Filled NaN with 0 (Assumed "No Event" / "No significant weather" if missing). Reasoning: This is a structural decision, not a guess. Since the original files only listed dates when the festival or a weather event actually occurred, any date that didn't match during our merge is logically a 'non-event' day. Therefore, treating NaN as 0 correctly represents 'No Festival' or 'Normal Weather'.

Weather Imputation (Temp, Wind, Clouds): Used Forward Fill followed by Backward Fill. Reasoning: Weather conditions (like temperature or cloud cover) typically persist over short periods. Using the last known value is a safe, logical baseline (Persistence Model).
