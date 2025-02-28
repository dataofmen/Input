[[ReadItLater]] [[Article]]

# [Never skip research day - UX Collective](https://uxdesign.cc/never-skip-research-day-7890ab3ea31c)

A comic illustration of ripped fitness pals exercising because they love research so ‘effing much. Credit: [me](http://tripcarroll.com/).

## It’s a powerful tool for organizational influence.

[

![Trip Carroll](Attachment/Trip%20Carroll.png)



](https://tripcarroll.medium.com/?source=post_page---byline--7890ab3ea31c--------------------------------)

[

![UX Collective](Attachment/UX%20Collective.png)



](https://uxdesign.cc/?source=post_page---byline--7890ab3ea31c--------------------------------)

You’re in your 30s. You’ve gained a little weight. You’re not fat, but some of your clothes don’t fit anymore. It’s not that big of a deal, but you’re starting to feel kind of old. You have a best friend who’s the same age as you, but he’s annoyingly fit, possessing the body of a greek god. He tells you that fitness is simple, that really all you need to do is know a handful of things and be consistent. You ignore him. But he keeps bringing it up. He offers to buy you a book if you promise you’ll read it. You promise, if only to shut his stupid mouth.

But the book kind of makes sense. In fact, this whole fitness thing doesn’t seem so hard after all. You try it. You loose 30lbs! You feel amazing!!!

WHY DIDN’T YOU LISTEN TO YOUR BEST FRIEND SOONER?!?

You know how you’ve experience all this? Yea… Me neither… But my best friend Chase does.

And his story is my story, but for user research.

## Always picked last…

I have led a design system team for the past three years. Throughout that time we have really struggled to make changes in our products. There are a multitude of reasons for that, [some of which I’ve covered here](https://medium.com/user-experience-design-1/youre-trying-to-turn-an-oil-tanker-288ed30876e4). Until very recently, we haven’t had an engineering team, so any kind of changes we wanted to make in our system were hamstrung by a lack of resources and shifting priorities.

This is the true problem that design system designers often face. [Nathan Curtis does an incredible job outlining it here in his article detailing the issues with a federated design system](https://medium.com/@nathanacurtis/the-fallacy-of-federated-design-systems-23b9a9a05542). Design systems don’t bring in revenue. We’re a shared service. We save money, we don’t make it. We make internal tools that allow engineers, designers, and product managers to solve real, valuable problems for our users (instead of reinventing wheels). Our work makes theirs more efficient, effective, and waaaaaaaaaaay sexier.

But we don’t sell products.

So, business leaders often give us the shaft. Product managers preferring to implement a new feature that will generate $5M in revenue than implement a few bug fixes that will save us $10M in accessibility fines.

I get it. Money is good. It’s a resource that we need to continue to make great work. But rolling rocks up hill is really hard, and I get really, really sad watching them roll back down.

I need another tool to affect more change in my organization.

## Research, my old friend, why did I ignore you for so long?

As UX designers, one of the most valuable tools in our toolkit is the skill to validate our design decisions with user research. It’s invaluable to making quality design decisions. And I’m sorry to say (at least in my my organization, particularly on my team) we rarely use it. We’ve had so many problems to solve rebuilding our Figma libraries, resolving design system requests, and telling engineering executives to stop making houses out of duct tape. User research was something that feature designers and our dedicated research team do, not us.

I was a big ‘ole idiot. Don’t be like me.

This decision severely hampered our ability to make a serious impact into the products we’re trying to serve. But, luckily for us, despite our camel’s capacity to carry a metric ton of straw, it’s back finally broke.

A screenshot of an incredible custom Figma plugin that we developed to sync our icon library with GitHub. It’s absolutely beautiful.

## A better icon library

One of the primary products that we serve is the Webex App. It’s a messaging and video chat tool. And, though on days when I’m honest I miss Slack, Webex is actually pretty great! It has noise cancellation that is literally magic, something that I, a father of three tiny embodiments of pandemonium and chaos very much appreciate.

We manage the icon library, and over the last year have develop some really amazing improvements. We collaborated with some web engineers to build a custom Figma plugin that allows us to sync our Figma component library with GitHub. There the raw SVGs are processed, optimized, and exported into a variety of formats used by various platform teams (Web, MacOS, iOS, Windows, and Android), all version controlled by NPM.

I could’ve sword I heard angels singing when we pushed our first icon.

Before this plugin was developed the entire process was manual. We might as well have carved our SVGs out of rocks (it would have gone faster). But after interviewing product and platform teams to understand their specific needs, we consolidated our icon system to a single pipeline where we could maintain consistency.

Well… Consistency for everything but…

A screenshot of the method that we used to export multicolored icons for the Windows platform. Multicolored icons are duplicated across dark and light themes. We had to use a completely separate methods for other platforms.

## Multi-colored icons

Ninety-nine percent of our library were single colored icons. Developers and designers could apply our color tokens to those icons in order to change their colors. However, there were a handful of icons in our library that contained two colors.

These icons were very problematic for us. They couldn’t use color tokens, and needed to be built in very different ways depending on the platform consuming them. Their usage of color also violated our icon color system, which made them illegible and confusing.

But they had been in our product for a long time…

We informed our product teams that they would either need to move to single colored icons or support their own multicolored icon library. That worked for most teams, but not all.

## Conflict

One of our product teams where the multicolored icons were used heavily pushed back. They said that their users were familiar with the icons and that moving to single colors would create a disruptive experience. We argued that, not only would it be easier for us to support, but it would make the icons far more legible and accessible.

No one budged an inch.

A screenshot of how the Webex App currently uses multicolored icons in its messaging interface.

A screenshot of our proposal for single colored icons.

## Research to the rescue!

Before Cisco, I used to work at a company called “Blackboard” (now Anthology). It was my first UX job, and thanks to my team leader, I received an education in user research (thank you so much Kelsey!). I was on a team exploring ideas for a new data and analytics tool that Blackboard wanted to create. We performed a tremendous amount of qualitative research via contextual inquiries and user interviews, as well as quantitative research with concept testing and surveys. It was an awesome opportunity, performing the research necessary to build a new product from the ground up.

And it gave me all the tools I should have needed to do research well. Yet, despite the depth of my knowledge, for years I had neglected to seriously implement it into my work here at Cisco.

A screenshot comparing the multicolored Mute Icon with the single colored Mute Icon.

A huge mistake.

When we started getting pushback from that product team, a switch finally flipped. We reached out to our research team to see if we could create a small usability test to validate (or invalidate) our design decisions. They didn’t have capacity to run it themselves, but helped us get set up with our tools and provided some advice.

After building a small proposal, we shared it with the product team, and looped in the lead designer on the research project. We wanted their feedback to make sure that the test we built wasn’t biased towards our goals. We created a simple A/B test asking question about icon clarity, scanability, and user preference between the two designs.

A screenshot comparing the multicolored Video Icon with the single colored Video Icon. Which one do you think is on? Can you tell?

Despite testing users who were very familiar with Webex, the results were conclusive.

A screenshot of four pie charts detailing the results of our research: Mute Button 4 participants prefer multicolored 6 prefer single-colored icons, Video Button 2 participants prefer multicolored 8 prefer single-colored icons, Record Button 1 participants prefer multicolored 9 prefer single-colored icons, Overall 3 participants prefer multicolored 7 prefer single-colored icons.

We synthesized the results and shared them with designs and the PM from the product team. Surprisingly, no pushback. The PM was sold, a Jira ticket was put on the backlog, and very suddenly, a problem that had plagued us for months was no more.

## Conclusion

One of our key skills as UX designers is the implementation of user research to validate design decision making. Don’t be like me. Don’t ignore the health of your UX practice. Do more research. It’s a powerful tool that can influence your organization in the right direction.

Honestly, after this project I felt like we were playing GoldenEye, and I just picked up the golden gun. What was this powerful weapon that my team was now wielding? Why weren’t we using it from the very beginning?!?

Currently, my entire team and I are undergoing a user research training course. I swear to you that we will only use our power for good (and world domination)!