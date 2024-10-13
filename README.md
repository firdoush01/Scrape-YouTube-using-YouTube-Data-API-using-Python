


# YouTube Video Analysis

## Overview

This project analyzes video statistics such as views, likes, and comments from a list of YouTube videos. The data includes video titles, publication dates, and engagement metrics, stored in a CSV file. The project provides insights into video performance over time.

## Features

- Extracts and stores video statistics such as:
  - **Title**
  - **Published Date**
  - **Views**
  - **Likes**
  - **Comments**
  - **Published Month**
- Analyzes YouTube video performance using CSV data.

## Dataset

The dataset used for analysis (`Video_details.csv`) contains the following columns:

- **Title**: Title of the YouTube video.
- **published_date**: Date when the video was published.
- **Views**: Number of views for each video.
- **Likes**: Number of likes each video has received.
- **Comments**: Number of comments on the video.
- **Month**: The month of publication.

### Sample Data

| Title                                    | published_date | Views | Likes | Comments | Month |
|------------------------------------------|----------------|-------|-------|----------|-------|
| My Top 5 Data Science Internship Tips     | 2019-06-15     | 12339 | 506   | 24       | Jun   |
| Golf STATS: Strokes Gained Explained      | 2019-06-07     | 8451  | 167   | 31       | Jun   |
| Most Data Science Hopefuls Overlook This  | 2019-05-25     | 629   | 44    | 5        | May   |

## Usage

1. **Prerequisites**:
   - Python 3.x
   - Required Python libraries:
     - `pandas`

   You can install the required dependencies with:
   ```bash
   pip install pandas
   ```

2. **Running the Analysis**:

   You can load the CSV file and start analyzing the video performance metrics using the following code:

   ```python
   import pandas as pd

   # Load the CSV file
   df = pd.read_csv('Video_details.csv')

   # Display the first few rows of the dataset
   print(df.head())
   ```

   This will provide an overview of the video data and allow further analysis such as identifying the most liked video, most commented, or most viewed.

## Example Analysis

You can use this dataset to perform various analyses, such as:

- **Finding the Most Viewed Video**:

   ```python
   most_viewed = df.loc[df['Views'].idxmax()]
   print("Most Viewed Video:", most_viewed['Title'], "with", most_viewed['Views'], "views.")
   ```

- **Analyzing Video Engagement**:
  Create visualizations of likes, views, and comments to assess which types of videos are performing well.

## Contributing

Feel free to submit issues or pull requests if you have suggestions to improve this project.

## License

This project is licensed under the MIT License.

---
