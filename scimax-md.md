
# Table of Contents

1.  [Headings](#org0520e68)
    1.  [subheading](#orgf0a045c)
        1.  [subsubheading](#org9143a2a)
2.  [Markups](#org2d3e1d8)
3.  [Lists](#org18b0d3b)
    1.  [Numbered lists](#orgd6fdc55)
    2.  [plain lists](#orgecd6087)
    3.  [checklists](#orgfc3d5f6)
    4.  [definition lists](#org5917637)
4.  [Equations](#orge474a75)
5.  [Code blocks](#org7031988)
6.  [Tables](#org7c0f358)
7.  [Citations  label:sec-citations](#org289b18c)
8.  [Radio targets](#org67d1cb1)
9.  [Cross-references](#orge2623dc)
10. [needed](#orgb75370c)
11. [Exporting](#org4585e16)

Why? Don't we already have org-mode? Yes, but some places like Markdown, it is no fun to write when you have really technical documents, and it would be harder to get markdown-mode to be as good as org-mode than to do this.


<a id="org0520e68"></a>

# Headings

It goes without saying I hope.


<a id="orgf0a045c"></a>

## subheading


<a id="org9143a2a"></a>

### subsubheading

Anything deeper than this gets turned into paragraphs by default.


<a id="org2d3e1d8"></a>

# Markups

**bold** *italics* <span class="underline">underline</span> <del>strike</del> `verbatim` `code`

subscripts: H<sub>2</sub>O

superscripts: H<sup>+</sup>


<a id="org18b0d3b"></a>

# Lists


<a id="orgd6fdc55"></a>

## Numbered lists

1.  one
2.  two
3.  three

Note these letters will render as numbers.

1.  apple
2.  bear
3.  cat


<a id="orgecd6087"></a>

## plain lists

-   one
-   two
-   three
    -   with nesting
        -   deeper
    -   back in
-   all the way


<a id="orgfc3d5f6"></a>

## checklists

-   [ ] one
-   [ ] two
-   [ ] three


<a id="org5917637"></a>

## definition lists

-   **org-mode:** what makes this possible
-   **emacs:** the other thing you need


<a id="orge474a75"></a>

# Equations

Suppose you have this equation to solve:

<a name="eq-sle"></a>

\begin{equation}
8 = x - 4
\end{equation}

    print(f'x = {8 + 4}')

    x = 12

The results above show the answer to [eq-sle](#eq-sle).


<a id="org7031988"></a>

# Code blocks

    %matplotlib inline
    import matplotlib.pyplot as plt

    plt.plot([1, 2, 4, 8])

    [<matplotlib.lines.Line2D at 0x10c6d34e0>]

![img](obipy-resources/0a58dae9b8af7857c4824224987cae2f-18961DFU.png)

You might like a caption.

./obipy-resources/0a58dae9b8af7857c4824224987cae2f-18961DFU.png


<a id="org7c0f358"></a>

# Tables

You can have tables, with captions and labels.

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 1:</span> A data table. <a name="tab-data"></a></caption>

<colgroup>
<col  class="org-right" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">x</th>
<th scope="col" class="org-right">y</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">1</td>
<td class="org-right">1</td>
</tr>


<tr>
<td class="org-right">2</td>
<td class="org-right">4</td>
</tr>


<tr>
<td class="org-right">3</td>
<td class="org-right">9</td>
</tr>


<tr>
<td class="org-right">4</td>
<td class="org-right">16</td>
</tr>
</tbody>
</table>


<a id="org289b18c"></a>

# Citations  <a name="sec-citations"></a>

You can have proper scientific citations like this <sup>[kitchin-2015-examp](#kitchin-2015-examp)</sup>, including multiple references <sup>[kitchin-2015-data-surfac-scien](#kitchin-2015-data-surfac-scien)</sup><sup>,</sup><sup>[kitchin-2015-examp](#kitchin-2015-examp)</sup><sup>,</sup><sup>[kitchin-2016-autom-data](#kitchin-2016-autom-data)</sup>.


<a id="org67d1cb1"></a>

# Radio targets

In org-mode you can define a <a name="target"></a>target that you can make a link to later.


<a id="orge2623dc"></a>

# Cross-references

Remember in Table [tab-data](#tab-data)?  How about [eq-sle](#eq-sle)? Or that figure we put a caption on (Fig.  [fig-data](#fig-data)).

How about section [sec-citations](#sec-citations) on citations?

Remember the [target](#target) we referred to earlier?


<a id="orgb75370c"></a>

# TODO needed

-   [ ] fix eqref in md export in org-ref
-   [ ] redo how labels are done. Should they be visible?


<a id="org4585e16"></a>

# Exporting

    (require 'scimax-md)

    scimax-md

To a buffer:

    (pop-to-buffer (org-export-to-buffer 'scimax-md "*scimax-md-export*"))

    #<buffer *scimax-md-export*>

    (org-export-to-file 'scimax-md "scimax-md.md")

    scimax-md.md

# Bibliography
<a id="kitchin-2015-examp">kitchin-2015-examp</a>: Kitchin, Examples of Effective Data Sharing in Scientific Publishing, <i>{ACS Catalysis}</i>, <b>5(6)</b>, 3894-3899 (2015). <a href=" http://dx.doi.org/10.1021/acscatal.5b00538 ">link</a>. <a href="http://dx.doi.org/10.1021/acscatal.5b00538">doi</a>.

<a id="kitchin-2015-data-surfac-scien">kitchin-2015-data-surfac-scien</a>: "John Kitchin", Data Sharing in Surface Science, <i>"Surface Science "</i>, <b>647()</b>, 103-107 (2016). <a href="http://www.sciencedirect.com/science/article/pii/S0039602815001326">link</a>. <a href="http://dx.doi.org/10.1016/j.susc.2015.05.007">doi</a>.

<a id="kitchin-2016-autom-data">kitchin-2016-autom-data</a>: "Kitchin, Van Gulick \& Zilinski, Automating Data Sharing Through Authoring Tools, <i>"International Journal on Digital Libraries"</i>, <b>18(2)</b>, 93--98 (2016). <a href="http://dx.doi.org/10.1007/s00799-016-0173-7">link</a>. <a href="http://dx.doi.org/10.1007/s00799-016-0173-7">doi</a>.