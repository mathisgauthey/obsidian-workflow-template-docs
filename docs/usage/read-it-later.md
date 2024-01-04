# Read-it-later and bookmark manager

## Why doing this ?

Every link you saved using Omnivore will be saved and synced as a markdown file in your vault.

It allows for easy search inside your knowledge base across your sources and notes. You can also link these notes during your write-ups.

## How to use it ?

This part is pretty simple. You simply need to connect your Omnivore account, add some pages to your inbox. It will then be synced to Obsidian inside the `_Sources` folder each time you use the Omnivore button on Obsidian left side bar or every 5 min.

## How is it configured ?

Front matter template :

```txt
id: {{{id}}}
title: >
  {{{title}}}
{{#author}}
author: >
  {{{author}}}
{{/author}}
{{#labels.length}}
tags:
{{#labels}} - {{{name}}}
{{/labels}}
{{/labels.length}}
state: {{{state}}}
date_published: {{{datePublished}}}
date_saved: {{{dateSaved}}}
date_read: {{{dateRead}}}
date_archived: {{#formatDate}}{{{dateArchived}}},"yyyy-MM-dd HH:mm:ss"{{/formatDate}}
```

Article template :

```txt
# {{{title}}}

#Omnivore

[Read on Omnivore]({{{omnivoreUrl}}})
[Read Original]({{{originalUrl}}})

{{#note}}
## Notes

{{{note}}}
{{/note}}

{{#highlights.length}}
## Highlights

{{#highlights}}
> {{{text}}} [⤴️]({{{highlightUrl}}}) {{#labels}} #{{name}} {{/labels}}
{{#note}}

{{{note}}}
{{/note}}

{{/highlights}}
{{/highlights.length}}
## Webpage

{{{content}}}
```
