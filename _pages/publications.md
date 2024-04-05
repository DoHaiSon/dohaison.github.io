---
layout: page
permalink: /publications/
title: Publications
description: 
nav: true
nav_order: 1
sortby: true        # true: Sort by types | false: Sort by years
years: [2024, 2023, 2022, 2021, 2020, 2019]
sections:
  - bibquery: "@preprint"
    text: "Preprint articles"
  - bibquery: "@article"
    text: "Journal articles"
  - bibquery: "@book|@incollection"
    text: "Books and Book chapters"
  - bibquery: "@inproceedings"
    text: "Conference and Workshop articles"
  - bibquery: "@misc|@thesis"
    text: "Thesis"
---
<!-- _pages/publications.md -->
<div class="publications">
    <a href="https://scholar.google.com/citations?user=8LqmCjAAAAAJ"><b>Google Scholar Profile</b></a>
    <p></p>

{%- if page.sortby -%}
    {%- for section in page.sections %}
        <a id="{{section.text}}"></a>
        <p class="bibtitle">{{section.text}}</p>
        {%- for y in page.years %}

            {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
            {%- capture citecount -%}
            {%- bibliography_count -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] -%}
            {%- endcapture -%}

            {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
            {%- if citecount !="0" %}

            {% bibliography -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] %}

            {%- endif -%}

        {%- endfor %}

    {%- endfor %}

{%- else -%}

    {% bibliography -f {{ site.scholar.bibliography }} %}

{%- endif -%}

<p style="border-top: 1px solid #2698BA; padding-top: 1em"></p>
<p>Nat. Ws : National Workshop article / poster</p>
<p>Nat. Conf. : National Conference article / poster</p>
<p>Nat. Jour. : National Journal article</p>
<p>Int. Ws : International Workshop article / poster</p>
<p>Int. Conf. : International Conference article / poster</p>
<p>Int. Jour. : International Journal article</p>

</div>