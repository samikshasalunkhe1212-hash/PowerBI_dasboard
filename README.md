# 📊 LinkedIn User Engagement Dashboard — Power BI Project

## 🧠 Project Overview
This Power BI project analyzes **LinkedIn user engagement data** to understand how users interact on the platform through posts, comments, articles, and messages.  
The dashboard helps identify **top-performing users, departments, and engagement trends** to make data-driven decisions that improve online presence and networking performance.

---

## 🎯 Objective
To build an interactive Power BI dashboard that:
- Tracks total engagement across multiple metrics (likes, comments, messages, and articles).  
- Identifies top users and departments with the highest engagement.  
- Analyzes user activity trends over time.  
- Helps companies, HR teams, or marketing groups improve participation and visibility.

---

## 🧾 Dataset Description
The dataset consists of **500 records** with the following columns:

| Field Name | Description |
|-------------|--------------|
| User ID | Unique identifier for each user |
| User Name | Name of the LinkedIn user |
| Job Title | Role/position of the user |
| Department | Department or team name |
| Post Likes | Number of likes received |
| Post Comments | Number of comments received |
| Articles Published | Count of articles published |
| Messages Sent | Number of messages exchanged |
| Last Engagement Date | Date of last activity |
| Engagement Score | Combined metric of user activity |

---

## ⚙️ Data Modeling & DAX Formulas
Power BI was used to clean, model, and visualize the data.  
Below are the main **DAX measures** implemented in this project:

```DAX
Total Likes = SUM('LinkedIn Data'[Post Likes])
Total Comments = SUM('LinkedIn Data'[Post Comments])
Total Articles = SUM('LinkedIn Data'[Articles Published])
Total Messages = SUM('LinkedIn Data'[Messages Sent])
Total Engagement = [Total Likes] + [Total Comments] + [Total Articles] + [Total Messages]
Average Engagement = AVERAGE('LinkedIn Data'[Engagement Score])
User Rank = RANKX(ALL('LinkedIn Data'[User Name]), [Total Engagement], , DESC)
# PowerBI_dasboard
