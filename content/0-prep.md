---
title: 1 - Prep
nav: true
--- 

# Turn Your Transcript Into a CSV

**Start Your Transcript Off Right**  

Doing the following very early on will save lots of time later on:
- Format each speaking instance as follows: `Speaker:* [01:23] Then the words they say`
- Put empty brackets (`[ ]`) for any speaking instances you don't have timestamps for.

**Prep Your Word Document:**
- Get rid of space between paragraphs: 
    - In Microsoft Word, open Find and Replace (Ctrl+H). In the Find box, type `^p^p`. In the Replace box, type `^p`. 
    - Replace All.
    - This will remove all white space between paragraphs.
    - **Note:** You may also need to highlight all (Ctrl+A) and go to: `File > Line and Paragraph Spacing > Remove Space Before Paragraph` (and) `Remove Space After Paragraph`
- The prepared Word Doc should look something like this:
{% include figure.html img="prep-1.png" width="100%" %}

**Paste to Google Sheets:**
- Open a blank Google Sheet.
- In the top left cell, copy all of the text from your word document. 
    - You'll want just the plain text, so copy your text this way: `Edit > Paste Special > Paste Values Only`. 
    - This makes each paragraph into a single cell.

{% include figure.html img="prep-2.png" width="100%" %}

**Split up Your Cells:**
- Insert a blank row of cells at the very top of the spreadsheet (so we can title columns in a bit)
- Highlight Column A (where all of your text currently resides). 
- Click on `Data > Split Text to Columns`. 
    - A `Separator` drop-down box will appear on your screen (sometimes way down at the bottom). 
    - Click the drop-down and choose `Custom`. 
    - Type `* [` into the box that says `Custom Separator`. 
        - This will delete the `*` from your speaker's name and the `[` from the beginning of your timestamp, and that's okay.
    - Column A should now consist only of speaker name tags ending in `:`
    - Title this Column `speaker` (lowercase)
{% include figure.html img="prep-3.png" width="100%" %}
{% include figure.html img="prep-4.png" width="100%" %}
{% include figure.html img="prep-5.png" width="100%" %}
- Highlight Column B (which now should only contain time stamps and the words spoken).
- Click on `Data > Split Text to Columns`. 
    - A `Separator` drop-down box will appear on your screen. 
    - Click the drop-down and choose `Custom`. 
    - Type `]` into the box that says `Custom Separator`. 
    - Title Column B `timestamp` (lowercase)
    - Title Column C `words` (lowercase) 
- Highlight the `words` column. 
- Click on `Format > Text wrapping > Wrap`. 
    - *Note: Some of the text in the `words` column may have overflowed into Column D. Scroll through the spreadsheet and copy and paste any stray text back into the `words` column.*
- Title Column D `tags`.

# Your Spreadsheet Should Now Look Something Like This:

{% include figure.html img="finished-csv.png" width="75%" %}
