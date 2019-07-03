---
title: Prep
nav: true
--- 

# Turn Your Transcript Into a CSV

**Prep Your Word Document:**
- Get rid of space between paragraphs: 
    - In word, open Find and Replace. In the Find box, type `^p^p`. In the Replace box, type `^p`. 
    - Replace All.

**Paste to Google Sheets:**
- Open a blank Google Sheet. Copy all of the text from your word document. In your new spreadsheet, click on `Edit > Paste Special > Paste Values Only`. This makes each paragraph into a single cell.

**Split up Your Cells:**
- Highlight Column A. Click on `Data > Split Text to Columns`. 
    - A `Separator` drop-down box will appear on your screen. 
    - Click the drop-down and choose `Custom`. 
    - Type `[` into the box that says `Custom Separator`. 
    - Title this column "speaker."
- Highlight Column B. Click on `Data > Split Text to Columns`. 
    - A `Separator` drop-down box will appear on your screen. 
    - Click the drop-down and choose `Custom`. 
    - Type `]` into the box that says `Custom Separator`. 
    - Title Column B "timestamp" and Column C "words." 
- Highlight the "words" column. Click on `Format > Text wrapping > Wrap`. 
    - *Note: Some of the text in the "words" column may have overflowed into Column D. Scroll through the spreadsheet and copy and paste any stray text back into the "words" column.*
- Title Column D "tags".