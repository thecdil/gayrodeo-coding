---
title: 3 - Upload
nav: true
---

# Add Your Content to the Repository

**Add Your New Tags:**
- Open `_data/filters.csv`. Add the tags you've used to encode your transcript. The "shortfilter" column should contain the tags exactly as they appear in your spreadsheet. The "text" column is a place to define or describe the tags.

**Add Your Transcript:**
- In Google Sheets, click on `File > Download as > Comma-separated values (.csv)`.
- Name your csv the last name of the interviewee, all lowercase (for example, Joe Vandal's interview would have the filename `vandal.csv`).
- Add your csv to the `_data/transcripts` directory.

**Add Some Information About the Transcript:**
- Navigate to the `_transcripts` directory.
- Create a new Markdown file (file extension `.md`). Title it with the same last name as your csv (i.e. `vandal.md`)
- Copy all text from an existing markdown file in the same directory.
- Change the data in your new markdown file to reflect information about the interviewee, date interviewed, location, interviewer, etc.
- Save your new markdown file.