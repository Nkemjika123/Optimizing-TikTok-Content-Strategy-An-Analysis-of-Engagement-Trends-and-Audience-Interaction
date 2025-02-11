# Optimizing-TikTok-Content-Strategy-An-Analysis-of-Engagement-Trends-and-Audience-Interaction


---

## Data Structure
- **Date, Day, Month, Year, Time, Period**: Information about when the posts were made.  
- **Like(s)**: Number of likes received.  
- **Who can view**: Visibility setting (e.g., Everyone).  
- **Allow comments, Allow stitches, Allow duets, Allow stickers, Allow sharing to story**: Content interaction settings.  
- **Sound**: Sound used in the post (e.g., original sound, popular sound).  
- **Title**: Post title or description.  
- **Location**: Geographical setting for the post (e.g., Nigeria).  
- **Username**: People who followed for the content.  

---

## Objectives
1. **Measure Content Performance**  
   Analyze engagement metrics such as likes and determine high-performing posts based on sound type, posting time, and content settings.  

2. **Identify Engagement Trends**  
   Track the growth in engagement over time and understand which factors (e.g., allowing comments, sharing to stories) contribute to better performance.  

3. **Optimize Content Strategy**  
   Uncover the best posting times, popular sound choices, and effective content themes to increase visibility and interaction.  

4. **Audience Interaction Analysis**  
   Study audience interaction settings (stitches, duets) to gauge how they affect engagement and content reach.  

5. **Provide Actionable Insights**  
   Offer recommendations to improve content creation strategies for influencers, educators, and marketing professionals.  

---

## People Who Can Use This Analysis
1. **Content Creators & Influencers**  
   Understand how to maximize reach, improve engagement, and tailor content to audience preferences.  

2. **Social Media Managers & Marketers**  
   Develop data-driven strategies for promoting brands and products on TikTok.  

3. **Educators & Coaches in Digital Marketing**  
   Teach students and clients about social media analytics and how data can drive success on platforms like TikTok.  

4. **Business Owners & Entrepreneurs**  
   Explore TikTok as a marketing tool and optimize content for brand awareness and customer engagement.  

5. **Data Analysts & Researchers**  
   Explore real-world applications of social media data and identify trends and patterns.  

---

# Key Questions
### Engagement Metrics
1. Which posts have the highest engagement (likes)?  
2. What is the average number of likes per post?  
3. What percentage of posts allow comments, duets, or stitches?  

### Content Strategy
4. Which sound or sound type performs best (most likes)?  
5. What type of content titles attract the most likes?  
6. Is there a relationship between posting time (Date/Time) and engagement?  

### Audience Insights
7. How many posts were restricted to specific locations (e.g., Nigeria) and how did they perform compared to those without a location restriction?  
8. What percentage of posts are visible to everyone?  

### Trend Analysis
9. How has engagement (likes) changed over time?  
10. Which content settings (allowing stitches, duets, sharing to story) correlate with higher likes?  

### Content Mix
11. What’s the distribution of video vs. photo-based posts?  

---

# Data Used
**TikTok_Post.csv**

# Data Cleaning Process
- No missing values.  
- No duplicated values.  
- Changed time format from `33:23:33` to `3:30 PM`.  
- Extracted **Day**, **Month**, and **Year** using custom formatting.  
- Filled all blank cells using `FIND` and `REPLACE` with `None`.  
- Extracted **Period** from time using the following formula:  
  ```excel
  =IF(AND(E1>=TIME(0,0,0), E1<TIME(6,0,0)), "Midnight",
  IF(AND(E1>=TIME(6,0,0), E1<TIME(12,0,0)), "Morning",
  IF(AND(E1>=TIME(12,0,0), E1<TIME(18,0,0)), "Afternoon", "Evening")))
  ```

---

# Descriptive Analysis
1. **Post with the highest engagement (most likes)**  
   - **Title**: *Data Analyst interview questions: Excel, SQL, and Power BI*  
   - **Likes**: 9,680  
   - **Date**: 2024-12-31  
   - **Sound**: *Overcome - Skott*  
   - **Time**: 21:09  

2. **Average likes per post**: 224 (rounded)  

3. **Percentage of posts allowing interactions**:  
   - **Comments**: 100%  
   - **Stitches**: 73.2%  
   - **Duets**: 0%  

---

# Exploratory Analysis

### 4. Which sound or sound type performs best (most likes)? 
![Screenshot 2025-02-10 210932](https://github.com/user-attachments/assets/90b8e085-eb47-4897-b736-fe8d9fca510e)

The table above shows that **trending sounds** are highly encouraged for better engagement.  

### 5. What type of content titles attract the most likes?  
![Screenshot 2025-02-10 215237](https://github.com/user-attachments/assets/6fb8655f-0c05-4173-ae65-f81cbd8b2705)

The chart above indicates that **educational content** titles attract the most likes.  

### 6. Is there a relationship between posting time (Date/Time) and engagement?  

The chart above highlights that the **7 PM to 10 PM** time slot is the most preferred, with an average of **over 3,000 likes** during these hours.  

### 7. How many posts were restricted to specific locations (e.g., Nigeria), and how did they perform compared to unrestricted posts?  
Posts restricted to specific locations, such as **Nigeria**, **perform better** compared to unrestricted posts.  

### 8. What percentage of posts are visible to everyone?  
Posts set to be visible to **everyone** show **better performance** than those with restricted visibility.  

### 9. What’s the distribution of video vs. photo-based posts?  
The chart above reveals that **video content dominates** with over **70%**, while photo-based posts make up around **25%** of the total.  

---

## Time Series Analysis

### 10. How has engagement (likes) changed over time?  
![Screenshot 2025-02-10 230009](https://github.com/user-attachments/assets/14d433bb-7dfb-4ef2-8279-b9024838ec96)

The line chart shows a **significant increase** in engagement during **December to January 2025**, with total likes exceeding **10,000**.  

- Likes decline in **February 2025**, which may be due to the data being extracted on **07/02/2025**, resulting in incomplete February data.  
- During **November to December**, there was an **increase in posts (1–3 per day)**. In January, posting frequency decreased to **1–2 posts per day**.  
- The **spike in January 2025** suggests that consistent posting efforts during the preceding months led to the increase in engagement.  

---

# Correlation Analysis

### 11. Which content settings (allowing stitches, duets, sharing to story) correlate with higher likes?  
![Screenshot 2025-02-10 215615](https://github.com/user-attachments/assets/632c26d2-1323-4517-b6cf-6328407c3d04)

The correlation matrix reveals the following:  

1. **Like(s) and Allow comments_Yes (-0.53)**:  
   Moderate negative correlation. This suggests that allowing comments is associated with a slight decrease in likes.  
   
2. **Like(s) and Allow stitches_Yes (0.44)**:  
   Moderate positive correlation, indicating that allowing stitches is somewhat associated with an increase in likes.  

3. **Like(s) and Allow duets_Yes (0.07)**:  
   Weak positive correlation. There’s little to no relationship between allowing duets and the number of likes.  

4. **Like(s) and Allow stickers_Yes (0.19)**:  
   Weak positive correlation, indicating a slight increase in likes when stickers are allowed.  

5. **Like(s) and Allow sharing to story_Yes (-0.78)**:  
   Strong negative correlation. Allowing sharing to stories correlates with a significant decrease in likes.  

---


---




    

