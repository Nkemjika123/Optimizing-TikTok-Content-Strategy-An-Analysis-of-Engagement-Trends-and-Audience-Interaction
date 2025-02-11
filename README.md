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

## Key Questions
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

## Data Used
**TikTok_Post.csv**

### Data Cleaning Process
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

## Descriptive Analysis
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

## Exploratory Analysis
*(Continue the analysis from here if needed, including visualizations and further insights.)*

---




    

