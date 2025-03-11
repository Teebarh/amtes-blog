---
title: "[Guest Post] Testing"
date: "2025-03-08T22:17:19+01:00"
authors:
  - "abdul-hameed"
  - "togba"
  - "toyibat"
  - "ileri"
showAuthorBottom: true
draft: false
layout: 
header: true  # centered | default single
modified: 
enableComments: true
font: GeistMono
replyByEmail: true 
---

{{< fullwidth src="image.jpg" alt="A Nice Beetle Car" >}}

## Default Body

This is some content inside this page. I want to learn to write and not stop writing. But writing is hard for me because I can't really think of

Okay wait, how exactly does this font look? I think it's similar to pretendard, in that in gives that cool modern sleek vibe

## RougeScript

{{< script >}}
**2024-03-10**  

Dear Friends,

I think I love this so much. You literally feel like you're going from one dimension and feeling to another! It's amazing

{{< /script >}}

## RUBIK

I think Rubik looks kinda nice, but I don't really feel the vibe right now. I mean it was nice when I used it previously for the heading (and maybe I could keep that use case), but for some reason headings don't seem to be working with the markdown inline style feature.
{.Rubik}

## Jost

I think Jost is like the really classy one amongst them, and I can't think of any direct writing type to use it for, but I would assume something that gives off the informal yet classy vibe. Similar to Outfit, but better.
{.Jost .text-lg}

## TT2020E

I think I really like this font. It gives off the typewriter/letter kinda vibe. Y'know those detective documents for example or something along those lines. Could be useful for those who want to engage in some creative writing.
{.TT2020E}

## Baskervville

Let's see what this looks like.  
Apparently, it's said to be best  
for poetry  
{.Baskervville .text-lg}

and it exudes that classic vibe  
I don't know  
{.Baskervville .text-lg}

That's what they said
{.Baskervville .text-lg}

## Shortcodes

### Blockquote

{{< blockquote 
  quote="How much do you want to know about the working conditions at every stage of the supply chain? How much are you morally obligated to know, with what consequences? Few of us would likely condone every moment of every supply chain for every product we consume. Yet to fully ethically withdraw from that participation would involve a renunciation of modern life." 
  author="Professor David Mindell, author, most recently, of “The New Lunar Society: An Enlightenment Guide to the Next Industrial Revolution”" 
  link="https://mitpress.mit.edu/books/new-lunar-society" 
  linkText="Full story via the MIT Press Reader"
  >}}

### Pullquote

{{< pullquote >}}
Hello World. This is some content in here!  

Or maybe it needs to be like a really long quote so that the thingies can then show up or something.  

“In an alternative grading system, grades are directly tied to what stu­dents actually learn, and reassessments make those grades more accurate. So when you see higher grades, it means more learning. That’s not “inflation”; it’s real growth.” (p. 59)
{{< /pullquote >}}

### Syntax Highlighting

```go {linenos=inline hl_lines=[3,"6-8"] style=github}
package main

import "fmt"

func main() {
    for i := 0; i < 3; i++ {
        fmt.Println("Value of i:", i)
    }
}
```