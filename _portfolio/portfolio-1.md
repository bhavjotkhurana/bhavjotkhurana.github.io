---
title: "Dougscore Dataset and ToolKit in R"
excerpt: "A comprehensive R dataset and analysis toolkit built around Doug DeMuro's vehicle scoring system, integrating technical specifications, comparison tools, and GPT-generated summaries.<br/><img src='/images/doug.png'>"
collection: portfolio
---

*THIS* is a data-driven project inspired by automotive journalist Doug DeMuro’s unique and structured car review system. Doug's reviews assign scores to various categories across two domains: *weekend score* and *daily score*, each contributing to a 100-point total. These scores have become a widely referenced benchmark among car enthusiasts, especially in YouTube and automotive blog communities.

This project takes the DougScore concept and builds a reproducible, extensible dataset and analysis toolkit in R. To look at or use the code and dataset you can check out the [Github repository](https://github.com/bhavjotkhurana/dougscore-dataset).

## Data Collection and Augmentation

The DougScore dataset used in this project was not directly available as a structured file, so I developed it from the ground up through a multi-step process:

- **Web Scraping:** I extracted many car entries and their associated DougScores from the Automobile Catalog Website and YouTube descriptions using targeted scraping scripts.
- **Manual Entry:** For a large subset of cars, especially rare or older models, I entered values by hand to ensure accuracy and coverage.
- **LLM-Assisted Completion:** For a portion of technical specifications (e.g., transmission type, fuel economy, displacement), I used a large language model to supplement missing entries when they were difficult to extract programmatically.

This hybrid approach resulted in a dataset of over 550 vehicles, enriched with real-world specifications and contextual labels.

## Dataset Overview

Each car entry includes:

- `year`, `make`, `model`: Identifying information
- DougScore components: `styling`, `acceleration`, `handling`, `fun_factor`, `cool_factor`, `features`, `comfort`, `quality`, `practicality`, `value`
- Calculated metrics: `weekend_score`, `daily_score`, `total_score`
- Specifications: `mpg`, `hp`, `displacement`, `transmission`, `fuel`, `cylinders`
- Flags and adjustments: `rotary_engine` (boolean), `cylinders_numeric` (cleaned numeric field)

This dataset is designed to be both human-readable and programmatically tractable, making it ideal for analysis, visualization, and modeling.

## Toolkit Features

The toolkit includes a suite of functions written in R for exploration, comparison, and visualization:

### Search and Filtering
- `search_cars()`: Allows fuzzy or partial text matching for vehicle queries
- `filter_by()`: Filters based on any categorical or text column, such as make or year

### Comparison and Similarity
- `compare_cars()`: Returns a tabular comparison of key specs and scores
- `find_similar_cars()`: Uses normalized feature distances to return vehicles most similar to a selected car

### Summarization with Language Models
- `get_car_summary_llm()`: Uses OpenAI’s GPT model to generate short summaries in the tone of Doug DeMuro
- `compare_cars_llm()`: Produces a side-by-side natural language comparison of two cars
- `generate_doug_joke()`: Generates a humorous one-liner mimicking the style of Doug’s YouTube titles

### Visualization Tools
- `plot_comparison()`: Compare selected cars on any numeric metric
- `plot_metric_by_make()`: Rank makes by average DougScore or specification
- `plot_score_vs_spec()`: Scatterplot DougScores against variables like mpg or horsepower
- `plot_score_by_carplay()`: Analyze the impact of features (e.g., Apple CarPlay) on scores

## Why I Built This

I’ve long appreciated Doug DeMuro’s approach to reviewing cars—not just for its structured scoring system but for how it blends enthusiasm, practicality, and personality. As someone with a background in data science and a passion for automotive design, I wanted to create a dataset that reflects both the analytical and subjective elements of car ownership.

DougScoreR is my attempt to formalize that structure while building a platform for meaningful comparisons and exploratory analysis. This project also served as a way to deepen my skills in web scraping, data cleaning, LLM integration, and R package development.

## Next Steps

The project is currently implemented in RMarkdown and fully version-controlled. It is being refactored into an R package for broader reusability and modularity. A Shiny dashboard for interactive browsing and comparison is also planned.
