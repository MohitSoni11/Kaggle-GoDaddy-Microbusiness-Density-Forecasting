# Kaggle GoDaddy Microbusiness Density-Forecasting Competition
Repository created for Kaggle competition: https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/overview/description.

## Description

The goal of this competition is to predict monthly microbusiness density in a given area. You will develop an accurate model trained on U.S. county-level data.

Your work will help policymakers gain visibility into microbusinesses, a growing trend of very small entities. Additional information will enable new policies and programs to improve the success and impact of these smallest of businesses.

### Context

American policy leaders strive to develop economies that are more inclusive and resilient to downturns. They're also aware that with advances in technology, entrepreneurship has never been more accessible than it is today. Whether to create a more appropriate work/life balance, to follow a passion, or due to loss of employment, studies have demonstrated that Americans increasingly choose to create businesses of their own to meet their financial goals. The challenge is that these "microbusinesses" are often too small or too new to show up in traditional economic data sources, making it nearly impossible for policymakers to study them. But data science could help fill in the gaps and provide insights into the factors associated these businesses.

Over the past few years the Venture Forward team at GoDaddy has worked hard to produce data assets about the tens of millions of microbusinesses in the United States. Microbusinesses are generally defined as businesses with an online presence and ten or fewer employees. GoDaddy has visibility into more than 20 million of them, owned by more than 10 million entrepreneurs. We've surveyed this universe of microbusiness owners for several years and have collected a great deal of information on them that you can access via our survey data here.

Current models leverage available internal and census data, use econometric approaches, and focus on understanding primary determinants. While these methods are adequate, there's potential to include additional data and using more advanced approaches to improve predictions and to better inform decision-making.

Competition host GoDaddy is the world’s largest services platform for entrepreneurs around the globe. They're on a mission to empower their worldwide community of 20+ million customers—and entrepreneurs everywhere—by giving them all the help and tools they need to grow online.

Your work will help better inform policymakers as they strive to make the world a better place for microbusiness entrepreneurs. This will have a real and substantial impact on communities across the country and will help our broader economy adapt to a constantly evolving world.

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
