# DS105-Module
Examples of summative work for DS105 module

## Notebooks Folder
**1. NB01 Data Collection - 28109**
- This notebook scrapes the LSE's IR dept webpage
- Output: Menu.json (A dictionary of the subheadings and their links)
- Output: Images folder (Data/Images) scraping all images and placing in respective folder from webpage

**2. NB01 Data Collection Notebook**
- This notebook first scrapes the Peaky Blinders Fandom Wiki, creating an output of Peaky_blinders_epsiodes.csv which contains the Season Number; Season Url; Episode number; Episode Name; Episode Url and Air date for all seasons
- Then it scrapes the synopsis for all episodes and collects all the hyperlinks per episode that are contained within the synopsis. Peaky_blinders_synopsis.csv contains the Season Number; Episode number; Paragraph Id; Hyperlink title; Link url for every hyperlink across all episodes, seasons 1-6.

**3. NB02 Data Analysis Notebook**
   -  This notebook creates two plots:
         1. Using ggplot: 'Top 20 most common first hyperlink in the synopsis across seasons'
         2. Using matplotlib: 'Most mentioned characters throughout the seasons'
    

