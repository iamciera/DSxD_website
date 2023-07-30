---
title: How Do You Document a Tech Project with Comics?
date: 2023-07-30 01:00:00
description: Julia Evans
featured_image: /assets/img/theme/Evans_Figure1.jpeg
locale: en
uid: tech-comics
---

{% include language-selector.html %}

Every so often, I get emails from people saying basically, “Hey Julia! We have an open-source project! We’d like to use comics/zines/art to document our project! Can we hire you?”

Spoiler: The answer is “No, you can’t hire me”—I don’t do commissions. But I do think this is a cool idea, and I’ve often wished I had something more useful to say to people than “No,” so if you’re interested in this, here are some ideas about how to accomplish it!

<center>
<figure>
	<img src="../assets/img/theme/Evans_Figure1.jpeg" alt="Six-panel zine by Julia Evans (Twitter handle @b0rk) about the Zulip chat software. The first panel states that “Zulip has channels, kind of like Slack.” The second panel explains that “every channel is organised into threads.” The third panel shows how “catching up is easier with Zulip” with a stick person thinking, “I’ll read the lambda calculus discussion and ignore the rest.” The panel notes that there are no more notifications of 100+ unread messages on Slack. The fourth panel tells the reader that “you can easily reply to a message hours later.” The fifth panel tells the reader that Zupli is open-source and they can “pay for a hosted Zulip at zulipchat.com (or learn more about it).” The final panel gives the link to the service (chat.zulip.org) and has a stick figure of Julia saying, “I’ve been using it every day for 4 years and I love it.”">
    Julia’s Zulip Zine
</figure>
</center>

##### Comics without good information are useless

Usually when folks ask me, “Hey, could we make a comic explaining X?” it doesn’t seem like they have a clear idea of exactly what information they want to get across; they just have a vague idea that maybe it would be cool to draw some comics. This makes sense—figuring out what information would be useful to tell people is challenging! That’s probably 80 percent of what I spend my time on when making comics.

You should think about comics the same way as any kind of documentation. Start with the information you want to convey, your target audience, and how you want to distribute it (Twitter? On your website? In person?), and then figure out how to illustrate it after. :) The information is the main thing, not the art!
Once you have a clear story about what you want to get across, you can start trying to think about how to represent it using illustrations!

##### Focus on concepts that don’t change

Drawing comics is a much bigger investment than writing documentation—it takes me,
like, five times longer to convey the same information in a comic than in writing—so use it wisely! Because it’s not as easy to edit art, if you’re going to make something into a comic, you’ll want to focus on concepts that are very unlikely to change. So, talk about the core ideas in your project instead of the exact command line arguments it takes!

Here are a couple of options for how you could use comics/illustrations to document your project.

##### Option 1: a single graphic

One format you might want to try is a single small graphic explaining what your project is about and why folks might be interested in it. For example: Zulip comic1.

This is a short thing that you could post on Twitter or print as a pamphlet to give out in person. The information content here would probably be basically what’s on your project homepage, but presented in a more fun, exciting way. :)

You can put a pretty small amount of content into a single comic. With that Zulip comic, the bits of information I picked out were:

- Zulip is sort of like Slack, but it has threads.
- It's easy to keep track of threads even if the conversation takes place over several days.
- You can much more easily selectively catch up with Zulip.
- Zulip is open-source.
- There’s an open Zulip server you can try out.

That’s not a lot of information! It’s only fifty words, so to do this effectively, you need to distill your project down to fifty words in a way that’s still useful. It’s not easy!

##### Option 2: many comics

Another approach is to make a more in-depth comic/illustration, like Google’s guide to Kubernetes 2 or The Illustrated Children’s Guide to Kubernetes 3.
To do this, you need a much stronger concept than “Uh, I want to explain our project”—you want to have a clear target audience in mind! For example, if I were drawing a set of Docker comics, I’d probably focus on folks who want to use Docker in production. So, I’d want to discuss:

Publishing your containers to a public/private registry
Some best practices for tagging your containers
How to make sure your hosts don’t run out of disk space from downloading too many containers
How to use layers to save on disk space/download less stuff
Whether it’s reasonable to run the same containers in production and in development

That’s totally different from the set of comics I’d write for folks who just want to use Docker to develop locally!

##### Option 3: a printed zine

A zine is a short, self-published booklet, usually printed pretty cheaply, like a small maga**zine**.

The main thing that differentiates this from option 2 is that zines are printed. Because of that, for this project to make sense, you need to have a place to give out the printed copies. For example, maybe you’re going to present your project at a major conference? Maybe you’re going to give workshops about your project and want to give out the zine as notes? Maybe you want to mail it to people?

##### How to hire someone to help you

There are basically three ways to hire someone to help you create a graphic, comic, or zine:

1. Hire someone who both understands (or can quickly learn) the technology you want to document and can illustrate well. I'm not aware of anyone who you can hire to do this though, so it's probably not the best option. There are very few people in the intersection of "have a strong understanding of the technology", "good at writing", and "available for freelance work".
2. Collaborate with an illustrator to draw it for you. The main issue here is that if you don’t give the illustrator clear explanations of your tech to work with, you won’t end up with a clear and useful explanation. From what I’ve seen, most folks underinvest in writing clear explanations for their illustrators; I’ve seen a few really adorable tech comics that I don’t find useful or clear at all. I’d love to see more people do a better job of this. What’s the point of having an adorable illustration if it doesn’t actually teach anyone anything?
3. Draw it yourself! This is what I do, obviously. :) Stick figures are okay!

Most people seem to use option 2. I’m not actually aware of any tech folks who have commissioned comics, though I’m sure it’s happened! I think collaborating with artists is a great option, and I’d love to see more folks do it. Paying illustrators is really fun!

**Bio:**

Julia Evans is a software developer and the creator of Wizard Zines, a collection of hand-drawn programming zines focusing on jargon-free fundamentals. The latest zine in the collection is The Pocket Guide to Debugging.

References:

1. Evans, Julia. zulip: chat software I love. Twitter [https://twitter.com/b0rk/status/986444234365521920](https://twitter.com/b0rk/status/986444234365521920) (2018).
2. Deploy code faster: with CI/CD and Kubernetes. Google Cloud [https://cloud.google.com/kubernetes-engine/kubernetes-comic](https://cloud.google.com/kubernetes-engine/kubernetes-comic).
3. The illustrated children’s guide to kubernetes. Cloud Native Computing Foundation [https://www.cncf.io/phippy/the-childrens-illustrated-guide-to-kubernetes/](https://www.cncf.io/phippy/the-childrens-illustrated-guide-to-kubernetes/).
