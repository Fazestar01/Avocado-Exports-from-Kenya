# Avocado Exports From Kenya Analysis
### Data Analyst: [Faiza Abdulqadir](https://github.com/Fazestar01)
**Avocado Exports from Kenya analysis** is a project focused on the ETL (Extract, Transform, Load) pipeline in Jupyter Notebook and visualisations in Tableau. The project examines Kenya's avocado export patterns, trading relationships, and market dynamics to assess competitiveness in the global avocado industry. 

![Kenyan Avocado Analysis Banner](Avocado-Export-Banner.png)

## Navigation
* [Data Investigations](https://github.com/Fazestar01/Avocado-Exports-from-Kenya/blob/main/jupyter_notebooks/kenyan-avocado-investigation.ipynb)
* [Raw Data](https://github.com/Fazestar01/Avocado-Exports-from-Kenya/blob/main/data/raw/kenyan-avocados-guide-2023.csv)
* [Cleaned Data](https://github.com/Fazestar01/Avocado-Exports-from-Kenya/blob/main/data/cleaned/cleaned_kenyan_avocados.csv)
* [Dashboard](https://public.tableau.com/app/profile/faiza.abdulqadir/viz/Kenyan_Avocado_Analysis/KenyanAvocadoExportsAnalysis?publish=yes)

## Dataset Content
* Data was acquried from a dataset on a software that includes several databases from various international organisation [WITS](https://wits.worldbank.org/trade/comtrade/en/country/KEN/year/2023/tradeflow/Exports/partner/ALL/product/080440?utm_source=chatgpt.com#), the data includes avocado export information from 2023 from Kenya showing weight, quantity and trade value.


## Business Requirements
The avocado industry is growing at a rapid rate with increasing international markets. With that being said, Kenya is amoungst one of the new kids on the block when it comes to being an avocado exporter. 

* This is being carried out by an Agricultual Analyst for the exporting company, Globalwema which is based in both the UK and Kenya. The purpose is to give this company insight on the potential produce they wish to embark on.

* The requirement is to look into which countries are Kenyas top trading partners. As countries like Mexico and South Africa have been in the running, is vital to know if Kenya is part of the running.

* In addition, are export volumes and values increasing over time and how is the pricing per tonnne varying across the markets and years. This is worth looking into as although Kenya is now exporting Avocados, does it mean it's a sustanable country in the long run. 

* In terms of future projective predictions, its worth looking at what is happening now and whether if Kenya can compete with the more seasoned players in the avocado exporting world or if this is a short term matter.



## Hypothesis and how to validate?

The following hypotheses reflect the initial expectations and goals of the project. However, as the analysis progressed, the results challenged these assumptions, prompting a shift in direction and a refinement of the original hypotheses.
Below, you will find my original hypothesis and then the new refined hypothesis shortly after that. This evolution highlights the power of data to reshape understanding; what started as a confident prediction turned into a more nuanced insight:


###  *Original Hypothesis 1* Kenya’s avocado export value is increasing year over year:
* Despite the fact that the Kenyan market for avocados is growing, the original hypothesis seemed quite vague due to the fact that the dataset findings were based on a year basis, just 2023 to be exact. Given that the avocado market is indeed growing, we still can't assume consistent year - on - year growth from a narrow dataset. This makes the analysis almost temperamental as change would be more ideal IF it had shown a monthly growth. The information given from the dataset might be oversimplified due to external factors like inflation, currency or market shocks. It is hard to tell. Not having monthly breakdowns as well as only having annual totals keeps a vague idea on what is to come for the avocado market in Kenya.


Another point to add is the category ‘World’. Upon cleaning and using the data for visualisation, I noticed that the dataset had a category under ‘World’ that sat under the ‘Country’ column. This was another vague data point as it was too broad for analysis and very tedious to figure out what countries were under ‘world’. 

At this point I had already added this into the Jupyter Notebook visualisation (see below) to show the client how vague this point was and that moving forward, the more advanced analysis on the Tableau visualisations wouldn’t need or miss out the finalisation of this analysis.


![alt text](image.png)


### *Original Hypothesis 2* Countries that import the most avocados from Kenya are also the ones paying the highest value:
* This is another point of assumption as it assumes a direct relationship between volume and value. This doesn't work on a wide spectrum as it oversimplifies the fact that some countries buy more but pay less per unit. Just having that as a statement ignores unit pricing and doesn't distinguish between value per tonne vs total value. 


It would be easy to say that this could have been the hypothesis for this section but it wouldn't be just as some countries pay more than others and still don't get the value of money compared to other countries. As you will see on the revised hypothesis further down, you will get an idea that just because a country is paying more, it doesn't equate to a higher quantity.


The final point is this original hypothesis does not account for trade deals, distance or value-added processing that comes with the produce trading world nor does it factor localisation pricing. 


### *Original Hypothesis 3* Kenya’s avocado export quantity is increasing annually:
* This hypothesis is an interesting one because, yes, indeed it may be true, but again relies on time-series granularity which this dataset did not have. The pain point of this dataset is the fact that this one in particular was broken down annually, which is the main reason as to why we didn't get to explore certain angles. Temporal growth does not explain economic value or market behaviour.



## Hypothesis testing:
All visualisations that test our hypotheses can be found in this [Dashboard](https://public.tableau.com/app/profile/faiza.abdulqadir/viz/Kenyan_Avocado_Analysis/KenyanAvocadoExportsAnalysis?publish=yes) 

### * New Hypothesis 1* Some countries pay a significantly higher price per tonne for Kenyan avocados than others
#### Chart 1 - Treemap:
![Treemap](image-1.png)


*Strongly supported — treemap shows major price variation by country (e.g. Zimbabwe vs Netherlands), suggesting different pricing strategies or trade relationships.*


* The focus is narrowed down more and focuses on `value per tonne` (unit price) and now offers a country - level comparison. This factors in that countries have their own tariffs and value- added prices which makes it common knowledge when it comes to different country currencies. 


* This new hypothesis also accounts for disparities in trade relationships (e.g. Zimbabwe vs Netherlands) which upon seeing the data, is unfortunate for Zimbabwe as they are paying more especially as we should factor in that they no longer trade in their local currency but in the US dollar due to the plummet on the Rhodesian Dollar before the new Dollar was introduced.

#### Verdict:
We get to uncover premium-paying countries, which may point out more niche markets and better trade terms which is a plus for analysis. This way it shows Zimbabwe pays more per tonne, while Netherlands imports more but pays less per tonne.


### *New Hypothesis 2* The top avocado importers by quantity are not necessarily those paying the most per tonne:
#### Chart 2 - Bar Chart:
![Bar Chart](image-2.png)


*Supported — bar chart (quantity) vs treemap (value per tonne) shows clear divergence; high-volume buyers don't always pay the most per tonne.*


This hypothesis is more supported, as it gives a deep dive on the disparity between **bulk buyers** and **premium buyers**. This opens up a discussion on **value** VS **volume** as it shows more nuance and reflects more on real- world trade complexities. An interesting point to add is that The Netherlands have been big importers as they work with several international supermarket chains that operate worldwide making them the hub of importing avocados.

#### Verdict:
The Netherlands is a top importer by quantity but pays less per tonne. Whilst in contrast with Zimbabwe, they import less but at a higher value per unit.
 

### *Hypothesis 3* There is a positive relationship between Kenya’s avocado export quantity and export value, but outliers exist:
#### Chart 4 - Regressive Line (Quantity vs Value):
![Regressive Line Chart](image-3.png)


*Partially supported — regression line shows a clear positive trend, but the 'World' outlier skews the relationship slightly. Strong R² and p-value give this statistical credibility.*

**P-value – Significance of the relationship (typically should be < 0.05)**


**R² (R-squared) – Strength of the correlation (closer to 1 is strong)**


This regressive chart tests the correlation between quantity and value, so this introduces regression analysis and clusters. The part that is a little skewed but also an important aspect as it shows `outliers` like ‘World’ totals. 


#### Verdict:
This shows that generally, more export quantity results in higher value which we have shown on previous hypothesis but ‘World’ is a major outlier, likely an aggregated or unmatched entry distorting the trend.

### *BONUS HYPOTHESIS* Some countries contribute large export value through small quantities, suggesting niche or high-value markets:


#### Emerging Insight (from combining Chart 1 & 3):


This bonus insight is derived from comparing Chart 1 (value per tonne) with Chart 3 (total export value). This bonus shows the mismatch in volume vs impact and opens the discussion on premium pricing, trade efficiency and strategic partnerships.
 

## Project Plan
The project board that aided in our planning and organisation can be found [here](https://github.com/users/Fazestar01/projects/7/views/1)


### High-Level Steps Taken


**Angle Used**  
The point was to explore the agriculture world and what is happening in the world of produce. Knowing of a client, Globalwema, that is currently exporting avocados from Kenya and having an insight of the current situation and somewhat struggles they are facing in the agriculture world is a key point on this project. Currently Kenya is projected to grow year by year in avocaods as it is now becoming the top exporters for avocados in Africa, almost surpassing South- Africa, which have been the top exporters for avocados from Afrca in the last 15 years. So it only seemed right to get in front of that and support Globalwema to the growing market of avocados.


I then used a dataset website under the world bank where I found insights on the 2023 avocado reports and data.

The angle used is to analyse who the key drivers are when it comes to importing avocados from Kenya and how much is exported, also giving a feel on the volume and value.

**Dataset Selection**  
I selected the [Kenyan Avocado 2023 dataset on WITS](https://wits.worldbank.org/trade/comtrade/en/country/KEN/year/2023/tradeflow/Exports/partner/ALL/product/080440) for its reliability on the data giving the company that curated the data — including country, year, quantity making it ideal for both statistical testing and visual storytelling.

**Planning & Analysis Flow**
1. Problem Definition & Hypothesis Planning
* The initial goal was to understand how Kenya’s avocado exports differ by country in terms of value, quantity and pricing.


* Initially 3 hypotheses were developed which were later refined based on data limitations (e.g, lack of monthly/yearly data granularity)
* Focus is shifted to country-level comparisons and statistical relationships instead.

2. Data Acquisition & Cleaning
* The data was soured from (WITS) 
* Cleaned using Python (Pandas), including handling missing values, filtering out vague entries like 'World', and calculating unit price per tonne.


3. Exploratory Data Analysis (EDA)
* Conducted using Jupyter Notebook with Pandas, Seaborn and Plotly.
* Visuals like bar charts, treemaps, boxplots and regression lines were used to test hypotheses and identify patterns.


4. Hypothesis Testing 
* Each hypothesis was tested through relevant visualisations or statistical analysis
* Hypothesis 3 (correlation between quantity and value) was backed with regression analysis (p-value, R²). 


**Data Cleaning**
- Missing null values.
- Fix errors in the data.
- Filtering out vague entries like ‘World’ and calculating unit price per tonne.

### Data Management Throughout the Project

| **Step**        | **Action**                                                                                                                                             |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Collection**  | Downloaded CSV file from Kaggle and stored it in a version-controlled GitHub repository for team collaboration.                                       |
| **Processing**  | Used Python (Pandas) in Jupyter Notebook to clean and transform data, including formatting, encoding, and feature engineering.                         |
| **Analysis**    | Performed EDA in both Jupyter and Tableau. Applied statistical methods suited such as linear regression.
| **Interpretation** | Combined numeric/statistical insights (e.g., p-values) with Tableau dashboards to communicate findings through dynamic charts and annotated stories. |

---

### Rationale for Research Methodologies

- **Hypothesis-Driven Approach:** We defined practical questions relevant to strategic decisions and tested them with appropriate statistical methods.
- **Tableau Public for Storytelling:** Enabled the team to create highly interactive and filterable dashboards for accessible, intuitive data exploration.
- **Python for Processing:** All cleaning and transformation were done in Python to ensure transparency, reproducibility, and modular processing.


## The rationale to map the business requirements to the Data Visualisations
#### Identify Key Drivers of Car Price Business Need: 
Understanding which features most influence pricing to support pricing strategy or customer targeting

Viusalisation: 
- Scatter plots of Engine Size and vehicle size vs Price
- Box plots of Drive Wheel vs Price Rationale: These visuals make it easy to see trends and variation across technical specs. Outliers or clusters can suggest relationships worth exploring with statistical testing.

### Compare Brand Positioning in the Market Business Need:
Evaluate how brands are priced in relation to each other to guide competitive analysis or partnership decisions.

Visualisation: 
- Bar charts showing Average Price by Brand
- Box plots showing Price spread within each brand Rationale: Highlights both the average market position and the consistency or variation in pricing within a brand—key for brand strategy.

### Assess Pricing Strategy Based on Drive wheel Configuration Business Need:
Determine how drive wheel (FWD, RWD, 4WD) impacts perceived value or cost to align with customer preferences

Visualisation:
 - Box plots or grouped bar charts of Drive Wheel vs Price Rationale: These plots show how drive wheel types cluster at different price tiers, helping identify if pricing strategies align with drive wheel desirability.

### Monitor Variability in Price Across Technical Specs Business Need:
Understand how variability in engine size, weight, and dimensions affects pricing to spot inconsistent or misaligned pricing.

Visualisation:
- Line graphs or histograms for price distribution Rationale: Helps detect relationships between variables and whether price changes smoothly or erratically with technical attributes.

## Analysis techniques used
* The ETL pipeline was done in a Jupyter notebook using pandas which can be found  [here](https://github.com/Fazestar01/Car-Price-Analysis/blob/main/jupyter_notebooks/car_price_investigations.ipynb). This allows a structured approach to data cleaning as you can see what you've done previously very clearly.
* The data was not paticularly limiting, except it did not include what form of measurements it used. This however did not stop us identifying trends in the data. 
* We used generative AI to resolve questions regarding dashboarding and git. 

## Ethical considerations
* The dataset contains no sensitive information thus does not require anonymisation or other ethical steps.

## Dashboard Design
*The Dashboard can be found [here](https://public.tableau.com/app/profile/kaori.ikarashi/viz/CarPriceAnalysis_17501618237170/Story1?publish=yes)*.
### Dashboard preparation:
The car name consists of the brand and manufacturer, so it is grouped into manufacturer to make the visualisation less crowded.

![dashboard image](image-9.png)

We used a Tableau Story format to keep the dashboard uncluttered. Viewers can explore each hypothesis using the buttons at the top.

![dahsboard image](image-10.png)

### Dashboard for hypothesis 1:
![alt text](image-11.png)

We used scatter plots to explore the relationship between vehicle size and price, adding trend lines to highlight which size factor has the most significant impact on pricing.

The second graph uses a dual-axis chart to compare curb weight and price by car brand, helping to reveal each brand’s weight–price profile.

We added a Car Name filter, allowing viewers to focus on vehicles from a specific manufacturer quickly.

![dashboard image](image-12.png)

### Dashboard for hypothesis 2:
![dashboard image](image-14.png)

We are exploring whether brand name affects car pricing.
The first visualisation highlights which manufacturers tend to price their vehicles higher on average.
The second graph illustrates the distribution of prices within each brand, enabling us to understand how consistent a company is with its pricing and identify brands with greater price variation.

To enhance interactivity, we added Carbody and Fueltype filters, allowing viewers to explore pricing patterns across different vehicle types and fuel categories.

![dashboard image](image-15.png)

### Dashboard for hypothesis 3:

![dashboard](image-16.png)

We are analysing whether drivewheel type affects car pricing.

A box plot is used to compare the price distribution across 4WD, FWD, and RWD vehicles.
To enhance interactivity, we included the same Carbody and Fueltype filters as in Hypothesis 2, allowing viewers to explore pricing patterns in more detail.

### Our logo:

![alt text](image-18.png)

To highlight that our team created this work, Datalicious, we added our logo to the top of each page



## Development Roadmap and issues faced
* The types of measurements for things such as height, weight etc were not included, to resolve this we asked Copilot what it thought the most reasonable assumption of the measurements are.
* One aspect of data cleaning was overlooked, 'VW' should have been changed to 'Volkswagen' in the Jupyter notebook. This was solved by using the 'groupby' function in Tableau to group VW under Volkswagen. 
* We had struggles with git that were resolved with a mixture of co-pilot and help from our tutors.
* Images couldn't be moved into an image folder without them being removed from github. That will be something we look more into for the next project.




## Main Data Analysis Libraries
* Pandas
* Numpy


## Credits 

* Code Institute Learning Management System modules on pandas and tableau
* Microsoft co-pilot aid in code generation
* Chat-GPT for questions regarding dashboarding in Tableau
* [Markdown Guide](https://www.markdownguide.org/)


### Media

- Header image was made using Canva


## Acknowledgements
* A huge thank you to Mark, Emma, John, Spencer and Niel from Code institute for their hard work in tutoring us! And a thank you to Carlos who showed us how to add a back to the top button on markdown. 

[Back to top](#top)