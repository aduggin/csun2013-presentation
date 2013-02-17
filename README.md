# Accessibility on the Olympics website

	TO DO:
	
	* Read my confluence accessibility pages
	* Read my blog article
	* Read support forum
	* Read emails to/from Henny and team
	* Read Read Bee reports
	* Read BBC Sport blog articles
	* Read CSUN emails
	
	* Record a video of the medal table

## Introduction to the product

### Scope of the Project

The most ambitious and comprehensive BBC digital project to date - 4 screen proposition - delivered to PC, tablet, Mobile and Connect TV

Grand vision - to deliver the first truly digital Olympics. Never miss a moment

Website built around the olympics domain - a page for every athlete, team, venue, sport and medal winning event.  Each with an index pages.

* 10, 000 Athlete
* 205 Countries
* 30 Venues
* 36 Sports
* 204 Medal Winning Events

Each of these pages displayed Facts and figures, latest news stories, image galleries, short form video clips, schedule, results and medals tables.

Other Page components including:
* Top Trump style comparison modules
* Twitter module
* Favourites Tray

Other sections and pages

* Interactive Video Player
	* 24 High definition live streams of content
	* 2500 hours of live coverage available on demand to all platforms
* Medals table
* Schedule and Results
* News Articles 

Over 100,000 pages in total

	@ACTION - ask Andy, Keith, Matt and Cait if they know how many desktop and mobile pages
	Most popular pages?
	An stats for medal table?
	
### Usage and Stats

We knew the website would be popular and receive a huge amour of traffic - don't think anyone expected the figure we got

	37 million UK browser - 66% UK online adult population
	57m global browser to bbc.co.uk
	111m video requests across all platforms
	
	7.4 million mobile browsers
	1.9m downloads of our Olympics smartphone app
	12m requests for video from mobile devices
	
	@ACTION: Ask Henny if we should mention no accessibility complains

## Accessibility at the BBC

The BBC has a duty to deliver big national events on behalf of the **whole population**.
 
Talk about

* Standards and Guidelines - Henny created a single document for all accessibility standards
* BBC Trust

Didn't want to repeat what happened to the Australian 2004 Olympics website.


## The challenges

Lots to build in a relatively short space of time

Immovable deadline

A 17 day event - huge traffic so code freeze during event

Dynamic website - don't get lots of the real data until the actual event

Design upfront with lots of javascript rich interactions

Lots of developers in lots of different teams
	London, Salford and external companies
	many new to BBC
	mixed knowledge of accessibility

BBC Standards and Guidelines not up to date - javascript, html5 and aria

No single good accessibility resource that shares best practices

Many best practices still not really established. Little or no empirical evidence - e.g what the best way to build a carousel.  There's a difference between making something technical accessible and intuitive/usable.


## The Development approach

Accessibility made a priority from above from the start

Thought about accessibility from the start

Spoke to experts early - Ian and Henny

Digest and circulate BBC standards and Guidelines

Organised training

* Screenreader training - JAWS/NVDA
* Accessibile web applications - javascript, aria and html5
	* Bespoke - used components that we were going to be building
	* Support forum

Trawl resources for accessibility knowledge and best practice

* blogs
* books
* web aim mailing list
* simply accessible q and a 
Wiki, Blog and Presentations to share round team / organisation

Set up a support network 

* Mentor new developers
* Set up an email list
* learning lunches - chance to review and discuss approaches

Review and feedback accessibility concerns early - to designers, developers and product owners

Agile methodology

* tackle features in priority order
* Push back on new features until core features complete - especially towards end of project

Let front-end developers concentrate on the front end - php developers concentrate on back end.

Library of elements and reusable components
* oocss - elements and common sub components. don't tie visuals to elements
* components that can be dropped into any page
* use static feeds so not dependant on real data
* reuse leads to consistency, easier to test and maintain and pages that become quicker /easier to put together
	
Progressive Enhancement. Only use aria an an extra if needed.

Test early and often:

* Developers - browser tests
* Code reviews before merging into release branch 
* Red Bee
* Henny

## Implementation examples

### Page Template

	INSERT SCREEN SHOT
	
Used HTML5 so can validates with aria and data attributes

Skips links

Landmark roles to aid screen reader navigation

Lang attribute

Unique title

Unique h1

### Content Pages

#### Content

Make sure that content is in logical order - rather than thinking about the visual design

#### HTML AND ARIA

Add hierarchical heading structure - one H1, don't skip and heading levels

Select most appropriate elements - e.g buttons and links. Ensure page is keyboard navigable and that assistive technologies can communicate content effectively

Don't over engineers or add too much aural clutter

	* heading inside lists
	* buttons inside lists

Didn't use any new HTML5 elements (e.g article/section) due to backwards compatibility

Make sure links make sense out of context - visually hide extra content if needed
	
Don't duplicate links

Make sure images have alt text when needed - but don't duplicate text

Make sure tables marked up correctly

Make sure forms marked up correctly (especially for and id) and have buttons

No title attributes - shouldn't use for core content or duplicate other text already on page

Make sure visual feedback is available without visuals - e.g selected

#### CSS

Take care not to introduce barriers

If hiding text of screen used absolute positioning - not display:none

Make sure that you implement keyboard focus as well as hover.

Check for colour contrast

Fonts resizable

Make sure content still readable when font size increased. **DEMO SPORT NAME**


### Interactive Components


#### Javascript

Where possible make sure everything works before you add javascript - Use progressive Enhancement.

Use http before implementing ajax.  Hijax

Layout should work

	EXAMPLE: carousel

If open/close 
	needs to be open if no javascript
	need to update the text button text to include open/close

	EXAMPLE: More articles and Event Table

Make inserted content (ajax) available to older screen readers -  update virtual buffer

	EXAMPLE: Event Table

Manage keyboard focus when inserting new content. Need to decide whether to take user to new content or inform them that new content has appears.

Provide instructions for how something works

	PROVIDE EXAMPLE

Keep users inform about what is going on - loading content, new content available
	
	EXAMPLE: ARIA LIVE REGION

### Medal Table

	VIDEO of Medal table


Used Hijax

Built to work without javascript. Good as means you deliver a basic/core version quickly - if you run out of time you still have something that work.  Also if there is an error it will still work. This actually happened during the olympics. A stray coma on international pages meant javascript failed.  However pages still worked.

Logical Content order - go to any page without javascript and the content is in logical order.

Most appropriate markup - th for countries 

Identify which content is selected in content layer as well as visual layer.

Alt for medal images

Visible active state for keyboard users

Inform users that content loading - aria live region

Users taken to loaded content

	WRITE UP ANY OTHER ACCESSIBILITY FEATURES IN MEDAL TABLE

### Add to Favourites

aria-labelledby and aria-describedby?

	READ UP ON 'ADD TO FAVOURITES' IN FORUM AND EMAILS
	
	SPEAK TO TIAN ASK ABOUT ACCESSIBILITY OF FAVOURITES


## Mistakes and solutions

	@ACTION - READ EMAILS WITH HENNY DURING THE OLYMPICS
	
	@ACTION - FIND RED BEE REPORT
	
	@ACTION - TALK TO SAM
	
* John's components - content not in logical order, multiple links and alt text. Wrong heading structure
* Favourite Button - a div
* Twitter module - infinite scroll, no way to exit for a keyboard user
* Couldn't play video using a keyboard.
* carousel - used field set, legend and button in links (over engineered)
* Olympic Powers - had to make lots of fixes!

* Non semantic markup in results sections. .caption etc
* Auto page refresh


## Stuff that got through / Compromises

* Team GB country page - different design, different content order
* Medal tables - only colour used to distinguish medals


## Mobile



## Video



## Lessons

Lack of known best practice - e,g
	
* how to use lists and headings
* carousel

Easy to over engineer things

Easy to introduce accessibility barriers

Progressive enhancement is key.

Thorough accessibility knowledge not as widespread amongst developers as one would hope.

Most accessibility issues are due to ignorance not carelessness or spite.

Most front end developers are keen to learn a better/accessible way of doing something - this knowledge just needs to be better well documented and findable.

Much easier to implement accessible from the start rather than 

Don't need to compromise aesthetics or functionality to achieve accessibility

Accessibility comes through diligence and attention to detail. Need to have everyone onboard as it's incredible easy for someone to accidentally introduce an accessibility barrier or usability issue.

Accessibility testing with real users is expensive - but you don't really know if you have achieved accessibility until you see a range of people and devices using your website.

You can make javascript accessible - and it can actually the improve the usability of a page for assistive technology users - e.g partial page refresh instead of full page refresh.

Aria not as well supported as you would expected - and support not well documented

There will be compromises - no such thing as perfect accessibility

## Conclusion

To make a website truly accessible buy-in is required from editorial, design and developer - and developer should implement sites/features using progressive enhancement

# Notes

## Links

* [sportui component Library](http://www.test.bbc.co.uk/sport/ui)
	* [elements](http://www.test.bbc.co.uk/sport/ui/docs/elements)
	* [columns](http://www.test.bbc.co.uk/sport/ui/docs/columns)
* [sos component library](http://www.test.bbc.co.uk/sport/olympics/2012/staticlibrary)
* [TGP Accessibility Forum]()
* [Browser Based Tests](https://confluence.dev.bbc.co.uk/display/accessibility/Browser+based+tests)
* [Building a webpage with accessibility and interoperability in mind: part 1](http://alistairduggin.co.uk/blog/accessibile-interoperable-webpage-1/)
* [Confluence - Alistair Duggin accessibility](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Home)
	* [Accessibility, Aria and screen readers](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Accessibility%2C+Aria+and+screen+readers)
	* [Accessibility - bad and good examples](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Accessibility+-+bad+and+good+examples)
	* [Accessibility Best Practices](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Accessibility+Best+Practices)
	* [Accessibility Testing](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Accessibility+Testing)
	* [Accessibility - web components](https://confluence.dev.bbc.co.uk/display/~alistair.duggin/Accessibility+-+web+components)

## Articles
* [BBC INternet Blog - BBC Sport](http://www.bbc.co.uk/blogs/bbcinternet/sport/)
	* [Delivering the Digital Olympics: a programme management perspective](http://www.bbc.co.uk/blogs/internet/posts/olympics_product_development) 5 Nov, Mark
	* [Audio and Video Streaming the Olympics](http://www.bbc.co.uk/blogs/internet/posts/audio_video_stream_olympics_tech) 16 Aug, Marina
	* [More traffic, more videos, more screens: building the BBC's Olympic site](http://www.bbc.co.uk/blogs/internet/posts/building_olympic_website) 16 Aug, Matt
		* [2012 Programme: Architecture Diagram](http://www.bbc.co.uk/blogs/bbcinternet/2012/08/21/2012_Architecture_Overview_Diagram_20120727.pdf)
	* [Olympics: Red Button](http://www.bbc.co.uk/blogs/internet/posts/olympics_red_button_and_connec) 14 Aug, Aaron
	* [The story of the digital Olympics: streams, browsers, most watched, four screens](http://www.bbc.co.uk/blogs/internet/posts/digital_olympics_reach_stream_stats) 13 Aug, Cait
	* [From starting gun to smartphone: delivering the Olympics to your device](http://www.bbc.co.uk/blogs/internet/posts/data_video_flow_olympics) 7 Aug, Cait
	* [Digital Olympics: week one in numbers](http://www.bbc.co.uk/blogs/internet/posts/olympic_statistics_traffic_week) - 3 Aug, Cait
	* [Building the Olympic Data Services](http://www.bbc.co.uk/blogs/internet/posts/olympic_data_xml_latency) 1 Aug, David
	* [Olympic Data Services and the Interactive Video Player](http://www.bbc.co.uk/blogs/internet/posts/olympic_data_services_and_the) 31 July, Oli
	* [Record breaking start to the Olympics for BBC Online](http://www.bbc.co.uk/blogs/internet/posts/online_olympics_traffic) 30 Jul, Cait
	* [BBC Olympic App on Android and iPhone](http://www.bbc.co.uk/blogs/internet/posts/olympic_app_android_iphone) 13 Jul, Lucie
	* [Olympics: User Experience and Design](http://www.bbc.co.uk/blogs/internet/posts/olympics_design)
	* [Launch of Live Interactive Video Player](http://www.bbc.co.uk/blogs/internet/posts/interactive_video_player_launc) 29 June, Alex 
	* [Olympic Favourites](http://www.bbc.co.uk/blogs/internet/posts/olympic_favourites) 29 Jun, Andy
	* [Sports Refresh: Dynamic Semantic Publishing](http://www.bbc.co.uk/blogs/bbcinternet/2012/04/sports_dynamic_semantic.html) 17 April, Jem
	* [Delivering the digital Olympics: 24 live streams via the red button](http://www.bbc.co.uk/blogs/bbcinternet/2012/04/olympics_24_streams.html) 3 April, Phil
	* [The BBC's approach to streaming the digital Olympics](http://www.bbc.co.uk/blogs/bbcinternet/2012/03/the_bbcs_approach_to_streaming.html) 30 March, Richard
	* [Sport Olympic Service Update](http://www.bbc.co.uk/blogs/bbcinternet/2012/03/sport_olympic_service_update.html) 28 March, Andy
	* [BBC Sport: Olympic page launch](http://www.bbc.co.uk/blogs/bbcinternet/2012/02/bbc_sport_olympic_page_launch.html) 8 Feb, Cait

## Videos

* [BBC WiE: Cait O'Riordan and Lucie Mclean on the digital Olympics](http://www.youtube.com/watch?v=zQg_GSb6fUY)
* [BBC Fusion Seminar: London 2012 - Alistair Duggin](http://www.youtube.com/watch?v=c1n_Btq2_5o)
* [BBC Fusion Seminar: London 2012 - Cait O'Riordan](http://www.youtube.com/watch?v=HE9NbqYTz3A)