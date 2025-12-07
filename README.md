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
