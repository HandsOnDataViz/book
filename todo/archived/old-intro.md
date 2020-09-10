OLD INTRO

## What is Data Visualization? {- #what}
TODO: Rewrite this entire section

Data visualization is broadly defined as a method of encoding quantitative, relational, or spatial information into images. Classic examples include [Charles Menard's figurative map](https://en.wikipedia.org/wiki/Charles_Joseph_Minard) of Napoleon's defeat and retreat during the Russian campaign of 1812, and [John Snow's dot map](https://en.wikipedia.org/wiki/John_Snow) of cholera cases during the London epidemic of 1854.

![Images: Menard's figurative map (left) and Snow's dot map (right), from Wikimedia](images/0-introduction/examples-Minard-Snow.png)

This free online introductory book focuses on selected topics in data visualization:

**Charts and maps** Despite the growing variety of visualization types, this book features chapters on creating [charts](chart) and [maps](map), and a wide range of ways to communicate with these classic models.

**Reusable tools and templates:** Unlike infographics created for one-time use, all of the tools and templates in this book are recyclable, and allow you to upload a new dataset to display your story.

**Free and easy-to-learn:** We have selected data visualization tools that are free to use (or work on a freemium model, where advanced features or higher usage requires payment), and searched for those that we believe are easy-to-learn, based on our teaching experience with undergraduate students and non-profit community organizations.

**Interactive on the open web:** Many books assume that you will deliver your data visualizations to in-person audiences on printed paper or presentation slides. But in this book, we show how to [embed interactive charts and maps on your website](embed), to share with the wider public.

**Storytelling:** Data visualization is more than pretty pictures. In this book, the best visualizations are those that [tell your data story](story) -- and pull readers' attention to what really matters -- by combining images and text, and offering exploration with explanation.

- Michael Friendly and Daniel J. Denis, “Milestones in the History of Thematic Cartography, Statistical Graphics, and Data Visualization,” 2001, http://www.datavis.ca/milestones/
- Isabel Meirelles, Design for Information: An Introduction to the Histories, Theories, and Best Practices Behind Effective Information Visualizations (Rockport Publishers, 2013), http://isabelmeirelles.com/book-design-for-information/
- Edward Tufte, The Visual Display of Quantitative Information (Graphics Press, 1983), and subsequent works at https://www.edwardtufte.com

## Why this book? {- #why}

TODO: Rewrite this entire section... emphasize what the book is and is not....   Our goal is to provide a comprehensive and accessible introduction to creating interactive visualizations with free and easy-to-learn tools and data sources. While most technical books specialize in one tool in great depth, our approach covers about a dozen tools, describes concepts for why and how to use them, with hands-on examples. Based on our experience in teaching introductory college courses, workshops, and a global online course, we tailored the text and images so that anyone with a computer can pick up the book and start learning, without pre-requisites.

What the book is not: an advanced manual in R.....


*Hands-On Data Visualization*, an open-access online textbook, seeks to help you tell your story---and show your data---through the power of the public web.

This open-access book reflects what I've learned while teaching data visualization [to undergraduate students at Trinity College](http://commons.trincoll.edu/dataviz), and now [to a global online class on the Trinity edX platform](https://www.edx.org/school/trinityx). Over the past few years, Trinity students and I have built interactive charts and maps in partnership with non-profit organizations in Hartford, Connecticut, to help them share their stories with data on the public web. Also, my students and colleagues have used these tools to create [On The Line: How Schooling, Housing, and Civil Rights Shaped Hartford and its Suburbs](http://ontheline.trincoll.edu), an open-access book-in-progress that features interactive historical maps of urban-suburban change. Students and colleagues who wrote tutorials, designed learning exercises, or developed code templates for *Hands-On Data Visualization* are listed as [authors and contributors](authors).

Although my outstanding colleagues have professional training, do not confuse them with me, the proverbial "Jack of all trades, master of none." I do not consider myself an expert in data visualization, nor should anyone mistake me for a computer scientist or data scientist. Inspect my higher education transcripts and you'll see only one computer science class (something called FORTRAN77 back in 1982), and not a single course in statistics, sadly. Instead, my desire to learn data visualization was driven by my need as an historian to tell stories about urban-suburban places and change over time. If you've ever watched me teach a class or deliver a presentation on these topics -- always talking with my hands in the air -- you'll understand my primal need to create charts and maps. Stories become more persuasive when supported with data, especially well-crafted images that convey data relationships more clearly than words. Furthermore, these data stories become more powerful when we share them online, where they reach broader audiences who can interact with and evaluate our evidence.

In the early 2000s, when I began to dabble in data visualization, our tools were expensive, not easy to learn, and not designed to share our stories on the public web. (One of my well-worn jokes is point to the bald spot on my head, and claim that it was caused while tearing out my hair in frustration while using ArcGIS.) But everything began to change around 2005 when Google Maps publicly released its application programming interface (API) that allowed people with some coding skills to show data points on an interactive web map. Gradually, between 2008-11, I began learning what was possible by working on map projects with talented programmers and geographers, such as Jean-Pierre Haeberly at Trinity, and Michael Howser at the [University of Connecticut Libraries Map and Geographic Information Center](http://magic.lib.uconn.edu/) (MAGIC, my favorite acronym), thanks to a grant from the [National Endowment for the Humanities](http://www.neh.gov). Free and low-cost workshops sponsored by [The Humanities and Technology Camp](http://thatcamp.org) (THATCamp) at the Center for History and New Media at George Mason University, and [Transparency Camp](https://sunlightfoundation.com/transparency-camp/) by the Sunlight Foundation, introduced me to many people (especially Mano Marks and Derek Eder) who demonstrated easier-to-use tools and templates, such as Google Fusion Tables and GitHub. Closer to home, Alvin Chang and other data journalists at the [Connecticut Mirror](http://ctmirror.org) showed me how to tell stories on the web with more flexible open-source tools, such as Leaflet and Highcharts.

All of these data visualization lessons I learned have been so valuable---to me, my students, our community partners, and thousands of readers on the web---that my co-authors and I have agreed to share our knowledge with everyone for free. This open-access book is guided by the principle of democratization of knowledge for the public good, hence the book's title: *Hands-On Data Visualization*. Not everyone can afford to make this choice, I realize. But the [mission of Trinity College](http://www.trincoll.edu/AboutTrinity/mission/Pages/default.aspx) is to engage, connect, and transform, with both our local city of Hartford and the world at large. Since Trinity already pays my salary as a tenured professor, the right thing to do with the knowledge my students and I have gained is to pay it forward. That's why we created *Hands-On Data Visualization.*

If this free book is valuable for your education, then join us by sharing and supporting it for future readers:

- Tell your friends about the book and share the link via social media, text, or email
- Improve the book by adding comments or suggesting new chapters on our GitBook platform

Try out the tutorials, explore the online examples, share what you've learned with others, and dream about better ways to tell your data stories.

Warning: To follow the steps in this book, we recommend either a desktop or laptop computer, running either the Mac or Windows or Linux operating system, with an internet connection and a modern web browser such as Chrome, Firefox, Safari, or Edge. Another good option is a Chromebook laptop, which enables you to complete *most* of the steps in this book, and we'll point out any limitations in specific chapters. While it's possible to use a tablet or smartphone device, we do not recommend it because you cannot follow all of the steps, and you'll also get frustrated with the small screen and perhaps throw your device (or this book) across the room, and possibly hit someone else in the head. Ouch! We are not responsible for injuries caused by flying objects.

Tip: If you're working on a laptop, consider buying or borrowing an external mouse that can plug into your machine. We've met several people who found it much easier to click, hover, and scroll with a mouse rather than a laptop's built-in trackpad.

Tip: If you're new to working with computers---or teaching new users with this book---consider starting with [mouse exercises](http://www.pbclibrary.org/mousing/mousercise.htm). All of the tools in this book assume that users already know how to click tiny buttons, hover over links, and scroll web pages, but rarely are these skills taught, and everyone needs to learn them at some point in our lives.

<!-- TODO: I added the tips above because these are huge yet surmountable obstacles for many people I've worked with, especially older generations and incarcerated people. But I'm uncertain about the link to the mouse exercises. Perhaps I should tweet at public library staff and instructors to find better beginning resources? -->
