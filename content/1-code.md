---
title: 2 - Code
nav: true
---
{% assign filters = site.data.filters | sort: "shortfilter" %}
{% assign conversation = site.data.conversation-filters | sort: "tag" %}

# Code Your Transcript

At this point, you should have a transcript that's set up like this...

{% include figure.html img="/code/codesample2.png" caption="Sample Transcript CSV" alt="a screenshot of a transcript coded in google sheets" width="100%" %}

...with four columns labeled `timestamp`, `speaker`, `words`, and `tags`

Now it's time to start coding! Follow these steps:

- [Tag Your Transcript](#trans)
- [Identify Conversations](#conv)
- [Finish Up](#finish)

{:.pt-4 .mt-4 #trans}
***

## Transcript Tagging

1. Read through your transcript and tag cells with the preapproved tags in the table below. These tags should be entered into the `tags` column, in the same row as the text they're describing.

2. Keep tags lowercase (following format in the table below).

2. If you put multiple tags in one cell, **separate them with a semicolon (`;`)**. 

{:.pt-4}
### Tags
<table class="table table-striped border">
    <thead>
        <tr>
            <th scope="col">Tag (for use when coding):</th>
            <th scope="col">Description:</th>
        </tr>
    </thead>
    <tbody>
    {% for f in filters %}
        <tr>
            <td>{{ f.shortfilter }}</td>
            <td>{{ f.text }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>


{:.pt-4}
### Coded Spreadsheet

{:.pt-3}
Here's how your tagged spreadsheet should look:

{% include figure.html img="/code/codesample1.png" caption="Sample Coded Spreadsheet" alt="a screenshot of a transcript coded in google sheets" width="100%" %}

{:.pt-4 .mt-4 #conv}
***

## Curate Some Conversations

Keep track of snippets of text that you think might fit into [existing conversations](https://www.voicesofgayrodeo.com/).

{:.alert .alert-danger .text-center .mx-5}
Important: **Don't** tag your transcript spreadsheets using the conversation tags. Follow these steps instead:

1. When you find some text you think might fit in a conversation, copy it and paste it into this spreadsheet: [Master Conversations](https://docs.google.com/spreadsheets/d/1TZpHcIRAI9KzGUwtXteLvNrPm6QO5HiNzHyZ2S9gxmU/edit?usp=sharing). 

2. Insert your snippet of text into the `comments` column in the spreadsheet, and add the speaker's first name and last name to the row. Once this is done, tag your snippet of text with an appropriate tag selected from *Conversation Tags* table below.

{:.pt-4}

### Conversation Tags
<table class="table table-striped border">
    <thead>
        <tr>
            <th scope="col">Tag (for use when coding):</th>
            <th scope="col">Question:</th>
        </tr>
    </thead>
    <tbody>
    {% for c in conversation %}
        <tr>
            <td>{{ c.tag }}</td>
            <td>{{ c.question }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

{:.pt-4 .mt-4 #finish}
***

## Finishing Up

When your transcript is finished, notify Becca and she will check it for you. 

Once she approves it, you'll need to download the transcript to your computer as a **comma-separated file (CSV)**. Follow the steps below:

1. Click on `File` > `Download` > `Comma-separated values (.csv, current sheet)`.

2. **Don't** open the CSV. Make sure you know where it's located on your computer, then move to the next page for instructions on what to do next.

{% include figure.html img="/code/download.png" caption="Download Your Transcript as a CSV" alt="a screenshot of steps to download a google sheet as a csv" width="100%" %}

