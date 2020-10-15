---
title: This is just a test
author: Max Mustermann
date: October 2020
abstract: A test is just a test. Nothing more. Nothing less.
bibliography: [references.bib]
linkReferences: true
link-citations: true
lang: en-GB
nameInLink: true
papersize: a4
colorlinks: true
links-as-notes: true
output:
  pdf_document:
    toc: true
    number_sections: true
  word_document:
    path: output.docx
    reference_doc: custom-reference.docx
    toc:
      depth_from: 1
      depth_to: 6
      ordered: true
---

# Introduction  {#sec:introduction label="Intro"}

The first valuable search result on using Makrdown in academic writing was this video tuorial [@durkop0006SettingScholarly2020]

At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat [@LoremIpsumAll].

# Will Images work?

![This is a black image](image.png){#fig:blackfigure}

<!-- @import "subsection.md" -->

# References {ignore=true}
