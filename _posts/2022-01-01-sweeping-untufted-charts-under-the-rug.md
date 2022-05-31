---
title: Sweeping Untufted Charts Under the Rug
date: 2022-01-01 00:00:00
description: Violeta Roizman
featured_image: /assets/img/sections/pattern_19.jpg
---

When discussing the future of data science during the Creator Conference, one of the main ideas that resonated with me was improving accessibility to data and information. As part of my everyday work, I usually create data visualizations to summarize and communicate insights to clients and stakeholders. I want those insights to be available to everyone, so as a minimum requirement, visualizations I put out there on the web should include alt-text. Alt-text (short for alternative text) is a description of an image that can be read out loud by screen readers, assistive technology for interacting with the content on computer screens without relying on sight. I wondered what the progress of accessibility in the overall dataviz field was. I imagined a line chart for the number of published data visualizations with alt-text: an increasing number, still low in the present but constantly increasing towards the future.

There happens to be data to create this exact line chart based on the visualizations shared by the data visualization learning community, known as Tidy Tuesday (#TidyTuesday on Twitter)<sup>1</sup>. Each Monday a data set is published, and the TidyTuesday community is encouraged to tidy it up and share a data visualization based on it. Silvia Canelón and Liz Hare presented a talk<sup>1</sup> at the CSV conference about the room for improvements in accessibility within the Tidy Tuesday practice<sup>2</sup>. Among other interesting facts, they found that only 3% of the published data visualizations were accompanied by alt-text.

I wanted to represent this information in a new (at least for me) medium and one that does not rely on sight to access the main point of a graph: I created a tactile data visualization heavily inspired by one of the graphs in Canelón and Hare’s presentation. I found that it was really impactful to compare the number of alt-texted images vs. the total number of images, and I wanted to keep this comparison in my visualization. The differences between my version of the visualization and the original are sometimes driven by medium needs (spoiler: I made a tufted rug!), and sometimes they are my own design choices.

<center>
<figure>
	<img src="../assets/img/theme/roizman_figure1.jpg" alt="A photo of someone sitting in front of a large piece of fabric with a line chart on it. A dog is on the floor next to them.">
	<figcaption>After the building of the frame, the tufting of the rug can begin. At home in Argentina creating the piece with Mojo the dog.</figcaption>
</figure>
</center>

The idea of perceiving the data in another way than visually is interesting, and the fact that the rug could be around in everyday life seemed kind of cool. On top of this, I wanted to play with the concept of presenting the data in (Edward) Tufte’s fashion. For example, I was wondering what the data-to-ink ratio would mean in this fabric context. (Would Tufte find this exercise just a form of chart junk? Perhaps.) I’m not an expert at all on this format, but I had already made rugs in the past.

<center>
<figure>
	<img src="../assets/img/theme/roizman_figure2.jpg" alt="A photo of a line chart on a rug taken from an angle showing the relief of the design, with the lines sticking out.">
	<figcaption>Close up showing fiber details of the tufted rug.</figcaption>
</figure>
</center>

Knowing that it takes a lot of time, I decided to use a tufting machine, which I was able to acquire thanks to the DSxD funding. Then, I had to order the materials and construct all the needed setup. I started this process in France and continued it in Argentina, where I bought some wood and constructed the frame with my own hands (with a little help from my father). I’m super proud of this part, because normally I wouldn’t be able to tell the difference between screws and nails. The next step was to draw the chart pattern on the rug fabric by using a projector.

Then I needed to fill the white background with wool. I enjoyed this process, but the learning curve was clearly visible on the carpet. The areas where I started looked much sparser than those I tufted later on. In the end, I had to fill the sparse areas in order to homogenize the whole surface. I decided to use a different texture for each of the tufted lines. The line in pink, which represents the number of dataviz without alt-text, is longer and in loop. The bottom green line, which represents the number of dataviz with alt-text, is a bit shorter and cut. As a result, one can tell the difference simply by touching the surface, even without being able to look at it.

Looking at the final chart and output of my project, I realize I was being quite optimistic when thinking about the current progress of accessibility in terms of alt-text. However, even if improvements are quite recent and in small steps, there is hope for a more accessible future. People like Canelón and Hare raising awareness of this topic really make a huge impact. As is annotated on their visualization, the increase of alt-texted dataviz towards the end of the chart happened just after they published the preliminary results from their presentation on Twitter. My project, this recreation in a tactile medium, offers a new dimension to perceive this data, but unfortunately only a limited number of people that visit my parents’ house in Argentina will truly be able to “access” it. You are all invited to visit and touch the data. :)

<center>
<figure>
	<img src="../assets/img/theme/roizman_figure3.jpg" alt="A line chart on a rug showing that the number of data visualizations with alt-text is lower than those without alt-text in 2020-2021.">
	<figcaption>Final piece measuring 0.73 m x 1.15 m.</figcaption>
</figure>
</center>

The data materials and analyses are available at the following sites:

1. Data: [github.com/spcanelon/TidyTuesdayAltText](https://github.com/spcanelon/TidyTuesdayAltText){:target="_blank"}{:rel="noopener noreferrer"} 
    
	(licensed under CC BY-SA 4.0)

2. The data analysis that Silvia and Liz performed:
    [github.com/spcanelon/csvConf2021](https://github.com/spcanelon/csvConf2021){:target="_blank"}{:rel="noopener noreferrer"}
    
	(licensed under CC BY-SA 4.0)
3. My take on the dataviz: [github.com/violetr/tufted-rug](https://github.com/violetr/tufted-rug){:target="_blank"}{:rel="noopener noreferrer"} 
    
	(licensed under CC BY-SA 4.0)


*Violeta Roizman is a freelance data scientist with a background in applied mathematics. She is passionate about solving problems and telling stories with data. She loves everything related to data visualization, data art, creative coding, and machine learning. She is also interested in tea, art in general, feminism, and eco-activism. You can find Violeta on Twitter as @violetrzn if you have any questions or ideas.*

<sup>1</sup> TidyTuesday: Official repo for the #TidyTuesday project. [https://github.com/rfordatascience/tidytuesday](https://github.com/rfordatascience/tidytuesday){:target="_blank"}{:rel="noopener noreferrer"}.

<sup>2</sup> Canelón, S. csvConf2021: Data visualization accessibility talk for csv,conf,v6 (2021). [https://github.com/spcanelon/csvConf2021](https://github.com/spcanelon/csvConf2021){:target="_blank"}{:rel="noopener noreferrer"}.