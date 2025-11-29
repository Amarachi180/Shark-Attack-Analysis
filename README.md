# Shark Attack Analysis


## Background
Shark attacks receive a lot of media attention, but comprehensive data analysis is sometimes eclipsed by sensationalized incidents. Understanding genuine patterns and risk factors is critical for public safety, conservation efforts, and sound policymaking.  

## Purpose
This report seeks to contribute to safer human-shark encounters and more effective marine safety standards by distinguishing between statistical reality and popular perception.  

## Key Metrics
1.	Make a graph of the number of shark attacks annually over time since 1900. What trends do you see?  
2.	Which countries report the most shark attacks? Within those countries, which areas and locations seem to be the most dangerous?  
3.	What body parts are most often injured?  
4.	Are shark attacks more common during certain parts of the day?  
5.	Which species of shark is attacking most often?  
6.	Are provoked shark attacks less frequent than unprovoked ones?  
7.	Which type of incident is most commonly associated with shark attacks?  
8.	Are provoked attacks more likely to result in fatal injuries?  

## Dataset Description
This dataset is obtained from Digitally Drive. It contains shark attack reports from the past 100 years, including location, activity, victim information (name, gender, age), shark species, and other details.
The total observation(rows) and the total columns are 6,094 and 22, respectively. The total missing values are 11,342. The key features include year, country, location, area, type, fatal (yes/no), time, injury, and species.


## Data Cleaning and Preparation
**During the data cleaning phase, several steps were taken to ensure data completeness and consistency before analysis:**  

**Country:** 46 rows with missing country information were removed.  
**Location:** 512 rows with missing location details were removed.  
**Area:** 412 rows with missing area information were removed.  
**Injury:** 28 rows with missing injury descriptions were removed.  
**Type:** 2 rows with missing incident type were removed.  
**Year:** 10 rows with missing year entries were removed.  
**Fatal (Y/N):** 11 rows with missing fatality status were removed.  
**Age:** 2,718 rows with missing age values were removed.  
**Time and species standardization:** Missing values in time and species columns were filled with “unspecified” and “unspecified shark species”, respectively (76 and 69 cells).  
**Text analysis** was performed on the species, country, location, area, type, fatal(y/n), time, and injury columns. The species status column was created to show confirmed and unconfirmed shark attacks using the species column as a reference.  

## Methodology & Tools
The analysis was conducted using the following tools: Excel, Power Query, and Power BI.  
Excel and Power Query were used during the data cleaning and preparation process (Extract-Transform-Load). DAX was used to create measures for visualizations such as “Injured Victims”, “Uninjured Victims”, etc. Power BI was used for visualization, creating a visual report like bar charts, line charts, and pie charts.  
Unconfirmed shark attack records were filtered out during visual creation for consistency and accuracy.  

## Key Performance Indicator (KPI)
The major KPIs that were created using DAX are:  
1.	Confirmed Shark Attack  
2.	Unconfirmed Shark Attack  
3.	Injured Victims  
4.	Uninjured Victims  
5.	Shark Attack Death Rate  

## Visualization & Analysis
![](https://github.com/Amarachi180/Shark-Attack-Analysis/blob/main/Screenshot%202025-11-29%20120323.png)  
![](https://github.com/Amarachi180/Shark-Attack-Analysis/blob/main/Screenshot%202025-11-29%20120356.png)  
![](https://github.com/Amarachi180/Shark-Attack-Analysis/blob/main/Screenshot%202025-11-29%20120848.png)  

**1.	Make a graph of the number of shark attacks annually over time since 1900. What trends do you see?**  

The shark attack data from 1900 to 2017 shows a long-term upward trend in recorded incidents, increasing from isolated single-digit counts in the early 1900s to consistent annual totals above 60 starting in the 1990s, with a peak of 101 attacks in 2015. Year-over-year changes were especially volatile in the early decades, with a +500% spike in 1905 and a -88.9% drop in 1918, mainly due to small base numbers. As reporting improved and coastal activity grew over the century, the data became more stable, with the 5-year moving average steadily rising from under 5 attacks in the 1910s to over 80 in the 2010s. The mid-century period (1940s–1980s) shows gradual but steady growth, implying better global tracking and increased human presence in marine environments. From the 1990s onward, the pattern becomes more consistent: yearly totals fluctuate within a narrower range (60–90 attacks), reflecting more reliable reporting systems and mature monitoring networks. Notable peaks, such as in 1959, 1995, 2000, and 2015, may relate to increased water recreation, tourism booms, or improved detection rather than ecological surges. Overall, the data indicate a shift from noisy, irregular early records to a clearer, more predictable trend over time, driven by rising human–ocean interaction and better documentation rather than changes in shark behavior.

**2.	Which countries report the most shark attacks? Within those countries, which areas and locations seem to be the most dangerous?**

The top three countries with the highest number of shark attacks are the United States, Australia, and South Africa. The United States recorded 1,397 attacks (45.53%), followed by Australia with 671 attacks (21.87%), and South Africa with 354 attacks (11.54%).  
In the United States, the three most dangerous areas were Florida, which recorded 779 attacks (55.76%), California with 174 attacks (12.46%), and Hawaii with 128 attacks (9.16%).
Australia’s top three high-risk regions were New South Wales, with 272 attacks (40.54%), Queensland with 176 attacks (26.23%), and Western Australia with 83 attacks (12.37%).
In South Africa, the provinces with the highest number of shark attacks were KwaZulu-Natal, with 133 attacks (37.57%), Eastern Cape Province with 111 attacks (31.36%), and Western Cape Province with 107 attacks (30.23%).  
Looking at specific locations, the United States’ top three hotspots were New Smyrna Beach, Volusia County, with 156 attacks (10.80%), followed by Daytona Beach, Volusia County, with 27 attacks (1.87%), and Ponce Inlet, Volusia County, with 18 attacks (1.25%).
In Australia, the top three locations with reported attacks were Coogee, with 6 attacks (0.89%), Byron Bay with 5 attacks (0.75%), and Ross River, Townsville, also with 5 attacks (0.75%).
For South Africa, the most affected locations were Nahoon, with 9 attacks (2.54%), Country Club Beach, Durban, with 8 attacks (2.26%), and North Beach, Durban, also with 8 attacks (2.26%).  

**3.	What body parts are most often injured?**  

The injury patterns show that the legs are the most frequently injured body part, accounting for 1,474 cases (52.79%). This is followed by hand injuries, which represent 498 cases (17.84%), and unspecified injuries, accounting for 479 cases (17.16%). Body injuries make up 315 cases (11.28%), while head injuries are the least common, with only 26 cases (0.93%) reported. Overall, the data suggests that shark attacks most often affect limbs, particularly the legs, which is likely due to their position and movement in the water.  

**4.	Are shark attacks more common during certain parts of the day?**  

The distribution of shark attacks across different times of day indicates a clear pattern. The afternoon accounts for the highest proportion of incidents, with 1,084 attacks (35.33%), suggesting that this period carries the greatest exposure to risk. Unspecified times represent 908 attacks (29.60%), showing that nearly one-third of cases lack detailed timing information. The morning period follows with 650 attacks (21.19%), while evening incidents total 386 attacks (12.58%). Nighttime attacks are rare, with only 40 cases (1.30%) occurring after dark. These findings suggest that shark attacks are predominantly daytime events, likely reflecting when people are most active in the water.  


**5.	Which species of shark are attacking most often?**  

An examination of the shark species involved in attacks reveals that most incidents are attributed to unspecified shark species, which account for 1,832 cases (65.31%). Among the identified species, the White Shark is responsible for the highest number of attacks, with 412 cases (14.69%), followed by the Tiger Shark with 168 cases (5.99%) and the Bull Shark with 141 cases (5.03%). Other species, such as the Blacktip Shark (72 attacks, 2.57%), Copper Shark (57 attacks, 2.03%), and Nurse Shark (35 attacks, 1.25%), contribute smaller proportions. Less frequently involved species include the Ragged-tooth Shark (32 attacks, 1.14%), Hammerhead Shark (29 attacks, 1.03%), and Grey Nurse Shark (27 attacks, 0.96%). Overall, while species identification is often unavailable, the data highlight that White, Tiger, and Bull Sharks are the most commonly implicated among known species.  

**6.	Are provoked shark attacks less frequent than unprovoked ones?**  

The data clearly indicates that unprovoked shark attacks dominate the overall incident records. A total of 2,643 cases (92%) occurred without any intentional human action toward the shark, showing that most encounters happen naturally in the marine environment. In comparison, provoked attacks account for just 241 cases (8%), making them relatively rare. This large gap suggests that the majority of shark–human interactions are spontaneous rather than triggered, emphasizing that sharks generally do not attack unless compelled or disturbed.  

**7.	Which type of incident is most commonly associated with shark attacks?**  

The data shows that unprovoked shark attacks are the most common type, accounting for 86.15 percent of all recorded incidents with a total of 2,643 cases. This indicates that most shark encounters occur naturally and without any deliberate action from the victim. Provoked incidents, where the shark reacts because it was disturbed or interacted with, make up only 7.86 percent with 241 cases. Other categories appear far less frequently, including invalid cases at 4.14 percent, sea disasters at 1.01 percent, and boat related incidents which together account for less than one percent of all cases. Overall, the findings highlight that the vast majority of shark attacks happen independently of human provocation.  

**8.	Are provoked attacks more likely to result in fatal injuries?**

The data shows that provoked shark attacks rarely result in fatalities. Of all recorded provoked incidents, 235 cases, or 98 percent, were non-fatal, while only 6 cases, or 2 percent, led to death. This indicates that even when sharks are provoked, the likelihood of a fatal outcome is very low, and most encounters do not result in serious harm.  

**You can interact with the live visualization here:** [HERE](https://app.powerbi.com/view?r=eyJrIjoiYjZmMTJlNTctNDE1ZC00ZTRiLTg0MDgtZWJiMWM1MzE4Y2QzIiwidCI6ImEzMWM5OWQ2LTA3MzAtNGNmMy04ZjI2LWJiYmI0YzA3YWYyMSJ9) 


## Conclusion & Recommendations  
### Conclusion  
This analysis of over a century of shark attack data reveals a clear distinction between the sensationalized perception of shark encounters and the statistical reality. The long-term increase in reported incidents is more likely attributable to rising human presence in coastal waters and improved reporting systems than to a change in shark behavior. Attacks are not random events; they follow predictable patterns tied to location, time, and human activity.  

**Key findings that define this reality include:**  
1.	Geographical Hotspots: A majority of incidents are concentrated in a few countries (USA, Australia, South Africa) and within specific, well-known regions within them (e.g., Florida, New South Wales, KwaZulu-Natal).
2.	Behavioral Patterns: Shark attacks are overwhelmingly unprovoked (92%) and occur most frequently during the afternoon, aligning with peak hours for human water recreation.
3.	Risk and Severity: The most common injuries are to the legs, suggesting sharks often investigate or mistake moving limbs for prey. Crucially, even in the rare event of a provoked attack, the outcome is rarely fatal (98% non-fatal).
4.	Species Involvement: While species data are often unspecified, the White Shark, Tiger Shark, and Bull Shark are the most frequently identified species in attacks.  

In essence, the data paints a picture where the risk of a shark attack, while real, is context-dependent and generally low in severity. The narrative of sharks as intentional, malicious predators is not supported by the evidence; instead, most incidents appear to be cases of mistaken identity or investigative behavior in the shark's natural environment.  

### Recommendations  
**1.	Enhance Public Awareness:** Launch targeted "Shark Smart" safety campaigns in identified high-risk areas (e.g., Florida, New South Wales, KwaZulu-Natal). Messages should emphasize avoiding water at dusk/dawn, not swimming near fishing activity, and never provoking sharks.  
**2.	Optimize Safety Resources:** Direct resources for beach patrols, warning systems, and emergency response to the most dangerous locations and times, as revealed by the data, to improve protection efficiently.  
**3.	Support Science and Conservation:** Use these findings to promote a fact-based understanding of sharks, supporting conservation efforts. Fund further research into the behavior of key species (White, Tiger, and Bull Sharks) in high-interaction zones to develop better prevention strategies.  




