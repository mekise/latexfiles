<h1>latexfiles</h1>
<p>In this repo, you find some custom latex stuff I regularly use in my notes and papers.</p>

<h2>DOI link style</h2>
<p>To have the DOI link formatted as in the examples below, you need to add these lines before the <code>\begin{document}</code></p>
<pre><code>%%% redefine doi command to remove box around hyperlink ###
\let\oldbibitem\bibitem % copy bibitem into oldbibitem
\renewcommand{\bibitem}{
    \renewcommand{\doi}[1]{\texttt{\href{https://doi.org/##1}{doi:##1}}} % override \doi
    \let\bibitem\oldbibitem % restore \bibitem
    \oldbibitem % call old \bibitem
}</code></pre>

<h2>Bibliographystyle examples</h2>
<p>This is how the different styles look like:</p>
<ul>
  <li>unsrtnat_compact.bst (unsrt_compact.bst is the same but without DOI)<img src="https://raw.githubusercontent.com/mekise/latexfiles/main/bib_examples/unsrtnat_compact.png" alt="unsrtnat_compact_example"></li>
  <li>alphaurl_compact.bst<img src="https://raw.githubusercontent.com/mekise/latexfiles/main/bib_examples/alphaurl_compact.png" alt="alphaurl_compact_example"></li>
</ul>

<h2>How to write the references in the .bib file</h2>
<p>This is how you create the entries in the .bib file:</p>
<ul>
    <li>Published articles<ul>
        <li>Copy and paste the bib entry that you find on <a href="https://search.crossref.org/">https://search.crossref.org/</a>. Search by DOI, this is the quickest way to search on crossref</li>
        <li>Remove the url entry (the entire line)</li>
    </ul>
    </li>
    <li>arXiv preprints<ul>
        <li>Copy and paste the bib entry from the arXiv page</li>
        <li>Change from @misc to @article</li>
        <li>Add DOI field (you find the DOI on the arXiv page): doi = {10.xxxx/arXiv.xxxx.xxxxx}</li>
        <li>Add field journal: journal = {arXiv preprint}</li>
    </ul>
    </li>
</ul>
