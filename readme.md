# Wiki'ed ('wikified' / 'wicked')

## What it is
A single page(-application) that either contains the functionality and the data of a wiki-editor. Just by saving the page the whole wiki-editor can be backuped and/or shared in a whole.

## How to use
Take the generated 'wikied.html' in 'dist/' and open it in your browser, that's it. More information can be found in the wiki-editor itself.

## Can i share my wiki page?
Sure, feel free to share it as you like.



# Development
## Installation
Get your copy of the source code by cloning this project. After that switch into the project folder and execute
```
npm run i
```
to install all needed packages.

## Developing
With
```
npm run watch
```
you invoke a watcher that will monitor the code and rebuilds the 'dist/wikied.html' at code change.

## CCSS
Inside in the code you'll find some special CSS, which is a bit like indented SASS, but with less features (no vars, no extend, no loops/if/else, etc.), just the more compact writing.

To create such CSS you'll have to meet these conditions:
- use a &lt;TEMPLATE&gt;-tag with the attribute ```lang=[ccss]```
- inside the template you have to write your CCSS-code
  - No curly brackets, the indention will define when a rule starts, ends and what belongs to a rule
  - No semicolon at the end of properties
  - Always have a space after the colon of a property, like ```color: red``` (but not: ```color:red```)
  - Rules can be nested. To reference a parent selector, use '&' as placeholder it will be replaced by the current parent selector (note: it will be the selector with not spaces around)
  - You can write one-line rules if it is just a selector and one property, use ```[SELECTOR] >> [PROPERTY]``` to do so, example ```.mySelector >> color: red```
