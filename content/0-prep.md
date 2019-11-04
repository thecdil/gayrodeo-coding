---
title: 1 - Prep
nav: true
--- 

# Preparing Your Transcript

- [Paste Your Transcript Into Google Sheets](#sheets)
- [Separate the Cells](#cells)
- [Check for Errors](#errors)
- [Read Your Transcript](#read)
- [Naming Your Transcript](#name)

{:.pt-4 .mt-4 #sheets}
***

## Paste Your Transcript Into Google Sheets

- Create a new Google Sheet

- In the first row, title four columns `timestamp`, `speaker`, `words`, and `tags`

- In a new browser tab, open your transcript as a Google Doc

- Copy all of the text of the transcript (leave out any biographical information at the beginning)

- Switch back to the Google Sheet you created

- Click on the cell underneath `speaker` 

- Click on `Edit` > `Paste Special` > `Paste Values Only`

{% include figure.html img="/prep/transcript1.png" caption="Edit > Paste Special > Paste Values Only" alt="a screenshot of pasting text in google sheets" width="100%" %}

- This should paste all the transcript text into the rows of the second column

- **Note**: Your transcript rows should ***not*** have a space between them. If you *do* have spaces between your rows, see below.

{% capture spacing %}
### Removing Spacing Between Rows

If the text you paste into your Google Sheet looks like this...

{% include figure.html img="/prep/transcript15.png" caption="Transcript With Spaces" alt="a screenshot showing how to edit a markdown file on GitHub" width="100%" %}

...you need to remove the space between paragraphs in your Google Doc. Follow the steps below:

{:.pt-3}
- Return to the Google Doc version of your transcript

{:.pt-1}
- Select all of the transcript text

{:.pt-1}
- In the top right of the screen, look for the `line spacing` button (three horizontal lines next to a vertical arrow). In the dropdown options, click on `Custom spacing`.

{% include figure.html img="/prep/transcript16.png" caption="Line Spacing" alt="a screenshot showing how to edit a markdown file on GitHub" width="100%" %}

- A `Custom spacing` popup will appear. Make sure the text boxes to the right of `Before` and `After` have values of `0`. Click `Apply`:

{% include figure.html img="/prep/transcript17.png" caption="Custom spacing" alt="a screenshot showing how to edit a markdown file on GitHub" width="100%" %}

- Now follow the steps above to copy and paste this text into your Google Sheet

{% endcapture %}
{% include bootstrap/alert.md text=spacing color="warning" %}

{:.pt-4 .mt-4 #cells}
***

## Separate Your Cells

- If they aren't highlighted already, highlight the cells you just pasted, so that your sheet looks like this:

{% include figure.html img="/prep/transcript2.png" caption="Highlight Cells" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Click on `Data` > `Split Text to Columns`

{% include figure.html img="/prep/transcript3.png" caption="Data > Split Text to Columns" alt="a screenshot of pasting text in google sheets" width="100%" %}

- A little box labeled `Separator:` will appear near the bottom of your screen. Click on the arrows to the right of `Detect Automatically`

{% include figure.html img="/prep/transcript4.png" caption="Separator" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Select `Custom` from the list of choices that appears.

- A box should appear labeled `Custom separator`

- Enter a **colon (`:`) followed by a space** into this box.

{:.alert .alert-danger .text-center .mx-5}
Make sure **your colon is followed by a space**! Otherwise your transcript will be a lot more difficult to clean up.

{% include figure.html img="/prep/transcript9.png" caption="Enter a colon (:) followed by a space" alt="a screenshot of pasting text in google sheets" width="100%" %}

- The text should separate into a new column automatically:

{% include figure.html img="/prep/transcript5.png" caption="Separated Text" alt="a screenshot of pasting text in google sheets" width="100%" %}


{:.pt-4 .mt-4 #errors}
***

## Check for Errors

- There is likely to be some text that accidentally got separated out to extra columns. To easily find this, select the entire spreadsheet so it's highlighted in blue

- Click on `Format` > `Text wrapping` > `Clip`

{% include figure.html img="/prep/transcript6.png" caption="Format > Text wrapping > Clip" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Now you can see text that should be in the `words` column:

{% include figure.html img="/prep/transcript7.png" caption="Rogue Text" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Copy and paste this text back into the appropriate `words` cells (you'll likely need to refer back to the Google Doc version of the transcript to verify that you're putting it in the right place)

- When this text is cleaned up, change the formatting to "Wrap" by selecting the entire spreadsheet again and clicking `Format` > `Text wrapping` > `Wrap`.

- Expand column C (the `words` column) so you can comfortably read the text. Your transcript should now look something like this:

{% include figure.html img="/prep/transcript8.png" caption="Transcript" alt="a screenshot of pasting text in google sheets" width="100%" %}

{:.pt-4 .mt-4 #read}
***

## Read Your Transcript

Now you'll need to read through your interview with three goals:

1. Correcting typos
2. [Separating big blurbs of text into smaller chunks](#text)
3. [Locating timestamps](#time)

{:.pt-3 #text}
### Separating Text

- If you encounter an especially large cell of text, you can create a new row below that cell and separate the text into two parts

- To separate a cell like this:

{% include figure.html img="/prep/transcript10.png" caption="Large Cell of Text" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Select the row so it's highlighted in blue

- Click on that row with two fingers, and select `Insert 1 below`

{% include figure.html img="/prep/transcript11.png" caption="Insert 1 below" alt="a screenshot of pasting text in google sheets" width="100%" %}

- Insert the speaker's initials into the `speaker` cell

- Select and copy half the text from the `words` cell, and paste it below into the cell you just created (make sure to also delete your selection from its original cell)

- Finished, your split should look like this:

{% include figure.html img="/prep/transcript12.png" caption="Text Split Between Two Rows" alt="a screenshot of pasting text in google sheets" width="100%" %}

{:.pt-3 #text}
### Locating and Moving Timestamps

- Timestamps are located periodically throughout the interview at the end of the text in the `words` cells:

{% include figure.html img="/prep/transcript13.png" caption="Timestamps" alt="a screenshot of pasting text in google sheets" width="100%" %}

- These need to be moved to the `timestamp` column

- When you come across a timestamp:

    - Copy and paste it into that row's `timestamp` cell

    - Replace the parentheses (`()`) with brackets (`[]`)

    - Put it into the format `[HH:MM:SS]` where `H` = hour, `M` = minute, and `S` = second

        - **Example:** `(7:55)` should become `[00:07:55]`

{% include figure.html img="/prep/transcript14.png" caption="Formatted Timestamps" alt="a screenshot of pasting text in google sheets" width="100%" %}

{:.pt-4 .mt-4 #name}
***

## Name Your Transcript

- Name your transcript spreadsheet using the following format: `lastnamefirstname` (all lowercase) (example: `bergmannroger`)

- If the interviewee has elected not to use his or her whole last name, use the first initial of their last name in place of their last name: `initialfirstname` (example: `broger`)

- If the interviewee has elected not to use his or her last name at all, simply title the transcript with their firstname: `firstname` (example: `roger`)