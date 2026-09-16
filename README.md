# Josh Talks AI — Question 2: Human Transcriber Quality Evaluation

## Purpose
This project evaluates the quality of human transcribers using data signals rather than manual review. The goal is to identify suspicious transcribers who may be rushing, barely reviewing audio, or making minimal effort, which compromises the quality of AI training datasets.

## Assignment Context
1. Whisper AI generates an initial transcription.
2. Human transcribers listen and correct it.
3. Transcribers are evaluated based on their activity patterns to detect poor-quality work.

## Dataset Availability Limitation
**Note:** The actual Q2 transcription dataset was not provided in the assignment link. This repository contains the rigorous analytical framework, feature engineering formulas, and engineering logic required to solve the problem. **No fake or synthetic data was fabricated.** The thresholds and blocking logic outlined herein are proposed frameworks ready for calibration once real data is supplied.

## Project Structure
- `01_Raw_Data/`: Target location for the actual dataset.
- `02_Data_Cleaning/`: Output for cleaned dataset and quality checks.
- `03_Analysis/`: Warning signs methodology and feature engineering plans.
- `04_Visualizations/`: Target location for generated charts.
- `05_Part_I/`: Detailed documentation of the warning signs (Time-to-Duration Ratio, High CPS + Low Edit Rate).
- `06_Part_II/`: Staged risk model and blocking recommendations.
- `07_Final_Report/`: The comprehensive Q2 Final Report.
- `08_Screenshots/`: Contains notes on dataset availability.
- `09_Metadata/`: Dataset specifications.

## Analysis Workflow (Upon Data Arrival)
1. **Validation**: Check for missing, invalid, or inconsistent data.
2. **Feature Engineering**: Calculate `time_to_duration_ratio`, edit rates, and CPS statistics.
3. **User-Level Aggregation**: Use medians and percentiles to establish robust user metrics.
4. **Calibration**: Plot distributions to set concrete thresholds for the GREEN/YELLOW/ORANGE/RED risk model.

## Reproducibility
- Core logic is documented in the Final Report and Part I/Part II markdown files.
- Requirements (`pandas`, `numpy`, `matplotlib`, `openpyxl`) are listed in `requirements.txt` for when numerical analysis begins.
