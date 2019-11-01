---
title: 2 - Code
nav: true
---
{% assign filters = site.data.filters | sort: "shortfilter" %}
{% assign conversation = site.data.conversation-filters | sort: "tag" %}

# Code Your Transcript

Read through your transcript and code cells by entering words from our controlled vocabulary into the "tags" column, right next to the cell you want those tags to describe.

### Tags:
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


### Here's an example:

{% include figure.html img="/code/codesample1.png" caption="Sample Coded Spreadsheet" alt="a screenshot of a transcript coded in google sheets" width="100%" %}

## Conversations

Keep track of snippets of text that you think might fit into existing conversations, or might be used to create new conversations. Current conversation questions are listed below. 

{:.alert .alert-danger .text-center .mx-5}
**Don't** tag your transcript spreadsheets using the conversation tags. Follow these steps instead:

When you find some text you think might fit, copy it and paste it into this spreadsheet: [Potential Conversation Content](). 

{% capture convo-field %}
- firstname
- lastname
- comments
- tag
{% endcapture %}

{% include bootstrap/card.md header="Be sure to fill in the following fields:" text=convo-field %}

{:.py-4 .mt-4}
***

### Conversation Tags:

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


**Rules for Entering Tags:**
- For consistency, keep tags lowercase
- Multi-word tags must be hyphenated (`data-sequencing`)
- To insert multiple tags, include a semi-colon between each tag with no spaces (`data-sequencing;genetics`)

