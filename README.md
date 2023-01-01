# Kaggle GoDaddy Microbusiness Density-Forecasting Competition
Repository created for Kaggle competition: https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/overview/description.

## Basic Description

The goal of this competition is to predict monthly microbusiness density in a given area. You will develop an accurate model trained on U.S. county-level data.

Your work will help policymakers gain visibility into microbusinesses, a growing trend of very small entities. Additional information will enable new policies and programs to improve the success and impact of these smallest of businesses.

## Data Description

Your challenge in this competition is to forecast microbusiness activity across the United States, as measured by the density of microbusinesses in US counties. Microbusinesses are often too small or too new to show up in traditional economic data sources, but microbusiness activity may be correlated with other economic indicators of general interest.

As historic economic data are widely available, this is a forecasting competition. The forecasting phase public leaderboard and final private leaderboard will be determined using data gathered after the submission period closes. You will make static forecasts that can only incorporate information available before the end of the submission period. This means that while we will rescore submissions during the forecasting period we will not rerun any notebooks.

### Files

A great deal of data is publicly available about counties and we have not attempted to gather it all here. You are strongly encouraged to use external data sources for features.

**train.csv** - training dataset
- `row_id` - an ID code for the row
- `cfips` - a unique identifier for each county using the Federal Information Processing System. The first two digits correspond to the state FIPS code, while the following 3 represent the county.
- `county_name` - the written name of the county.
- `state_name` - the name of the state.
- `first_day_of_month` - the date of the first day of the month.
- `microbusiness_density` - microbusinesses per 100 people over the age of 18 in the given county. This is the target variable. The population figures used to calculate the density are on a two-year lag due to the pace of update provided by the U.S. Census Bureau, which provides the underlying population data annually. 2021 density figures are calculated using 2019 population figures, etc.
- `active` - the raw count of microbusinesses in the county. Not provided for the test set.

**sample_submission.csv** - a valid sample submission. This file will remain unchanged throughout the competition.
- `row_id` - an ID code for the row.
- `microbusiness_density` - the target variable.

**test.csv** - metadata for the submission rows. This file will remain unchanged throughout the competition.
- `row_id` - an ID code for the row.
- `cfips` - a unique identifier for each county using the Federal Information Processing System. The first two digits correspond to the state FIPS code, while the following 3 represent the county.
- `first_day_of_month` - the date of the first day of the month.

**revealed_test.csv** - During the submission period, only the most recent month of data will be used for the public leaderboard. Any test set data older than that will be published in **revealed_test.csv**, closely following the usual data release cycle for the microbusiness report. We expect to publish one copy of **revealed_test.csv** in mid February. This file's schema will match **train.csv**.

**census_starter.csv** Examples of useful columns from the Census Bureau's American Community Survey (ACS) at data.census.gov. The percentage fields were derived from the raw counts provided by the ACS. All fields have a two year lag to match what information was avaiable at the time a given microbusiness data update was published.
- `pct_bb_[year]` - The percentage of households in the county with access to broadband of any type. Derived from ACS table B28002: PRESENCE AND TYPES OF INTERNET SUBSCRIPTIONS IN HOUSEHOLD.
- `cfips` - The CFIPS code.
- `pct_college_[year]` - The percent of the population in the county over age 25 with a 4-year college degree. Derived from ACS table S1501: EDUCATIONAL ATTAINMENT.
- `pct_foreign_born_[year]` - The percent of the population in the county born outside of the United States. Derived from ACS table DP02: SELECTED SOCIAL CHARACTERISTICS IN THE UNITED STATES.
- `pct_it_workers_[year]` - The percent of the workforce in the county employed in information related industries. Derived from ACS table S2405: INDUSTRY BY OCCUPATION FOR THE CIVILIAN EMPLOYED POPULATION 16 YEARS AND OVER.
- `median_hh_inc_[year]` - The median household income in the county. Derived from ACS table S1901: INCOME IN THE PAST 12 MONTHS (IN 2021 INFLATION-ADJUSTED DOLLARS).


## Evaluation

Submissions are evaluated on <a href="https://en.wikipedia.org/wiki/Symmetric_mean_absolute_percentage_error">SMAPE</a> between forecasts and actual values. We define SMAPE = 0 when the actual and predicted values are both 0.

### Submission File
For each `row_id` you must predict the `microbusiness_density`. The file should contain a header and have the specific format detailed <a href="https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/overview/evaluation">here</a>.

The submission file will remain unchanged throughout the competition. However, the actively scored dates will be updated as new data becomes available. During the active phase of the competition only the most recent month of data will be used for the public leaderboard.

## Timeline

* December 15, 2022 - Start Date.
* March 7, 2023 - Entry Deadline. You must accept the competition rules before this date in order to compete.
* March 7, 2023 - Team Merger Deadline. This is the last day participants may join or merge teams.
* March 14, 2023 - Final Submission Deadline.

Forecasting Timeline: Starting after the final submission deadline there will be periodic updates to the leaderboard to as new data becomes available for inclusion in solution file. Updates will take place once a month.

**June 14, 2023 - Competition End Date - Winner's announcement**

## Prizes

* First Prize: $20,000
* Second Prize: $15,000
* Third Prize: $10,000
* Fourth Prize: $5,000
* Fifth Prize: $5,000
* Sixth Prize: $5,000

## Code Requirements

Submissions to this competition must be made through Notebooks. In order for the "Submit" button to be active after a commit, the following conditions must be met:

* CPU Notebook <= 9 hours run-time
* GPU Notebook <= 9 hours run-time
* Internet access disabled
* Freely & publicly available external data is allowed, including pre-trained models
* Submission file must be named submission.csv

Please see the Code <a href="https://www.kaggle.com/docs/competitions#notebooks-only-FAQ">Competition FAQ</a> for more information on how to submit. And review the <a href="https://www.kaggle.com/code-competition-debugging">code debugging doc</a> if you are encountering submission errors.

## Additional Context for Competition

American policy leaders strive to develop economies that are more inclusive and resilient to downturns. They're also aware that with advances in technology, entrepreneurship has never been more accessible than it is today. Whether to create a more appropriate work/life balance, to follow a passion, or due to loss of employment, studies have demonstrated that Americans increasingly choose to create businesses of their own to meet their financial goals. The challenge is that these "microbusinesses" are often too small or too new to show up in traditional economic data sources, making it nearly impossible for policymakers to study them. But data science could help fill in the gaps and provide insights into the factors associated these businesses.

Over the past few years the Venture Forward team at GoDaddy has worked hard to produce data assets about the tens of millions of microbusinesses in the United States. Microbusinesses are generally defined as businesses with an online presence and ten or fewer employees. GoDaddy has visibility into more than 20 million of them, owned by more than 10 million entrepreneurs. We've surveyed this universe of microbusiness owners for several years and have collected a great deal of information on them that you can access via our survey data here.

Current models leverage available internal and census data, use econometric approaches, and focus on understanding primary determinants. While these methods are adequate, there's potential to include additional data and using more advanced approaches to improve predictions and to better inform decision-making.

Competition host GoDaddy is the world’s largest services platform for entrepreneurs around the globe. They're on a mission to empower their worldwide community of 20+ million customers—and entrepreneurs everywhere—by giving them all the help and tools they need to grow online.

Your work will help better inform policymakers as they strive to make the world a better place for microbusiness entrepreneurs. This will have a real and substantial impact on communities across the country and will help our broader economy adapt to a constantly evolving world.
