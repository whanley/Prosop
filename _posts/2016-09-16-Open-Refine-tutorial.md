---
title: "OpenRefine introduction"
date: 2016-09-16
categories: openrefine tutorial
---
Here's a few rough notes from a rough tutorial to openrefine extraction of tabular data that I did for Sarah Craft's classics class at FSU.

[Powerpoint](https://docs.google.com/presentation/d/1GZJYc8-9RERSuIPIYoe5D7iWe8bqk3l5zXuHzcFg1fc/edit?usp=sharing)

# My examples

1. Indicateur Egyptien 1897: [Original](https://babel.hathitrust.org/cgi/pt?id=coo.31924007302890;view=1up;seq=5) and [tables](). I broke this material down into factoids, and could facet it by name and addresses.

2. Materials for an [Ottoman Gazetteer](https://github.com/whanley/Ottoman-Gazetteer/tree/master/data). These feature a very complex line structure, and were hard to turn into data tables.

# Your examples

## Late Fortresses in the Notitia

### Preprocessing
1. Copy text and paste into a word processor document.
1. Notice that you must trim the edges of the PDF, and do so using a PDF editor.
2. Notice that the last page of the PDF produced mismatched columns. Use Convert Text to Table function in the word processor, and move the last lines of the table into new columns following the appropriate rows.
3. Notice that there's still a problem: not every row of the table corresponds to a single record--some contain half records. To fix this, use Find and Replace with regular expressions: First, change Occ. to FSUOcc. and Or. to FSUOr. Then, then change $ (which indicates a line break) to space. Then, (using Regex) change FSU (which we added as a prefix to Occ. and Or.) to \n (which indicates a hard line break).
4. Now export this table as csv (or simply using the clipboard) and import it into OpenRefine.

### In OpenRefine
1. Split columns using spaces and commas.
1. Use GREL expressions:
to concatenate cells: `value + " " + cells["Command 1"].value`; to extract only the last word: `value.partition(smartSplit(value," ")[-1])[1]` More GREL recipes [here](https://github.com/OpenRefine/OpenRefine/wiki/GREL-String-Functions) and [here](https://github.com/OpenRefine/OpenRefine/wiki/GREL-Functions) and [here](https://github.com/OpenRefine/OpenRefine/wiki/GREL-Other-Functions).

## Other, more challenging examples

A geographic dictionary [like this one](https://catalog.hathitrust.org/Record/101713701) is interesting to parse. Unfortunately it's in Greek and Italian, and the Greek characters were not OCRed as Greek. Similar problems with the Arabic letters in this [Ottoman historical geography](https://babel.hathitrust.org/shcgi/pt?id=hvd.32044012720520;view=1up;seq=25).
