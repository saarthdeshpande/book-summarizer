# Book-Summarizer
<b>NLP-based</b> book summarizer which summarises the book chapter-wise.

Why summarise a book?
<ul>
<li>The goal of writing a summary of an article, a single chapter or a whole book is to offer as accurately as possible the full sense of the original, but in a more condensed form. 
<li>A summary restates the author's main point, purpose, intent and supporting details in your own words.
</ul>

How the summarizer works?
<ul>
<li>The summarizer is developed using <i><b>T5-small</b></i> pretrained model from <b>HuggingFace Transformers</b>.</li>
<li>Chunks are created from individual chapters.</li> 
<li>Then the chunks are tokenized using <i><b>T5Tokenizer</b></i>.</li>
<li>The tokenized text is passed to <b><i>T5ForConditionalGeneration</i></b> model class, for summary-ids generation.</li> 
<li>The summary-ids are decoded to text using <i>decode()<i> function from the <i><b>T5Tokenizer</b></i>.</li>
</ul>

How to run the Flask app :
<ol>
<li>Clone the repository.</li>
<li>Install all the dependencies mentioned in the <b>requirements.txt</b></li>
<li>Run <b>views.py</b> </li>
</ol>
