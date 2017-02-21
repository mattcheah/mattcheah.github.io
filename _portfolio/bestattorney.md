---

layout: post
title: BestAttorney.com
thumbnail-path: "img/bestattorney.com.png"
short-description: "BestAttorney.com is the website for the Orange County-based personal injury law firm Bisnar | Chase."

---

{:.center}
![]({{ site.baseurl }}/img/bestattorney.com.png)

## Bisnar Chase Personal Injury Attorneys

Bisnar Chase Personal Injury Attorneys hosts information about their firm on their website BestAttorney.com, in addition to practical information and recommendations for injury victims. The firm also posts injury related news stories from local incidents and updates on national situations that affect consumer safety. 

## Static and Slow 

When I was first hired in November of 2014 to perform marketing and web development, bestattorney.com did not look too different than it does now. The inside structure however was a different matter. The website was running on html files with very little dynamic content, and many scripts were included that could all perform similar functions without any thought to page speed or organization. Multiple tracking scripts for analytics and ads were included at various points throughout each page and numerous CSS styles would override each other while some large chunks of CSS would not be used on the pages they were loaded on.  

## First Actions

Cleaning up the website was a slow process, as it had to be organized in a clean and understandable manner while maintaining a consistent look on the website. While working with a team of marketing consultants, I organized header and footer dynamic files, consolidated all tracking and analytics to be loaded by Google Tag Manager, created CSS sprite sheets to load all of the common image resources in one http request, and got rid of a lot of unnecessary scripts. One such script I got rid of was jQuery on a majority of internal pages, where all functions previously carried out by the library could have been rewritten in native Javascript, which is what I did. 

## Results

With the constant improvements being made over a period of 2 years, the website load times were almost cut in half from an average of 6 seconds to 3.5 seconds. Changes to the website are now much more simple to make, as templated files can be edited in one place supplementary sidebar or footer content can be diverse or identical across similar sections of the website without having to hardcode anything. The website also conforms to technical SEO standards with appropriate inter-page linking, SCHEMA markup, breadcrumbs, canonical tags, and analytics event tracking.  