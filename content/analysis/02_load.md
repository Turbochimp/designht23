---
Title: Load
Description: This article discusses load times on various websites.
Template: technologies
---

<div class = "box .grid-analysis wrapper-analysis" markdown=1>


Analysis of styling in Newssites
=======================

<div class="sub-grid-a sub-wrap-a urv" markdown=1>

Selection
-----------------------

<div class = "r1" markdown=1>

For this analysis i will be comparing the load times of websites owned by various swedish law enforcement agencies, such as Tullverket, Kustbevakningen and Polisen.

These websites were chosen due to them being fairly similar in the nature of the services that they provide, mainly being up-to-date information with regards to current regulations in Sweden, ongoing events and other important information.

[Polisen](https://polisen.se) is Sweden's national police agency, acting as the main body of law-enforcement across the whole country. On their website, they provide news with regards to current events, contact information for reporting crime and other information for security guards, as well as other resources.

</div>

<div class = "r2" markdown=1>

[Kustbevakningen](https://www.kustbevakningen.se/) is Sweden's Coast Guard, their work mainly revolving around rescue, surveillance and protection of Sweden's maritime environment at sea. Their website provides insight into current operations, such as the Marco Polo incident that occured in autumn 2023. 

The Swedish Coast Guard also performs controls of vessels and crew at sea, to ensure that people stay safe on the baltic sea and Sweden's coast.

Other than providing news, they post useful information with regards to fishing regulations, required permits and other resources useful for Swedish nationals and foreigners aboard vessels in Sweden's economic zone.

</div>

<div class = "r3" markdown=1>

Last, but not least is [Tullverket](https://www.tullverket.se/), Sweden's Customs agency, their work mainly revolving around controlling the circulation of contraband products. Highlighted for members of the general public, are rules and regulations with regards to online shopping, taxation of goods ordered from outside the EU and information about bringing goods back in to Sweden when having travelled abroad.

On their main site the customs agency provides updated information with a total amount of seized, illicit products that has been prevented from being brought into the country.

</div>

</div>

<div class="sub-grid-a sub-wrap-e met" markdown=1>

Methodology
-----------------------

<div class = "r1" markdown=1>


[Pagespeed](https://pagespeed.web.dev/) is a tool that provides valuable information for web-developers, including opportunities to improve efficiency and load speed by adjusting loading elements, scripts, unused assets and more.

Firefox Developer Edition also provides useful insight for developers, as the inspect-tool is easibly able to generate reports and display key information, such as load time, transferred size and requests performed.

To analyze the efficiency of these webpages I will be using both the pagespeed tool as well as the built-in developer tool in Firefox Dev Edition.

My reasoning for using both of these tools, is that I find the pagespeed tool to be lacking in some information, such as total amount of requests performed, and this information is more easily displayed in Firefox.

Firefox is set to have:
* No Throttling
* Disable Cache

</div>

</div>

<div class="sub-grid-a sub-wrap-f res" markdown=1>

Results
-----------------------


<div class = "r1" markdown=1>

<div class="flex-row-rifr" markdown=1>

<iframe class="kbv" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR6INNBnRPFYnkrwy-q-ZRdlC8CowUM8eQkUmPlEEIk9d2c5Rw4ujBs-Q4EC5LhuXUDunL05WlK4C2F/pubhtml?gid=1048930559&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

<iframe class="pol" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR6INNBnRPFYnkrwy-q-ZRdlC8CowUM8eQkUmPlEEIk9d2c5Rw4ujBs-Q4EC5LhuXUDunL05WlK4C2F/pubhtml?gid=592902256&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

<iframe class="tul" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR6INNBnRPFYnkrwy-q-ZRdlC8CowUM8eQkUmPlEEIk9d2c5Rw4ujBs-Q4EC5LhuXUDunL05WlK4C2F/pubhtml?gid=1136028191&amp;single=true&amp;widget=true&amp;headers=false"></iframe>


</div>  

<div class="flex-row-rscreenshots" markdown=1>

![Polisen](%assets_url%/img/pol-mob.jpeg "Polisen Mobil")

![Kustbevakningen](%assets_url%/img/kbv-mob.jpeg "Kustbevakningen Mobil")

![Tullverket](%assets_url%/img/tull-mob.jpeg "Tullverket Mobil")

</div>

<div class="flex-row-rdesktop" markdown=1>

![Polisen](%assets_url%/img/pol-desk.jpeg "Polisen")

![Kustbevakningen](%assets_url%/img/kbv-desk.jpeg "Kustbevakningen")

![Tullverket](%assets_url%/img/tull-desk.jpeg "Tullverket")

</div> 

<div class = "r2" markdown=1>

### Polisen

There are not many areas where Polisen's website can improve, as it already performs well, however for desktop users, one of the images on the front page lazyloads, which may be unnecessary as it will anyway for most 1080p displays as soon as the website is loaded.

The images displayed on the front page do not have a specified `<width>` or `<height>` tag, which causes layout shifts.

This may not be an issue for visitors with a higher connection speed, however can be quite jarring if the visitor has a slow connection.

### Kustbevakningen

As Kustbevakningen uses a custom font, it may be prudent to force the browser to use a custom font during loadtimes, to ensure that text remainds visible. 

The images displayed on the website also causes a large cumulative layout shift when loaded slowly. 

It would be beneficial to use more effective formats for the images displayed on the website.

Although the current ones provide a very high quality, a high amount of data needs to be transferred to view the image.

A possible solution is scaling using smaller resolutions and using .webp format instead.


### Tullverket

Similarly to Polisen and Kustbevakningen, many of the images loaded do not have set `<width>` or `<height>` tags, which can cause drastic cumulative layout shifts.

It may also be beneficial to lazyload offscreen images for mobile users, that do not see images farther down on the page due to the smaller viewport size.

</div>

<div class = "r3" markdown=1>

All of these websites have many issues in common, most common being the problem with a cumulative layout shift occuring when images load slowly.

Large portions of the data transferred from these websites consists of the images loaded.

It would be beneficial for the host and the visitor have less massive images be presented, be it at the cost of image quality. 

</div>

</div>

</div>

<div class="sub-grid-a sub-wrap-e ana" markdown=1>

Analysis
-----------------------

<div class = "r1" markdown=1>

In conclusion, two out of three websites suffer from slower loadtimes due to a few issues:
1. Image file sizes are too large
2. Image elements do not have size tags, causing layout shifts.
3. Custom fonts are used, however font-display may not be leveraged properly.

Due to the drastically increased load times of Kustbevakningens and Tullverkets webpages compared to Polisens, the visitor may experience more layout shifting and invisible text. 

Since the content on these sites in all likelyhood receives regular updates in the form of new images or text, it may take extra work to implement a new file-format for images uploaded to the webpage. 

However it would benefit the hosts of these websites to:
1. Reduce image file size
2. Specify image size tags like:
 - `<img src="gandalf.jpg" width="250" height="750" alt="Gandalf the Grey">`
3. Lazy-load images that are not immediately visible on landing page `load="lazy"`
4. Avoid showing invisible text, i.e
 - `src: local('comic sans'),
 url(https://customfonturl);
 font-display: swap;`


### The 'Winner'

Polisen's website outperformed the other websites by far, having less amounts of data being transferred and smaller images, giving it a perfect score.

Kustbevakningen and Tullverket share a commonc second place, as they both had reasonably similar scores, with faults in the same area.

As all of these are government agencies, it is reasonable to believe that the developer for Kustbevakningen's and Tullverket's websites may be the same firm or company, if the project was outsourced.

These tests were completed without the webbrowser cache enabled, this still reflects the performance that a browser may have when visiting the website for the 'first' time, however it is reasonable to expect that most visitors may save the cookies and cache stored by websites, thereby improving loadtimes on repeat visits.

All of the websites covered are however, still very well designed and are simple to navigate, and deliver the information that they are supposed to in an efficient manner.

Preferrably, the website should be viewable in under two seconds on a good, and load completely within tree to four seconds, on connecting for the first time, this is from the perspective of a user that has a stable internet connection, preferrably through fiber or 5G.

Due to the larger size of some of the image files and fonts, these sites, except for Polisen's website, do not load within my personal standards.

</div>

</div>

<div class="sub-grid-a sub-wrap-d etc" markdown=1>

Author
-----------------------

<div class = "r1" markdown=1>

This article was written by Benjamin Thulesen.

</div>

</div>

<div class="sub-grid-a sub-wrap-a ref" markdown=1>

References
-----------------------

<div class = "r1" markdown=1>

Sites used in this article:

- [Polisen](https://polisen.se)
- [Kustbevakningen](https://www.kustbevakningen.se/)
- [Tullverket](https://www.tullverket.se/)

</div>

<div class = "r2" markdown=1>

This exercise is part of kmom05 in the design course: [Teknisk webbdesign och användbarhet](https://dbwebb.se/kurser/design-v3)

</div>


<div class = "r3" markdown=1>

Other tools used:

1. [PageSpeed Insights](https://pagespeed.web.dev/)
2. [Firefox Browser Dev Edition](https://www.mozilla.org/en-US/firefox/developer/)

</div>

</div>

</div>