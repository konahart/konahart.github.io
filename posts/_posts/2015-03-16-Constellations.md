---
layout: post
title: User Interface Design for Creative Writing Software
---

## Inspiration

### The State of Creative Writing Software

For whatever reason, I can never stop thinking about creative writing software
(you might be familiar with my 
[promptbot project](http://konahart.com/promptbot/)). 
Maybe it's a form of procrastination---I'm forever fidgetting with the 
software, never actually doing the writing. I have tried a number of different
programs, from [WriteItNow](http://www.ravensheadservices.com/index.php) back 
in the day, to [Scrivener](http://www.literatureandlatte.com/scrivener.php), 
to [Writer's Cafe](http://www.writerscafe.co.uk/), 
to [yWriter](http://www.spacejock.com/yWriter5.html), to just about every 
[alternative to Scrivener](http://alternativeto.net/software/scrivener/). 
While many of them are serviceable, most are little more than pared-down word
processors, glorified corkboards, or flow chart makers, and very rarely more 
than one or two of those. Worst of all---to me---all I've seen have the 
clunkiest, ripped-out-of-the-90s user interfaces. Few take advantage of more
recent forms of knowledge organization, such as tagging, nor new forms of
interaction such as touch. None look like they were natively written for 
post-millenial operating systems and devices; to my knowledge, none of them 
were. 

Which is not, in any way, to imply they are totally useless. Certainly word 
processors, corkboards, and flow charts are useful in creative writing.
However, I have found them limiting and wanting. Of the programs I have tried,
I prefer Scrivener because I find it the most richly-featured, but still feel 
constricted by its limited ways of interacting with my writing and its 
antiquated-looking interface.

## Design

### Borrowing from Coders --- Code Bubbles 

It was during my last term as a student, that my Human-Computer Interaction 
seminar discussed 
[Code Bubbles](http://www.andrewbragdon.com/codebubbles_site.asp). My
thoughts immediately turned to how I could apply those design decisions to 
creative writing software. At first I decided that there was not much that
would translate usefully; however, the idea kept churning in my brain. 

On the surface, the needs of writing creatively are very different from those
of writing software. Where an IDE might reasonably include things like tab-
completion and templating, these features are of very limited use to creative
writing. However, both acts center around both creating content and organizing
it. A large codebase can quickly get out of hand if there is no way to usefully
understand its structure; likewise, an author can get lost in all the details
of a story they are trying to create. When does a particular item or character
first appear in the story? Is its appearance described consistently? 

The "novel user interface metaphor" developed by Code Bubbles can be usefully
extended to the realm of creative writing. *More on this later.* 
 
Take-aways / novel features of Code Bubbles:

* Manipulate snippets
* Concurrently-visible working sets
* Groups with minimal border decoration, no overlap
* Large, pannable 2-D virtual space in which to cluster groups
* Small representation (map) of larger virtual space for easy navigation

### Interface Metaphor

Essential to good design is an intuitive metaphor---or model---of how
elements are organized and can be manipulated. Code Bubbles introduced 
"bubbles," but even this is not so much a comprehensive metaphor that fully
explans the bubbles' fuctionality, but mostly serves to emphasize that bubbles
fuction differenty from more-familiar "windows." 

Returning to existing creative writing software, many have the same component 
elements: 

* hierarchical file system on one side
* word processor in the middle
* meta-notes on the side
* short notes that are rearrangable within a grid 

The first two are probably familiar to the user by dint of being related to 
basic computational tasks. There is no particular metaphor in place that
relates these elements with the others; nor, necessarily, does there need to 
be.

The most novel element is the occasional inclusion of small notes that are 
rearrangable in a grid. These are always akin to index cards, a simple analogy
to the physical world: to add meta-notes to a document in the real world, one
might reasonably attach a Post-It note or an index card; the same metaphor is
reused for the digital world. But within that analogy, there is actually a 
loss of usefulness: index cards in the real world can be arranged in more
than just a grid. They can be manipulated in more meaningful ways. They can
be color-coded with multiple colors. They might also take the form of images,
whether a quick sketch, a photograph, or other useful bit of visual
information. In the real world, an author will use whatever material best suits
the information to be conveyed. The only limitations are related to being 
physical: portability, duplication, and so on. Unfortunately, this model 
consistently fails to solve some of those very problems. They fail to make use
of the advantages of using a computer program instead of actual notecards. 

Furthermore, the model these programs adopt is minimally commital, with only
one or two components being related to the real world, while the rest are 
unrelated to one another. The model gives no clear idea of the functionality
of its components. 

Instead, I propose a program with a model based around the night sky. 

Just looking at the night sky, you might see a mess of little lights: 
stars, planets, various celestial bodies. These lights (we'll say stars for 
simplicity) have no immediately apparent organizational structure. How can one
ever learn to consistently identify specific stars, transform the mess of 
lights into useful information? 

The solution to this problem is ancient, yet still applicable to modern life:
constellations.

By connecting and making pictures out of patterns of lights, humans have been
able to chart the night sky in ways that are memorable and meaningful to even
those with only passing interest in the celestial bodies. Furthermore, stars
can be part of multiple, overlapping constellations---being a member of one 
grouping does not prevent it from being part of another.

How does this map to creative writing?

Imagine a story that involves multiple narrator characters. One way to look at
the story is how it will appear in the story's final, written form: a series of
events, perhaps presented non-chronologically, from a variety of narrators. 
But perhaps, as the author creates the story, they want to look at the story
as it happens chronologically. Or perhaps they want to examine each character's
part as separate from the others'. Or perhaps the writer wants to group scenes
by their locations. All of these are perfectly valid ways to organize the same
set of documents, yet in most creative writing software, attempting to create
a new organization either destroys what existed previously or creates a lot of
needless duplication.

Therefore, I propose software that, like Code Bubbles, allows for snippets of
writing to be intuitively grouped, but unlike Code Bubbles, allows for 
multiple, overlapping organization schemes. The night sky model provides an
intuitive interface metaphor that will encourage ease of understanding and use.

Terminology:

* Stars - notes/nodes/vertices
* Clusters - multiple stars collapsed into a smaller representation
* Constellations - arrangements/relationships/networks

## Components

### Stars

Stars function much like you would expect notes to, but can actually have a 
range of uses. A Star might consist of:

* a snippet of writing
* a character profile
* a scene
* notes about a scene
* a setting
* an image
* a quote
* an event
* a link
* a piece of audio or video

### Constellations

Constellations operate much like Code Bubbles' bubbles, but multiple can be
defined from the same set of Stars. Grouping will be available both in terms of
an outline that encompasses the component Stars, as in the graphical 
representation of a constellation in real like, and in network-like edges 
between Stars (nodes). This can be used to create series of events, as in a
chronological or diegetic order, while having simultaneously associated but 
"orderless" elements.

Constellations will be given names and colors, to allow them to be easily
distinguished from one another in a selection menu.

### Clusters

For simplicity, it is advisable that groups of Stars be collapsible. For
example, a group of Stars might consist of notes related to a character---
perhaps one Star is a profile, others are images of the character, and so on. 
Perhaps the author wants to include all the character notes in a Constellation
that contains notes on all the characters. Including all the notes on this 
character at the "top level" in this Constellation would make it 
difficult to understand the relationship between all the Stars---notes on this
character are not directly related to notes on another character. Instead,
these Stars should be embeddable into a Cluster that represents the character.
Then is is possible to have a Constellation of all the characters, from which
each Cluster can be expanded into its component Stars.

### Other features

* small 'sky map' of all inhabited parts of the virtual field
* search across all snippets
* name/character generator
* document statistics (word counts, etc)
* selection of sky/star themed backgrounds will help give the software a modern
look
* bare-bones editor mode for focused, long-form writing

## Miscellanea

Working titles for this software design include:

* Constellate / Constellations
* Celestial
* Sky Writer
* Written in the Stars

