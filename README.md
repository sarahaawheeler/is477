# IS 477 Final Project Report: Analyzing COVID-era Instagram Sentiment in relation to Vaccination Rates

### Contributors
* Megan Sia
* Sarah Wheeler

### Summary
We aim to understand how public sentiment surrounding the COVID-19 pandemic has shifted over time, with particular attention to the period before and after the introduction of COVID-19 vaccines, as well as different vaccine uptake rates. The pandemic, by forcing people into quarantine and limiting in-person interaction, made digital platforms one of the primary channels through which individuals expressed their thoughts, fears, and hopes. As a result, online platforms such as Instagram provide a large dataset for tracking evolving public opinion.

Our motivation centers on the nature of the pandemic as both a public health crisis and as the catalyst for the creation of an information environment defined by emotionally charged expression. Vaccines were rolled out worldwide as a turning point since they offered a path toward reduced disease severity and a return to normalcy. Because of this, we hypothesized that increasing vaccinations might correspond with increases in positive sentiment. More vaccinations might signal increased protection, optimism, and relief, which would be reflected in the content posted on Instagram.

To explore this, we combined two datasets. The first, “COVID-19 Vaccinations” by Our World in Data, contains global vaccination statistics, including both daily and cumulative vaccination measures. This dataset offers clear indicators of how vaccination campaigns progressed over time. The second dataset, “Five Years of COVID-19 Discourse on Instagram,” contains more than 500,000 posts labeled as positive, neutral, or negative sentiment. This integration allows us to ask: How does online sentiment toward the pandemic change in relation to vaccination trends, and is there any observable relationship between the two over time? The merged dataset (see in Box folder linked below) allows us to examine whether increases in new vaccinations or cumulative vaccination milestones correspond with shifts in positive sentiment on Instagram. 
We also acknowledge limitations that shape the interpretation of our results. Instagram users represent a narrower demographic slice. They are typically younger, more engaged online, and not necessarily representative of the global population. Posts may be influenced by news events, political developments, misinformation cycles, personal circumstances, or even the use of hashtags for unrelated content. Likewise, vaccination data is subject to uneven global reporting practices, with some countries lacking consistent or complete information.

Even with these limitations, integrating these datasets provides an opportunity to examine COVID-era discourse. Rather than claiming causality, our goal was to identify patterns that reveal how people responded emotionally during major phases of the pandemic. Throughout the project, we maintained data management practices by creating a comprehensive README and codebook, documenting each preprocessing step, and ensuring that all intermediate files were derived directly from the original sources. To preserve data integrity and provenance, we stored the files separately, avoided manual edits, and relied exclusively on reproducible code to clean, merge, and analyze the datasets. Ultimately, our findings indicate a weak positive relationship between vaccination rates and positive sentiment, suggesting that while public health progress may influence online discourse, it does so in complex ways shaped by many other social factors.

### Data Profile 
The two datasets we picked to utilize for our project are “COVID-19 Vaccinations” and “Five Years of COVID-19 Discourse on Instagram.” The vaccination dataset documents the globally-reported COVID-19 vaccinations from 2020 to 2023. Sourced from Our World in Data, the vaccination dataset offers information on the progress of international vaccination campaigns (Mathieu et al., 2024). The dataset includes vaccinations at both the subnational, national, and international aggregate. We chose to use the national level for our analysis, but meta analyses can be conducted for regions like Northern Ireland or entities like the European Union. In addition to the number of total vaccinations, the dataset includes a number of per capita metrics that are calculated based on the United Nations World Population Prospects. The sentiment classification dataset addresses public discourse on the pandemic, covering 500,123 posts in 161 languages published between January 2020 and September 2024. The multilingual analysis was performed by classifying each post as positive, negative, or neutral. To perform the data mining process, a list of trending hashtags related to COVID-19 was developed (Thakur, 2024). The posts that contained at least one hashtag related to COVID-19 and were published between January 21, 2020, and September 23, 2024, were mined using the Instagram API. All posts that were collected during this data mining process were posted by accounts that were public at the time of mining and did not necessitate needing an Instagram account to view. It should be noted that the main criteria for assuming the post was COVID-19 related was the inclusion of the hashtag. This introduces the possibility of including irrelevant posts made by users spamming a number of hashtags or using trending hashtags to expand their reach. Utilizing these datasets allows for examining the relationship between vaccination efforts and public sentiment on social media.  

Additionally, one of the reasons these datasets were selected is because they capture two essential dimensions of the pandemic: objective health outcomes and subjective public perception. Vaccination numbers provide a quantifiable measure of health outcomes, distribution capacity, and government response to COVID-19, while sentiment analysis reflects how different global populations are perceiving and reacting to the circumstances. By integrating the datasets, we can thus attempt to evaluate whether the increasing use of the vaccination (presumably offering hope and better prognosis for those infected with the virus) has any effect on how people perceive the pandemic itself based on the content they are posting online.

However, it should be mentioned that both datasets come with limitations. Vaccination data may be incomplete in regions with poor reporting infrastructure, meaning the data may not represent the true population statistic. There are also some regions that do not report numbers at all, or whose data has previously been falsified, adding a layer of uncertainty to our analysis. On the sentiment side, Instagram users represent only a fraction of the global population. People may post differently on Instagram than they may on Twitter or other social media sites. This may create demographic bias and inaccurately reflect populations with those less engaged with social platforms. 

### Data Quality 
The public sentiment dataset includes a DOI (https://doi.org/10.5281/zenodo.13896353), ensuring permanent retrievability and citation consistency. The vaccination dataset does not have a DOI but is hosted on a searchable repository with metadata and contributor information. Both datasets can be located using repository search tools and relevant keywords. The path of the vaccination repository, can be found at https://github.com/owid/covid-19-data/blob/master/public/data/README.md, complete with a codebook, author contribution, and changelog. Since both datasets are hosted on secure sites with a sufficient amount of metadata, we felt that we had the necessary information needed to properly analyze and understand the data. 

Both datasets are publicly available and downloadable through HTTPS links. Due to this, the datasets are open access for researchers and practitioners. Furthermore, the hosting platforms of the dataset, Zenodo and GitHub, guarantee stable data storage. Therefore, the datasets remain accessible after updates or revisions. This consistent availability supports reproducibility and long-term usability. Each dataset provides essential information such as data collection methods and documentation that outline the dataset’s purpose and structure. Both are released under the CC BY 4.0 open license which allows users to freely share and adapt the data with proper attribution. This licensing supports the responsible reuse of data in future studies.

Throughout the project, we considered how we can make our integrated dataset reliable and usable. Our integrated dataset was a result of merging the public sentiment dataset with the vaccination dataset. The first step we took to integrating the datasets was ensuring we cleaned both datasets. Fortunately, both original datasets were largely clean upon download. There was minimal missingness, and they both had consistent formatting. The integration process was straightforward and required little preprocessing. Nonetheless, we performed several quality checks to ensure that the merged dataset was accurate and suitable for analysis.

Across all four dimensions of data quality, the merged dataset ultimately proved to be fit for our use. Because the integrated dataset was accurate, complete for our time window, consistent with schema expectations, and appropriately aligned in terms of timing, it fully supported the analytical questions we aimed to answer. The dataset was suitable for the specific purpose of comparing Instagram public sentiment and vaccination trends during the COVID-19 era.

Both datasets were also largely accurate upon download. To verify its accuracy, we cross-checked key variables such as vaccination counts and geographic identifiers in comparison to global health records. After merging the datasets, we repeated this validation step by recalculating summary statistics and comparing them to publicly available figures. This ensured that no inaccuracies were introduced during the integration process.

The datasets showed no meaningful incompleteness during our selected time period, making them suitable for integration. The sentiment dataset included all necessary attributes described in its documentation, and the vaccination dataset provided full coverage for the dates and locations needed. Because our analysis focused on a defined historical period, completeness was especially important, and both datasets met this requirement.

The vaccination dataset followed a clear schema and codebook published on GitHub, and our integrated dataset preserved this structure. Although the public sentiment dataset lacked a formal codebook, its variables aligned with the dataset description. During integration, we ensured that variable types and units matched across both datasets to maintain internal consistency. While timeliness was less critical because the project analyzes historical rather than real-time trends, we ensured alignment of the two datasets by filtering them to the same date range before merging. There were no major gaps or irregularities during the selected period.

## Data Collection & Acquisition
Link to Box folder with datasets: https://uofi.box.com/s/e7e2673dnqdzk1yvtle374cq8okac1um

To acquire the data from its original source:
   1. Navigate to https://zenodo.org/records/13896353.
   2. Scroll to the bottom after reading through the metadata and determining suitability.
   3. Click the download button next to "Dataset.xlsx." The size should be 121.9 MB.
   4. Run a command to get the hash value of the data (ex: certutil -hashfile "C:\Users\xxx\Downloads\data\Dataset.xlsx" SHA512).
   5. Compare the resulting hash against the reference hash listed below.

   6. Navigate to https://github.com/owid/covid-19-data/blob/master/public/data/README.md.
   7. Scroll to "Download our complete COVID-19 dataset : CSV | XLSX | JSON."
   8. Click CSV to download the full dataset.
   9. Repeat steps 4-5.


## Hashes 
Hash for "Dataset.xlsx": 2fc56f6a6f5677d9803cf37f41ab53138a0a29afe3aadeab972a3ff7e7a19eefe36d93e41e25a6514fe999fd6d885070d49420f285723853c39c094b2dc7171d

Hash for "owid-covid-data.csv": 5bd0a9d616a1adf91575e54eb803acaab1d1a1212bd839a8f7f05c1de9d0ec614879711b521c011528c278e314580662ec67aa2ad666864e9ec0626d6b45c113


This project uses a directory structure. The GitHub repository stores only code and documentation, while all input and output datasets are stored in a separate Box folder (see above) due to size and privacy requirements. Regarding naming conventions, we followed the required names in the IS 477 project documentation for all project-oriented documentation.

## Filesystem Layout

The filesystem layout is as follows:

is477/
│

├── data/

│   └── .gitkeep                               # Placeholder so the folder appears in GitHub; actual data stored in Box.

│

├── scripts/

│   ├── Data_Integration_Script.ipynb           # Script for integrating datasets.

│   ├── Data_Quality_Script.ipynb               # Script for cleaning data.

│   ├── Data_Analysis_Script.ipynb              # Script for analysis and visualizations.

│   ├── Run_All_Script_IS477_Final_Project_Workbook.ipynb   # Script to reproduce the entire workflow.

│

├── .gitignore

├── IS477_Codebook.txt

├── ProjectPlan.md

├── README.md

├── StatusReport.md

├── pip_freeze.md

└── requirements.txt
