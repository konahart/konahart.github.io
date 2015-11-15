---
layout: post
title: New NLP-ish Repo
---
Curious about what I worked on over the summer? Check out my
<a href="https://github.com/konahart/relation-extraction-pipeline">
new, elegantly-named repo</a>:
<a href="https://github.com/konahart/relation-extraction-pipeline">
https://github.com/konahart/relation-extraction-pipeline</a>

I decided to open source my work because a) my bosses had no problem with it
(<i>i.e.</i>, "because I can") and b) I believe there are parts which may be more
widely useful, such as:
<ul>
<li>GigawordCorpusHandler, which parses the XGML structure given by
<a href="https://www.ldc.upenn.edu/">LCD</a>'s
Gigaword Corpus (consistent across English, Spanish,
and Chinese); </li>
<li>CoreNLPProcessor, which uses
<a href="http://nlp.stanford.edu/software/corenlp.shtml">Stanford's CoreNLP </a>
to perform tokenization, NER, and POS annotation (although not the most
efficiently... more on that later); and </li>
<li>Utils, which provides a function to check whether a
file is gzipped, then returns the appropriate InputStream (useful for dealing
with large corpora like Gigaword, but not having to gzip all files).</li>
</ul>

In the coming months I'll likely work on breaking them out into their own,
useful little repos, but since the code runs, I might as well make it available
now. Enjoy!
