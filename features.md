---
layout: page
title: Features
permalink: /features/
layout: single
---

Prosop is a workflow to collect and aggregate information about historical individuals.  The tool is meant to preserve such information in its native format, without any fixed category requirements.  It will then find connections within a very large pool of demographic data, and allow aggregate analysis.  

Prosop is intended to help three kinds of users:

* microhistorians who have completed research projects and want to preserve their data,
* microhistorians doing new work, who want to collect material in a format more useable than a word processor document or spreadsheet, and
* family historians, who are currently doing tremendous “crowd-sourcing” style work with primary documents, work that is being captured by for-profit sites but passed over by professional historians.

At this point, the workflow involves four steps:

1. Gathering - a social undertaking
2. Cleaning and Structuring - using [OpenRefine](http://openrefine.org/)
3. Importing and Linking - using [Stardog](http://stardog.com/)
4. Querying - using [SPARQL](http://www.w3.org/TR/rdf-sparql-query/)

The next step on the horizon is ontology editing, using [Protege](http://protege.stanford.edu/).

The building block of Prosop is the "person page": a collection of information about a single individual (such as name(s), dates, locations, and relationships) who appears in a historical record.  This information is recorded using the categories and language of the original source.  Prosop then finds connections between this individual and other historical individuals in its database, including those described using different categories and languages.  For example, a record describing a baker named Giovanni residing in Livorno might be connected with a different record describing John Baker of Leghorn. 

### Adding names
Users can upload their own databases (using a wizard), or enter information directly (using a web-based form).  Every item of information is attributed to its contributor, and edits can be tracked using a wiki-style history.  Every item is also linked to the original source where it can be found.  Although Prosop has a strong preference for open information, users can control access to various parts of the data they submit.

### Categories
One of Prosop's distinctive features is its tolerance of flexible categories (or fields).  Unlike with traditional databases, Prosop users are not bound by fixed categories when recording information about historical individuals.  Users can define, redefine, and even hypothesise the categories of their description.  For a technical description of the database structure, see here.

### Networks
Prosop situates the individuals populating its database in networks, according to categories that users define.  So, for example, users want a map of inhabitants of a particular city at a particular time can choose to define inhabitation as any and all of residence, birth, employment, tenancy, or anything else.  Genealogical and corporate networks are similarly flexible, and other forms of networking can be produced.

### Languages
Prosop is designed to work equally well in any language.  Users define the terms and language of the data they submit.  Initially, the interface will be stocked with the languages of the Mediterranean, but users can add new languages as they please.