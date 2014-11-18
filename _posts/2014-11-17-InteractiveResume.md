---
layout: post
title: Some fun with JQuery &#58; Lists &amp; Links
---
###Inspiration
My afternoon project for last Friday happened to be my first ever endeavor
into JQuery, and among my first uses of Javascript. Since seeing the elegant
use of collapsing/expanding lists for the 
<a href="http://knowitall.cs.washington.edu/summa/demo.html">demonstration of a
news summarization system</a>, I had fallen in love with this strategy for
representing hierarchical data (in Summa's case, increasingly specific 
summarizations). At the same time, I was looking for a way to augment 
<a href="/resume/">my resume page</a>; a way to add more information without 
cluttering the page. Eventually hit upon the idea of combining these two ideas.

A single page resume is nice, but somewhat negates the point of creating a 
webpage&mdash;why not just post the .pdf (which <a href="/resume/resume.pdf">
I also do</a>), if it's not going to add anything else? My resume is one page 
of things <i>I</i> think will be most relevant to a position I am interested 
in. During a recent chat with a recruiter, I realized that the skills I chose 
not to include may be important, too. In this case, my training the Linux/Unix
systems, which has been pushed off my resume in favor of an NLP/Machine
Learning focus, was just the ticket to show that I had the skills the job 
required. My goal with my online resume, then, was to highlight certain things
&mdash;particularly recent projects and things I'm most proud of&mdash;
while allowing for further exploration and delving into everything I have to 
offer.

###Selectively Collapsing Lists
Creating collapsing/expanding lists was mostly a matter of following 
<a href="http://jasalguero.com/ledld/development/web/expandable-list/">
jasalguero's tutorial</a>, which works quite admirably. However, the page 
created by this tutorial loads with all lists collapsed. The "expand all" and 
"collapse all" buttons provide a detailed view and sparse overview, 
respectively. I wanted something in the middle, a "one page summary" by 
default, which could then be expanded or collapsed at will. 

To do this, I added a class that I could use to manually mark highlights, or
things that would be expanded by default. Since the page doesn't include any
content that might change, it creates lists of "highlights" and "lowlights" 
(everything but highlights) on loading. Collapsed style is then added to every
element of lowlights, and both collapsed and expanded styles are added to 
highlights. This allows highlights to maintain proper behavior when expanding
is toggled. Full code for this can be found in 
<a href="https://github.com/konahart/resume/blob/gh-pages/js/collapseList.js">
my resume repo</a>. 

###Differing Behavior for Anchor (fragment) and Outgoing Links
Because of the way click events are handled by the above tutorial, they must be
explicitly re-enabled in the script (which, to jasalguero's credit, is 
explained in the tutorial). However, solution provided would cause anchor links
to open in a new window/tab without actually focusing the page to the anchor. 
What I needed was to specify one behavior for anchor links and one behavior for
outgoing links. Although I saw plenty of similar questions online, I did not 
see any answers that fit my specific case. Since I wasn't able to find a clear
answer anywhere, here is my solution (minus aspects needed for 
collapsing/expanding elements):

{% highlight javascript %}
$('a').unbind('click').click(function(){
    var link = $(this).attr('href');
    var fragment = link.split('#')[1];
    if ( fragment ) {
        fragment = $('[name="' + link.substr(1) + '"]');
        $( root ).animate({
            scrollTop: $( fragment ).offset().top
        }, 500);
    } else {
        window.open( link );
    }
    return false;
});
{% endhighlight %}

Someone with better knowledge of JQuery might be able to produce a more 
elegant solution, but this seems to work.  
