# IS 477 Final Project 

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

│   └── .gitkeep          # Placeholder so the folder appears in GitHub, input data files after downloading from the Box folder.

│

├── .gitignore 

├── Dataset_Integration_Script.ipynb

├── IS477_Codebook.txt

├── ProjectPlan.md

├── README.md

├── Run_All_Script_IS477_Final_Project_Workbook.ipynb

├── StatusReport.md

├── pip_freeze.md

└── requirements.txt
