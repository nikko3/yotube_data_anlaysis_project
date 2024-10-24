# YouTube Data Science Channel Analysis
### Project Overview
- This project performs Exploratory Data Analysis (EDA) on video data from four popular YouTube channels in the data science niche. The goal is to analyze the content and performance of these channels by extracting video statistics, understanding patterns in views, engagement (likes, comments), and upload schedules.  

The analysis uses YouTube's API to retrieve data, then visualizes and interprets the results through various plots and statistics.

### Data Sources
Data is collected from the following YouTube channels:

- Luke Barousse (UCLLw7jmFsvfIVaUFsLs8mlQ)  
- Ken Jee (UCiT9RITQ9PW6BhXK0y2jaeg)  
- Alex The Analyst (UC7cs8q-gJRlGwj4A8OmCmXg)  
- Tina Huang (UC2UXDak6o7rBm23k3Vv5dww)  
- The data includes details like:  

Number of subscribers, views, and total videos for each channel.
Video-specific data such as title, publish date, view count, like count, comment count, and duration.

### Tools and Libraries Used

  Google API: To extract YouTube channel and video data using googleapiclient.discovery.  
  Pandas: For data manipulation and cleaning.  
  Seaborn & Matplotlib: For data visualization.  
  Dateutil: To parse dates.  
  Isodate: To convert video durations to seconds.  
  
### Key Functions

  1. get_channel_stats(youtube, channel_ids)
  Fetches statistics for each YouTube channel, including subscribers, views, total videos, and the playlist ID of uploaded videos.

  2. get_video_ids(youtube, playlist_id)
  Retrieves all video IDs from the provided playlist.

  3. get_video_details(youtube, video_ids)
  Fetches detailed information for each video, including view count, like count, duration, and interaction data.

### Data Processing

  1.Null Handling: Missing values are handled for fields like tags and favoriteCount.  
  2.Data Type Conversion: The columns related to counts (views, likes, comments) are converted from object to numeric types.  
  3.Duration Conversion: Video durations are converted from ISO 8601 format to seconds.  
  4.Day of the Week: Extracted the day videos were published for analysis of upload schedules.  
  
### Visualizations  

  1.Best & Worst Performing Videos: Bar charts showing the highest and lowest view counts.  
  2.View Distribution: Violin plots visualizing the distribution of views across channels.  
  3.Engagement Analysis: Scatter plots showing the relationship between view count, likes, and comments.  
  4.Video Duration Distribution: Histogram analyzing the distribution of video lengths.  
  5.Upload Schedule: Bar chart representing the frequency of video uploads by day of the week.  
  
### How to Run

  1.Clone the repository.  
  2.Install the required Python packages  
  3.'''bash
  pip install google-api-python-client pandas seaborn matplotlib python-dateutil isodate  
  4.Replace the api_key in the script with your own YouTube Data API key.  
  5.Run the script to extract data and visualize results.  
  
### Results and Insights

  - Performance Patterns: The most and least viewed videos provide insight into content preferences in the data science community.
  - Engagement Trends: Higher view counts correlate with increased likes and comments.
  - Upload Behavior: Analyzing the frequency of uploads shows preferred days for posting new content.

### Future Improvements

  - Include more YouTube channels for broader analysis.
  - Add sentiment analysis of video comments.
  - Use machine learning models to predict video performance based on content features.
