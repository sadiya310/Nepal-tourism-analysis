NEPAL TOURISM DESTINATION ANALYSIS
=====================================
Analyst: [Sadiya Prabin]
Date: June 2026
Dataset: Nepal Tourism Destinations (512 rows, 9 columns)
Tools Used: SQL (sqliteonline.com)
Data Source: Kaggle — Nepal Tourism Dataset

OBJECTIVE
----------
To analyse Nepal's tourism destinations across 7 provinces and identify 
opportunities for tourism development using SQL data analysis.

=====================================

QUERY 1 — DESTINATIONS BY PROVINCE
-------------------------------------
Business Question:
How many tourism destinations exist in each province of Nepal?

SQL Query:
SELECT province, COUNT(*) AS no_of_destinations
FROM Tourism
GROUP BY province;

Result:
Province 1 — 90 destinations
Province 2 — 31 destinations
Province 3 — 121 destinations
Province 4 — 123 destinations
Province 5 — 74 destinations
Province 6 — 44 destinations
Province 7 — 34 destinations

Insight:
To understand the distribution of tourism destinations across Nepal, 
we analysed destination counts by province. Province 4 has the highest 
number of destinations with 123, closely followed by Province 3 with 121. 
Province 2 has the fewest destinations with only 31, indicating an 
opportunity for tourism development in that region.

=====================================

QUERY 2 — AVERAGE ADVENTURE SCORE BY PROVINCE
------------------------------------------------
Business Question:
Which province offers the best adventure tourism experiences?

SQL Query:
SELECT province, ROUND(AVG(adventure), 2) AS average_adventure
FROM Tourism
GROUP BY province
ORDER BY average_adventure DESC;

Result:
Province 1 — 2.81
Province 3 — 1.92
Province 4 — 1.55
Province 6 — 1.25
Province 5 — 0.96
Province 7 — 0.88
Province 2 — 0.23

Insight:
To understand adventure tourism potential across Nepal, we calculated 
the average adventure score by province. Province 1 leads significantly 
with an average score of 2.81, followed by Province 3 at 1.92, while 
Province 2 scores the lowest at 0.23. We recommend prioritising adventure 
tourism investment and infrastructure development in Province 1 to 
maximise revenue growth.

=====================================

QUERY 3 — HIGH CULTURE DESTINATIONS
--------------------------------------
Business Question:
Which destinations have strong cultural significance (culture score above 3)?

SQL Query:
SELECT * FROM Tourism WHERE culture > 3;

SELECT COUNT(*) AS high_culture_destinations
FROM Tourism
WHERE culture > 3;

Result:
161 out of 512 destinations score above 3 in culture (31% of all destinations)
Top destinations include: Pashupatinath Temple, Janaki Mandir, 
Hanumandhoka Palace, Patan Durbar Square, Manakamana Temple

Insight:
Cultural tourism is a significant strength of Nepal, with 161 out of 512 
destinations scoring above 3 in culture, representing 31% of all destinations. 
This indicates strong potential for cultural tourism promotion, particularly 
around Hindu temples, Buddhist monasteries, and historical heritage sites.

=====================================

QUERY 4 — TOTAL SIGHTSEEING SCORE BY PROVINCE
------------------------------------------------
Business Question:
Which province has the strongest sightseeing potential?

SQL Query:
SELECT province, SUM(sightseeing) AS total_sightseeing
FROM Tourism
GROUP BY province
ORDER BY total_sightseeing DESC;

Result:
Province 4 — 455.5
Province 3 — 348.5
Province 5 — 233.0
Province 1 — 200.0
Province 6 — 166.5
Province 2 — 120.0
Province 7 — 117.5

Insight:
Province 4 leads Nepal in total sightseeing score with 455.5, followed 
by Province 3 with 348.5, while Province 7 scores the lowest at 117.5. 
Notably, every province scores above 100, indicating strong sightseeing 
potential across all of Nepal. Since Province 4 also has the highest 
number of destinations, it should be the primary focus for tourism 
infrastructure investment and international marketing campaigns.

=====================================

QUERY 5 — ADVENTURE AND WILDLIFE HOTSPOTS
-------------------------------------------
Business Question:
Which destinations offer both high adventure and strong wildlife 
experiences (scores above 3 in both)?

SQL Query:
SELECT * FROM Tourism
WHERE adventure > 3 AND wildlife > 3;

Result:
16 destinations scored above 3 in both adventure and wildlife, including:
- Chitwan National Park (Province 3)
- Bardiya National Park (Province 5)
- Koshi Tappu Wildlife Reserve (Province 1)
- Shivapuri Nagarjun National Park (Province 3)
- Langtang National Park (Province 3)

Insight:
Analysis reveals 16 destinations in Nepal where both adventure and 
Wildlife scores exceed 3, representing the country's strongest 
eco-tourism opportunities. These destinations are predominantly national 
parks and wildlife reserves such as Chitwan, Bardiya, and Koshi Tappu, 
suggesting that Nepal has significant untapped potential in wildlife and 
adventure tourism that could attract international eco-tourists.

=====================================

KEY FINDINGS SUMMARY
----------------------
1. Province 4 is Nepal's strongest tourism province — most destinations, 
   highest sightseeing score.
2. Province 1 leads in adventure tourism with an average score of 2.81.
3. 31% of all destinations have strong cultural significance — Nepal's 
   biggest tourism strength.
4. Every province scores above 100 in sightseeing — nationwide potential.
5. 16 eco-tourism hotspots combining adventure and wildlife — strong 
   international appeal.

RECOMMENDATION
---------------
Nepal should prioritise Province 4 for general tourism investment, 
Province 1 for adventure tourism marketing, and develop its 16 
eco-tourism hotspots to attract high-value international tourists 
seeking wildlife and adventure experiences.

=====================================
Project by: [Sadiya Prabin]
Email: [sadiya310753@gmail.com]
GitHub: [sadiya310]
