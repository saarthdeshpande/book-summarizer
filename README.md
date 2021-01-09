# Book-Summarizer
<b>NLP-based</b> book summarizer which summarises the book chapter-wise.<br>
In case the book does not contain chapters: the entire book is summarized.

Why summarize a book?
<ul>
<li>The goal of writing a summary of an article, a single chapter or a whole book is to offer as accurately as possible the full sense of the original, but in a more condensed form. 
<li>A summary restates the author's main point, purpose, intent and supporting details in your own words.
</ul>

How does the summarizer work?
<ul>
<li>The summarizer is developed using <i><b>T5-small</b></i> pretrained model from <b>HuggingFace Transformers</b>.</li>
<li>Chunks are created from individual chapters.</li> 
<li>Then the chunks are tokenized using <i><b>T5Tokenizer</b></i>.</li>
<li>The tokenized text is passed to <b><i>T5ForConditionalGeneration</i></b> model class, for summary-ids generation.</li> 
<li>The summary-ids are decoded to text using <i>decode()<i> function from the <i><b>T5Tokenizer</b></i>.</li>
</ul>

How to run the book summarizer:
<ol>
<li>Clone the repository.</li>
  
```
git clone https://github.com/saarthdeshpande/book-summarizer.git
```

<li>Install all the dependencies mentioned in the <b>requirements.txt</b>.</li>

```
pip install -r requirements.txt
```
<li>To run via CLI:</li>

```
python3 bsCLI.py --path <path-to-PDF-file>
```
<li>To run on Flask server with frontend and mail:
    <ol>
        <li>Update the value of <b>sender_address</b> and <b>sender_pass</b> in <b>mail.py</b>.</li>
        <li>Run <b>views.py</b>.</li>

```
python3 views.py
```
</ol>
</li>


</ol>

**Screenshots**

<p align="center">
  <b>Home Page</b><br><br>
  <img width="640" height="480" src="https://github.com/saarthdeshpande/book-summarizer/blob/master/screenshots/homepage.png">
</p>

<p align="center">
  <b>Mail on Successful Processing</b><br><br>
  <img width="640" height="480" src="https://github.com/saarthdeshpande/book-summarizer/blob/master/screenshots/mail.png">
</p>
