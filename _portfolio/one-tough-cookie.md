---

layout: post
title: One Tough Cookie Scholarship
thumbnail-path: "img/one-tough-cookie2.png"
short-description: "The One Tough Cookie Scholarship awarded $1,500 to a college student who shared their story of overcoming difficulties in their lives. Winners were chosen by popular vote."

---

{:.center}
![]({{ site.baseurl }}/img/one-tough-cookie.png)

## The One Tough Cookie Scholarship

This scholarship involved a voting competition to determine whose story would be considered to be the most encouraging display of endurance through difficult times. Students were encouraged to submit their stories and share on social media with their friends, as well as link their story on forums or blogs that had content relating to their stories. Besides benefitting a student in need and spreading multiple encouraging stories, I also wanted to leverage the scholarship competition in a way that would allow the participants to market our website for us, as I would get some SEO benefit from the links and social shares pointing back to our website.  

## Challenges

I first had to decide how to let people vote for their favorite submissions. The easiest way to prevent cheating was to require all voters to create an account (possibly verified through Facebook), and only allow them to vote once they had signed in. This method, however, directly contradicted our scholarship goals of having the students market their own submissions, as far fewer people are likely to vote and re-share a link if the process itself is inaccessible - similar to why you don't use a captcha on a contact form. 

I eventually decided on an open system that would allow anyone to vote once every minute. This, of course, required us to identify users specifically so as to prevent them from voting more than once a minute, but allow other users to vote when they were allowed. 

## Identifying Unique Users

There are several Javascript plugins online that claim to be able to assign a unique ID to a user just based on the information available sent to the server when a page loads. After reviewing these, however, I determined that they could be error-prone and unsafe, and decided to go with a much more simple route. I constructed a 'unique' user string with some data from the `screen` object, as well as the IP address of the user, and I stored each unique voter in a database with the timestamp of the last time they voted. When they tried to submit a vote before 60 seconds was up, we'd read the timestamp and send back an error.  

## Catching Cheaters

This was a relatively insecure method of dealing with this issue, as voters could find several different methods of changing their unique user ID, which was why I set the voting to once per minute. Any longer and it would be worth the time that it would take to cheat the system using whatever method they found.

I also assumed (correctly) that the low-hanging fruit of cheating would be creating a macro to vote for you, so I moved the vote button around after 20 minutes active on the website, and placed an invisible 'cheater' button where the original button was. If a user repeatedly clicked on the cheater button, I knew they were using a macro. In the case where a cheater button was created, I also changed the ID and classes of this button to match the original in case the macro was positioning its mouse based on Xpath. Unfortunately multiple applicants attempted to take this route and had all of their votes reset. 

## Conclusion

We were very pleased with the results of the scholarship - our winner received more than 48,000 votes in a one month time span, and his story alone received more than 100 facebook shares, which we considered to be very successful. I feel that the setup was not perfect, but for a competition that was intended to be accessible and easy, it served its purpose extremely well. 