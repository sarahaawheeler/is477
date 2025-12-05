# IS 477 Final Project 

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
          
Hash for "Dataset.xlsx": 95437d289889f90c76541a477488d6c13633d00af1a996e58b1069e39947d91680eb680ff63a8b0ce6abdfad290d49fd2caa81f9c07636e4f2e80cb01528c1ed

Hash for "owid-covid-data.csv": 5bd0a9d616a1adf91575e54eb803acaab1d1a1212bd839a8f7f05c1de9d0ec614879711b521c011528c278e314580662ec67aa2ad666864e9ec0626d6b45c113


This project uses a directory structure. The GitHub repository stores only code and documentation, while all input and output datasets are stored in a separate Box folder (see above) due to size and privacy requirements.

The filesystem layout is as follows:

is477/

│
├── data/   

│   └── .gitkeep          # Placeholder so the folder appears in GitHub

│

├── .gitignore 

├── Dataset_Integration_Script.ipynb

├── Run_All_Script_IS477_Final_Project_Workbook.ipynb

├── ProjectPlan.md

├── StatusReport.md

├── README.md

└── requirements.txt
