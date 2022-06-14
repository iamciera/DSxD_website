---
title: Twelve Quick Tips for Software Design
date: 2022-06-15 00:00:00
description: Greg Wilson shares easily implemental software design tips in this shortened version of his paper by the same name. Header illustration by Ashley Caswell.
featured_image: /assets/img/theme/wilson_header.jpg
---

Most people can lift one kilogram but would struggle to lift one hundred and could not lift a thousand without planning and support. Similarly, most researchers can write a few lines of Python, R, or MATLAB to create a plot but would struggle to create a program that was a few hundred lines long and wouldn't know where to start building an application with many thousands of lines spread across dozens of modules or packages. While you may not (yet) write software at that scale, knowing how to design in the large helps ensure that you are pointed in the right direction.

### Tip 1: Design After the Fact

Researchers often don't know what their code should do tomorrow until they've seen today's results. Lots of up-front design is therefore often unprofitable, but this isn't a license to create a tangled mess: we can and should make it look as though we knew where we were going so that the next person will be able to understand our work<sup>1</sup>. Refactoring is the process of rewriting code without changing its behavior<sup>2</sup> describes common refactorings, such as "extract function" (i.e., move some code out of the function it’s in and put it in a new function that can be called separately). Just as the tidying steps in a data pipeline either convert messy data to a tidy layout or move the data from one tidy layout to another<sup>3</sup>, most refactoring operations move code toward or between well-defined patterns<sup>4</sup>.

### Tip 2: Design for People’s Cognitive Capacity

Miller<sup>5</sup> estimated that the average person could hold 7±2 items in short-term memory at once, and more recent estimates put its capacity closer to 4±1. The second tip for software design is therefore to minimize the number of "things" someone has to remember at any time to understand the code they're looking at. Breaking code into many short functions, each of which takes only a few parameters, and defining default values for most of those parameters both aid this. Another approach is to create families of functions that take similar inputs and outputs and combine them using pipes so that readers only have to "carry forward" one piece of information at a time. This model was one of Unix's key contributions to computing<sup>6</sup> and has been adopted by other programming systems like the "tidyverse" family of packages in R<sup>7</sup>.

### Tip 3: Design in Coherent Levels

Every function should implement a single logical operation. The easiest way to check if it does so is to read it aloud and ask if the steps are at the same conceptual level. For example, if I read this Python function aloud:

```
def main():
    config = buildConfiguration(sys.argv)
    state = initializeState(config)
    while config.currentTime < config.haltTime: 
        updateState(config, state)
        report(config, state)
```

The comparison in the “while” loop feels like a lower level of detail than the function calls. Replacing it with another function called something like “stillEvolving” feels more uniform:

```
def main():
    config = buildConfiguration(sys.argv)
    state = initializeState(config)
    while stillEvolving(config, state): 
        updateState(config, state) 
        report(config, state)
```

### Tip 4: Design for Evolution

The replacement shown above also makes future evolution easier. If we decide the simulation should run until a specified time or until its state has stabilized, we can make that change in the still-evolving function without modifying anything else. This example shows that good design enables independent evolution of parts so that a fix here doesn't require changes there. Programmers achieve this by separating interface (what a piece of software can do) from implementation (how it achieves that). Doing this enables construction of components that can be plugged together like USB devices. Many advanced features of programming languages exist to support or enforce this, such as being able to derive classes in object-oriented languages like Python or creating generic functions that do the same logical thing in different ways for different types of data in languages like R and Julia.

### Tip 5: Group Related Information Together

If several things are closely related or frequently occur together, our brains combine them into a "chunk" that only takes up one slot in short-term memory<sup>8</sup>. We can aid this by combining related values into data structures. For example, instead of managing the XYZ coordinates of points separately like this:

```
def enclose(x0, y0, z0, x1, y1, z1, nearness):
    ...
```

We can store points' coordinates in structures and pass those around.

```
def enclose(p0, p1, nearness):
    ...
```

Grouping related information also aids code evolution. For example, if we decide to use radial coordinates instead of Cartesian coordinates, we can change how points are represented without changing the functions that pass them around.

### Tip 6: Use Common Patterns

Some chunks appear so often that we call them "patterns" and give them names. Good programmers use these design patterns to reduce the amount of thinking they have to do and because these patterns have proven to be useful in the past. Patterns can be found at all scales of programming: "most valuable" variables<sup>9</sup>, doubly nested loops to process the elements of two-dimensional arrays, and the filter-group-summarize pattern common in data analysis are just three examples. Learning these patterns helps make someone a better programmer<sup>10</sup>.

### Tip 7: Design for Delivery

Developer operations (DevOps) is a shorthand term for automating compilation, packaging, distribution, deployment, and monitoring so that programmers can focus on other problems<sup>11,12</sup>. Investment in automation pays off many times over, but only if you design things so that they can be automated. Taschuk and Wilson<sup>13</sup> lays out some rules for doing this, and a few others include:

1. Use the same tools to build packages as everyone else who uses your language, e.g., pip for Python or devtools for R.
2. Organize your source files in the way your build system expects.
3. Use a logging library rather than print commands to report what your program is doing and any errors it has encountered.

### Tip 8: Design for Testability

Research software is notoriously difficult to test<sup>14,15</sup>, in part because its developers often don't know what output it's supposed to produce. (As a frustrated chemist once said to the author, "If I knew what the right answer was, I'd have published it already.") It is possible to test the parts of an application that parse input files, clean up messy data, etc., and doing this makes it easier to refactor code<sup>16</sup>, but we can only create tests if we design the software in testable pieces. We can check how well we've done this by asking:

- How easy is it to create the fixture that a test runs on?
- How easy is it to invoke just the behavior we want?
- How easy is it to check the result?
- How easy is it to figure out what “right” is?
- How easy is it to delete the feature? 

### Tip 9: Design as if Code Was Data

Code is just another kind of data; programs are just text files, and once a program is loaded into memory it is just another data structure whose bytes are instructions rather than characters, numbers, or pixels. The first fact allows us to use tools that process it in many ways, provided the code is designed with these tools in mind. Examples include:

- Style-checking tools that check that the layout, variable names, and other properties conform to coding standards;
- Documentation tools that extract specially-formatted comments and create cross-referenced manual pages; and
- Indexing and navigation tools that enable us to jump directly to the definition of a function or variable.

The second insight—the fact that a function in memory is just another kind of data—is the basis of many techniques for shortening and reusing code:

- Passing functions as arguments to other functions so that common operations only have to be written once.
- Storing functions in data structures so that new operations can be added to a program without changing any of the preexisting code.
- Loading modules based on configuration parameters (as in the earlier example of getting species information).

Many features in modern languages, such as lazy evaluation in R or decorators in Python, leverage this insight, and taking advantage of it can make code much smaller and easier to understand—but only if you remember that what is powerful in the hands of experts is spooky action-at-a-distance for novices.

### Tip 10: Design Graphically

Many programmers sketch when they're designing. These sketches are usually not meant as blueprints; instead, they help people externalize cognition, i.e., get their thoughts out where they can see them<sup>17,18</sup>. Among the drawings programmers often find helpful are:

- Flowcharts showing possible paths through a piece of code;
- Entity-relationship diagrams showing how database tables relate to one another; and
- Concept maps showing how the designer thinks about the overall problem.

In most cases, the act of drawing (with or without a collaborator) is more important than the drawing itself.

### Tip 11: Design with Everyone in Mind

Fairness, privacy, and security cannot be sprinkled onto software after the fact. Designers should therefore follow the principle of least privilege: every component in the system should require as few permissions as possible for as short as possible. But there is much more to safety-conscious design than just data protection. For example, if an application requires users to change their password every few weeks, security fatigue will soon set in and people will choose less and less secure passwords<sup>19</sup>. Similarly, programs should not email files to people; doing that trains them to open attachments, which is a common channel for attacks. Accessibility also can't be sprinkled onto software after the fact. Close your eyes and try to navigate your institution's website. Now imagine having to do that all day, every day. Imagine trying to use a computer when your hands are crippled by arthritis. Better yet, don't imagine it—have one of your teammates tape some popsicle sticks to your fingers so you can't bend them and see what it's like to reply to an email. A good, short guide for accessible design is a set of posters from the UK Home Office<sup>20</sup>. Each poster in this series lays out a few simple dos and don'ts that will help make your software accessible to people who are neurodivergent, use screen readers, are dyslexic, have physical or motor challenges, or are hard of hearing.

### Tip 12: Design for Contribution

Study after study has shown that diversity improves outcomes in fields from business to healthcare<sup>21,22</sup>. Good design, therefore, makes it easier for people who aren't already immersed in your project to figure out where and how they can contribute to it<sup>23</sup>:

- Software licensing is a design issue, since a program can’t use libraries whose licenses are incompatible with its own. Many designers therefore prefer permissive licenses like the MIT License to maximize the number of people who will be able to take advantage of their work.
- Applications that support plug-ins are often easier for newcomers to contribute to, as are libraries with strong and consistent conventions for passing data (like Unix command-line tools or R’s tidyverse functions).

*This piece is a shortened version of Wilson et al., 2022<sup>24</sup>.*

*Dr. Greg Wilson is a programmer, author, and educator based in Toronto. He cofounded and was the first executive director of Software Carpentry, which has taught basic software skills to thousands of researchers worldwide, and was the coeditor of Beautiful Code and The Architecture of Open Source Applications. Greg is a member of the Python Software Foundation and a recipient of ACM SIGSOFT’s Influential Educator of the Year award.*

<sup>1</sup> Parnas, D. L. & Clements, P. C. A rational design process: How and why to fake it. IEEE Trans. Software Eng. SE-12, 251–257 (1986).

<sup>2</sup> Fowler, M. Refactoring: Improving the Design of Existing Code. (Addison-Wesley Professional, 2018).

<sup>3</sup>Miller, A. M. Review of R for Data Science: Import, Tidy, Transform, Visualize, and Model Data by Hadley Wickham and Garrett Grolemund. ACM SIGACT News vol. 48 14–19 (2017).

<sup>4</sup> Kerievsky, J. Refactoring to patterns. (Pearson Deutschland GmbH, 2005).

<sup>5</sup> Miller, G. A. The magical number seven plus or minus two: some limits on our capacity for processing information. Psychol. Rev. 63, 81–97 (1956).

<sup>6</sup> Kernighan, B. W. UNIX: A History and a Memoir. (Kindle Direct Publishing, 2019).

<sup>7</sup> Wickham, H. & Grolemund, G. R for Data Science: Import, Tidy, Transform, Visualize, and Model Data. (‘O’Reilly Media, Inc.’, 2016).

<sup>8</sup> Thalmann, M., Souza, A. S. & Oberauer, K. How does chunking help working memory? J. Exp. Psychol. Learn. Mem. Cogn. 45, 37–55 (2019).

<sup>9</sup> Byckling, P., Gerdt, P.& Sajaniemi, J. Roles of variables in object-oriented programming. in Companion to the 20th annual ACM SIGPLAN conference on Object-oriented programming, systems, languages, and applications 350–355 (Association for Computing Machinery, 2005).

<sup>10</sup> Tichy, W. The evidence for design patterns. Making Software: What Really Works, and Why We Believe It 393–414 (2010).

<sup>11</sup> Gene Kim. Jez Humble. Patrick Debois. John Willis. DevOps Handbook. (IT Revolution Press, 2016).

<sup>12</sup> Forsgren, N., Humble, J. & Kim, G. Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations. (IT Revolution, 2018).

<sup>13</sup> Taschuk, M. & Wilson, G. Ten simple rules for making research software more robust. PLoS Comput. Biol. 13, e1005412 (2017).

<sup>14</sup> Kanewala, U. & Bieman, J. M. Testing Scientific Software: A Systematic Literature Review. Inf Softw Technol 56, 1219–1232 (2014).

<sup>15</sup> Hook, D. & Kelly, D. Testing for trustworthiness in scientific software. in 2009 ICSE Workshop on Software Engineering for Computational Science and Engineering 59–64 (2009).

<sup>16</sup> Feathers. Working Effectively With Legacy Code. (Pearson Education, 2005).

<sup>17</sup> Cherubini, M., Venolia, G., DeLine, R. & Ko, A. J. Let’s go to the whiteboard: how and why software developers use drawings. in Proceedings of the SIGCHI Conference on Human Factors in Computing Systems 557–566 (Association for Computing Machinery, 2007).

<sup>18</sup> Petre, M. & Van Der Hoek, A. Software Design Decoded: 66 Ways Experts Think. (MIT Press, 2016).

<sup>19</sup> Smalls, D. & Wilson, G. Ten quick tips for staying safe online. PLoS Comput. Biol. 17, e1008563 (2021).

<sup>20</sup> Designing for Accessibility. UK Home Office [https://ukhomeoffice.github.io/accessibility-posters/posters/accessibility-posters.pdf](https://ukhomeoffice.github.io/accessibility-posters/posters/accessibility-posters.pdf){:target="_blank"}{:rel="noopener noreferrer"}.

<sup>21</sup> Gompers, P. & Kovvali, S. DIVERSITY DIVIDEND. Harv. Bus. Rev. (2018).

<sup>22</sup> Gomez, L. E. & Bernet, P. Diversity improves performance and outcomes. J. Natl. Med. Assoc. 111, 383–392 (2019).

<sup>23</sup> Sholler, D. et al. Ten simple rules for helping newcomers become contributors to open projects. PLoS Comput. Biol. 15, e1007296 (2019).

<sup>24</sup> Wilson, G. Twelve quick tips for software design. PLoS Comput. Biol. 18, e1009809 (2022).
