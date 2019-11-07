---
title: 3 - Upload
nav: true
---

{% assign markdown = site.data.markdown %}

# Add Your Content to the Web

- [Create a GitHub Account](#github)
- [Upload Your Transcript](#upload)
- [Create a Markdown File](#bio)
- [Upload an Image](#image)
- [Check GitHub Pages](#pages)
- [Make Changes Live](#live)

{:.pt-4 .mt-4 #github}
***

## Create a GitHub Account

{:.alert .alert-warning .text-center .mx-5}
If you already have a GitHub account, skip this step.

1. Go to <https://github.com/>.

2. Create an account.

3. Check your email to verify your account.

{:.pt-4 .mt-4 #upload}
***

## Upload Your Transcript

Head over to the Voices of Gay Rodeo Development [GitHub Repository](https://github.com/thecdil/gayrodeo_dev). This is were all the source code for the Voices of Gay Rodeo website is stored. We'll use your GitHub username to make you a collaborator for this repository. 

The repository looks something like this:

{% include figure.html img="/upload/github1.png" caption="Voices of Gay Rodeo GitHub Repository" alt="a screenshot of the Voices of Gay Rodeo GitHub repository" width="100%" %}

Once you're a collaborator, you'll have the ability to upload and edit files in the repository.

{:.pt-4}

### How to Upload

{:.pt-3}

- Navigate to the `_data` folder (located at the top of the repository). Click on the `_data` folder.

- Inside the `_data` folder, you'll see another folder labeled `transcripts`. Click on the `transcripts` folder.

- Now you should see a list of transcript CSVs (see the screenshot below). Let's add yours.

- In the top right of your screen, locate and click on the button labeled `Upload files`. 

{% include figure.html img="/upload/github2.png" caption="'Upload files' button" alt="a screenshot of the repository's upload files button location" width="100%" %}

- Find your transcript CSV in your computer's File Explorer (PC) or Finder (Mac) and drag and drop it into the space that says "Drag files here."

- **"Commit"** your upload: In the text box near the bottom of the screen under "Commit changes," write a short message that describes what change you made. 

- When you're satisfied with your message, click on the green `Commit changes` button.

{% include figure.html img="/upload/github3.png" caption="Commit Your Upload" alt="a screenshot of the repository's commit entry box" width="100%" %}

- Your transcript has now been successfully uploaded.

{:.pt-4 .mt-4 #bio}
***

## Create a Markdown File

We need to create some biographical information for your interviewees so that their [interview](https://www.voicesofgayrodeo.com/interviews/bergmann.html){:target="_blank"} and [transcript](https://www.voicesofgayrodeo.com/interviews/transcripts/bergmann.html){:target="_blank"} pages have the appropriate context.

To do this, you'll be creating a [Markdown](https://www.markdowntutorial.com/){:target="_blank"} file. You don't need to know anything about Markdown other than what is discussed below.

There are two major steps you'll need to undertake in this section:
1. [Create a Markdown File in the `_interviews` Folder](#create)
2. [Copy Your Markdown File to the `_transcripts` Folder](#copy)

{:.pt-3 #create}
### Creating Your Markdown File in `_interviews`

- Starting back at the home page of the Voices of Gay Rodeo [GitHub Repository](https://github.com/thecdil/gayrodeo_dev){:target="_blank"}, click on the folder labeled `_interviews`.

- In the top right, click on the button labeled `Create new file`.

{% include figure.html img="/upload/github6.png" caption="Create new file" alt="a screenshot showing how to create a new file on GitHub" width="100%" %}

- Name your file the same name you gave your transcript (using the format `lastnamefirstname`). **End your file name using the extension `.md`** (this stands for Markdown).

{% include figure.html img="/upload/github5.png" caption="Name Your File" alt="a screenshot showing how to name a markdown file on GitHub" width="100%" %}

- Copy *all* of the following (including the hash marks (`---`)!) into the body of the file:

{:.card .card-body}
```
---
object-id: bergmannroger  
transcript: transcript-bergmannroger  
first-name: Roger
last-name: Bergmann
date-interviewed: November 19, 2016
location: Austin, Texas
interviewer: Rebecca Scofield
image: y
---
```

{:.pt-3}
- What you've just copied is called YAML front matter. The fields *before* the colons (`:`) are called **Variables**, and the entries after the colons are the **value** of each variable. 

- In order for your new pages to show up on the website, you need to **(1) delete the current values (everything to the right of the colons)**, and **(2) enter values that describe the interview you just uploaded**.
    - Follow the example values you copied into your document, or see the table below for more detail:

{:.pt-3}
### Formatting Your Markdown File
<table class="table table-striped border">
    <thead>
        <tr>
            <th scope="col">Variable:</th>
            <th scope="col">Format:</th>
            <th scope="col">Example:</th>
        </tr>
    </thead>
    <tbody>
    {% for m in markdown %}
        <tr>
            <td>{{ m.variable }}</td>
            <td>{{ m.format }}</td>
            <td>{{ m.example }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

{:.pt-3}
- Now you should have updated all the variables between the hash marks (`---`). The last step is to **add a biographical paragraph** about your interviewee underneath the second row of hash marks.

- When you're finished, your markdown file will look something like this:

{% include figure.html img="/upload/github4.png" caption="New Markdown File" alt="a screenshot of the a newly created Markdown file on GitHub" width="100%" %}

- Before committing this file, **copy** all of the text in the body of the file (you'll need it for the next section):

    1. Place your cursor anywhere in the file
    2. Select All: Press `ctrl` + `a` (on PC) or `cmd` + `a` (on Mac)
    3. Copy: Press `ctrl` + `c` (on PC) or `cmd` + `c` (on Mac)  
{:.pt-2}
- Scroll to the bottom of the page, enter a commit message, and press the green `Commit changes` button.

{% capture markdown %}
### Editing Your Markdown File

If you want to make an edit to your markdown file after committing, follow these steps:

{:.pt-3}
- Click on your markdown file 

{:.pt-1}
- Click on the pencil icon in the top right corner  

{:.pt-1}
- Make your new changes and commit them
{% include figure.html img="/upload/github7.png" caption="Editing Your Markdown File" alt="a screenshot showing how to edit a markdown file on GitHub" width="100%" %}
{% endcapture %}
{% include bootstrap/alert.md text=markdown color="warning" %}

{:.pt-3 #create}
### Copy Your Markdown File to `_transcripts`

- Starting back at the home page of the Repository, click on the folder labeled `_transcripts`.

- In the top right, click on the button labeled `Create new file`.

- Name your file the same name as the markdown file you just created in `_interviews` (Don't forget to add the extension `.md` to the end!).

- Paste the content from the markdown file you just created in `_interviews`:
    1. Place your cursor in the body of the file
    2. Paste: Press `ctrl` + `v` (on PC) or `cmd` + `v` (on Mac)
{:.pt-2}
- Scroll to the bottom of the page, enter a commit message, and press the green `Commit changes` button.


{:.pt-4 .mt-4 #image}
***

## Upload an Image

- Make sure the image you're uploading has the same file name as the transcript and markdown file you labeled earlier (`lastnamefirstname`). The image should have either a `.jpg` or `.png` extension.

- Find the `images` folder from the home page of the repository. Click on it.

- Inside the `images` folder, you'll find a folder labeled `people`. This is where all the images of interviewees are stored. Click into this folder.

- In the top right of the screen, find and click on the button labeled `Upload files`.

- Drag and drop your file into the repository. 

- Write a commit message, and click the green `Commit changes` button.

{:.pt-4 .mt-4 #pages}
***

## Check Your Upload Using GitHub Pages

- Wait a few minutes after your last commit for the repository to update.

- Follow this link: <https://thecdil.github.io/gayrodeo_dev/>{:target="_blank"} to see how the interview you added looks on the demo site.

{:.pt-4 .mt-4 #live}
***

## Make Your Changes Live

- When your interview is ready to be made live on the official [Voices of Gay Rodeo website](https://www.voicesofgayrodeo.com/){:target="_blank"}, email [Olivia Wikle](mailto:omwikle@uidaho.edu) and [Devin Becker](mailto:dbecker@uidaho.edu). Be sure to include the name of the interview you added in your email.