### Airbnb Listing Quality Analysis

#### Question:
What is the relationship between Airbnb Superhost status, neighborhood location, and listing quality (as measured by guest reviews) in California?

---

### Data Source

I located this dataset on kaggle, at **Inside Airbnb on Kaggle**. This dataset is outdated (last updated in 2021), however I was able to find more current datasets on the main Inside Airbnb website at `https://data.insideairbnb.com/`. There is a lot of data, but I am just going to focus on California. I have downloaded most recent data already from the site.

The attached file has the number of lines (wc -l) of each of the csv files, as you can see:

```
% grep /data/listings.csv data-full-list.txt | sort -n
    795 data.insideairbnb.com/united-states/ca/pacific-grove/2024-12-31/data/listings.csv
   2849 data.insideairbnb.com/united-states/ca/santa-cruz-county/2024-12-31/data/listings.csv
   4582 data.insideairbnb.com/united-states/ca/oakland/2024-12-22/data/listings.csv
   7667 data.insideairbnb.com/united-states/ca/san-mateo-county/2024-12-23/data/listings.csv
  17003 data.insideairbnb.com/united-states/ca/san-francisco/2025-03-01/data/listings.csv
  17099 data.insideairbnb.com/united-states/ca/santa-clara-county/2024-12-23/data/listings.csv
  28013 data.insideairbnb.com/united-states/ca/san-diego/2024-12-23/data/listings.csv
  82935 data.insideairbnb.com/united-states/ca/los-angeles/2025-03-01/data/listings.csv
```

Pacific Grove has only 795 listings and LA has like 82K listings.

---

### Techniques

The analysis will employ standard data analytics methods, including data cleaning (such as converting price fields to numeric values and standardizing categorical variables), sentiment analysis using TextBlob to assign polarity scores to review texts, and keyword frequency analysis to quantify the presence of quality-related terms. A composite quality metric will be developed by integrating sentiment scores, keyword weights, and normalized review volume. Statistical comparisons, such as the Mann-Whitney U test, will be used to evaluate differences in quality scores between Superhosts and non-Superhosts. Spatial aggregation will be applied to identify neighborhood-level trends. Additionally, Large Language Models (LLMs) may be utilized to extract nuanced thematic patterns from reviews, supplementing traditional natural language processing approaches while maintaining transparency and reproducibility.

---

### Expectations

1. **Neighborhood Rankings**
   - Table of neighborhoods ranked by median quality score.

2. **Host Status Comparison**
   - Chart showing quality score distributions for Superhosts vs. regular hosts.

3. **Review Themes**
   - Summary of most frequent positive/negative themes (e.g., "20% of negative reviews cite noise").

---

### Importance

#### **Stakeholder Impact**

- **Policymakers**:  
  Without this analysis, cities lack data to regulate short-term rentals effectively, risking housing shortages in neighborhoods with high commercial Airbnb activity.

- **Hosts**:  
  Hosts cannot objectively benchmark their performance or prioritize improvements (e.g., cleanliness vs. amenities) to achieve Superhost status.

- **Guests**:  
  Travelers have no systematic way to identify high-quality listings, leading to inconsistent experiences.

#### **Consequences of Inaction**

- Unregulated growth of short-term rentals in residential areas.
- Hosts investing in irrelevant upgrades due to lack of guest feedback insights.
- Guests relying on subjective reviews rather than data-driven quality metrics.

#### **Benefits of Analysis**

- **Policymakers**: Identify neighborhoods needing regulatory intervention.
- **Hosts**: Receive actionable feedback to improve listing quality and guest satisfaction.
- **Guests**: Access objective quality scores for informed booking decisions.

---

### Implementation Plan

This will involve using paid/$$ calls to a LLM, and I am not sure of how much this will run into so I will go in 2 stages:

1. **Initial Attempt: Pacific Grove**
   - Develop and validate methodology on the 794-listing dataset.

2. **May be scale/adapt to bigger cities**
   - Apply to larger cities (e.g., Los Angeles) if LLM API costs for review analysis are feasible.

---
