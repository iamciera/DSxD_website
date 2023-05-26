---
title: "Multilingual Data Science: Ten Tips to Translate Science and Tech Content"
date: 2023-07-26 01:00:00
description: Yanina Bellini Saibene & Natalia Soledad Morandeira
featured_image: /assets/img/theme/bellini.png
---

Language is a cognitive instrument; it is our vehicle for learning and building our world, and thus it can become a source of exclusion.

<center>
<figure>
“Approximately 64% of Internet content is in English, although only 4.8% of the world's population speaks English as a first language. If we consider Internet users, almost 3 in 4 cannot understand more than 60% of all web content.”¹
</figure>
</center>

Data science affects many people's lives globally. This practice uses technological tools developed under global open science, software, and education, but most resources are built and published exclusively in English.

<center>
<figure>
“The predominant language of open source is English—in code, content, and community interactions—and English proficiency is a metric by which performance and personality can be judged.”²
</figure>
</center>

English is the lingua franca for data science, creating a significant barrier for non-English speakers wanting to join the field: We are not allowed to participate if we can’t understand the language.³ The authors have experienced this barrier firsthand, as we both were born in a South American country where the official language is Spanish. Being able to access and use technology and data science is a necessity to adequately teach and research in our careers.

<center>
<figure>
“The use of the English language [. . .] represents a significant trend in the history of programming language design.”⁴
</figure>
</center>

So, what actions can we take when faced with such a situation? We can use our privileges to change it, and that is where community-driven translations come into play.

## Community Path

Translations function as substitutes for original texts. You use them in place of a work written in a language you cannot read5 or that you have difficulties reading; even if you have proficiency in a second language, learning in a foreign language increases your cognitive load. Translations are one of the efforts we can undertake to create a more diverse field of data science.
We know that voluntary and collaborative content creation is possible. Open-source software and Wikipedia are great examples of how each person can do their bit. The primary advantage of working collaboratively is distributing the work (hopefully) among a diverse set of people.

In 2017, R-Ladies' Code of Conduct was translated into Spanish and Portuguese. In 2018, the Latin America R Community collectively translated the [R for Data Science (R4DS)](https://es.r4ds.hadley.nz/) book into Spanish, including the packages [datos](https://github.com/cienciadedatos/datos) (Spanish) and [dados](https://cran.r-project.org/web/packages/dados/index.html) (Portuguese).6 Then the community translated [Teaching Tech Together](http://teachtogether.tech/es/index.html) (T3) and contributed to collectively translating [Cheatsheets](https://posit.co/resources/cheatsheets/?type=translations/#translation-12), [The Carpentries](https://software-carpentry.org/lessons/)’ lessons, and [The Programming Historian](https://programminghistorian.org/es/) lessons. The active and growing Spanish-speaking community drives rOpenSci (ropensci.org) to do its [first Spanish-language code peer review](https://ropensci.org/blog/2021/07/27/censo2017/) and translate into Spanish the [rOpenSci’s book on best practices for software development, code review, and contribution to open-source projects](https://ropensci.org/multilingual-publishing/).⁷
The following ten tips summarize what we have learned in these community-driven translations from being coordinators, translators, reviewers, and editors of books and materials used by tens of thousands of people.

## 1. Motivation

Translating technical material of living documents is a long process with two well-defined stages involving different resources. The first is to achieve a full version of the translated material; the second is to keep the material updated and synchronized between the languages. The project’s type, goals, stage, motivation, and expectations should be clear from the start to have the best chance at success. Different motivation levels appear in collaborative translations:

1. **Community Motivations**: For example, making the material accessible to Latin American people and striving to use it in specific workshops.
2. **Personal Motivations**: The motivations of the specific people involved in the project, such as learning and discussing the content with other participants while translating it.
   Before people can decide to participate, we must detail the kinds of benefits they might gain, such as: learning technical skills useful beyond this project, giving back to their community, gaining experience working collaboratively in open-source and international teams, connecting with people with similar interests, increasing their network, and mentoring other people during the project.

## 2. Consent of the Text's Author(s)

Most materials have a license, and for translations, the license should allow derivative work. The authors and/or the editor may have rights to the material. Seek the authors’ consent, and involve them in the process for questions and opinions. In a technical text, the author may define novel terms, and being able to correspond with that person is essential to be as faithful to the original text as possible.
From the authors' point of view, this exchange also invariably improves the original text, from error corrections to finding more diverse examples, gaps in the content, and more. Authors can promote translations by considering this in advance when creating their content. For example, they might publish the text in a markup language, publish in a public repository, or create the text with a structure that lends itself to multi-language translation. If an organization publishes such material, it can assign funding to community translation initiatives.

## 3. Share and Document Your Process and Agreements

Having clear written guidelines for contributing and decision-making makes the entire translation process easier. In this section, we focus on **the technical aspect of a project**. See section 10 for details about constructing a **governance document** to formalize the decision-making process and describe how project participants interact.
You will need to discuss, use, and regularly update several instruments such as:
Roles and responsibilities like translator, reviewer, editor, project lead, graphic designer, etc. This helps to assign responsibilities and credit for contributions (see sections 6 and 10).
A tentative agenda with deadlines, tasks assigned, and progress tracking. This helps to keep the project on track (see section 6).

A guide detailing the standardized use of language, including:

- Voice usage (e.g., conversational, scientific, formal)
- Dialectal variety (see sections 7 and 8)
- Grammar, orthography, and punctuation rules
- Inclusive and nonsexist language guide
- Translating figures and alt text (accessibility, see section 5)
- Bilingual technical glossary (see section 9)
- Nontechnical words to be translated, such as people’s names, sports or cities in the examples (see Localization in section 4)

These project products are just as important and useful as the main translated text. Share them with an open license.

## 4. Translation in the Spotlight

Internationalization refers to the technology and design that allows software to adapt to several regions without engineering changes to the source code. The technical solution allows us to localize our content.⁸

Localization makes content more accessible and suitable within the context of another region, country, or audience.⁸ This includes language, date formats, currency, measure units, and compatibility with different characters.

There are many solutions for internationalizing and localizing content, and translation is typically the most time-consuming component.⁸

Many projects focus their efforts on internationalization, trying to choose the right tool for the job. For example, trying to decide if they should use translation management systems (Crowdin, Transifex, Weblate), automatic translators (Google Translate, DeepL), version control systems (GitHub, GitLab), markup languages (LaTeX, Markdown), and tools for writing these languages (Overleaf, RStudio).

Whatever translation tools and markup languages you choose, they should not be a barrier for the team. Choose the tools that best suit your team and the material. For instance, how important is it to prioritize version control? Updates? Preview? Output format? How high is the entry-level knowledge needed to contribute?

Additionally, create processes to help team members that cannot use a particular tool due to accessibility or their own skills. Train the team on the project’s infrastructure, develop instructions (videos, how-to guides, etc.) on using the tools, create peer translation opportunities, and organize onboarding and coworking translation meetings.

## 5. Inclusive and Nonsexist Language

Many languages utilize feminine and masculine gender indicators. Using nonsexist language or gender-equal language in translation means avoiding lexical choices that are biased, discriminatory, or exclusionary in nature. In tech and data science communities, using nonsexist language helps to fight stereotypes about gender roles and promote female and nonbinary representation.

<center>
<figure>
“The type of language we use is not innocent. If we use a language that takes as the norm and measure of humanity only a part of it (the masculine), we help to persist in the collective imagination the perception that everything that is not masculine is subsidiary, secondary and dispensable. We call this sexist use of language.”⁹
</figure>
</center>

Study nonsexist language recommendations in the language you want to translate, seek advice from experts, discuss options with the team, and document the decision to be consistent through the chapters (and projects). The Carpentries, for example, decided to always use feminine terms in their Spanish translations. In T3 and rOpenSci, we adjusted the wording to avoid having to assign a gender at all. When we couldn't prevent gender marking, we used feminine/masculine or masculine/feminine splits. For consistency throughout the text and to show that there is no particular hierarchy, we alternated the use of these splits between chapters, with the use of each one being consistent throughout each chapter. Another possibility is to use nonbinary nouns, pronouns, and adjectives (e.g., in Spanish, using -e or -x is the most common option). Which is the best option for the readers of your community?

## 6. Baby Steps and Tracking Progress and Contributions

Dividing the entirety of the work into smaller activities and milestones allows for better task assignment and tracking. For book translations, a chapter is often a good unit of division. But other items must also be translated, like figures, alt texts, code examples, and datasets. There are also extra activities: ensuring the correct use of nonsexist or inclusive language, checking spelling/grammar, and looking for alternative external references available in the language of the translation, among others.

Keeping a record of these activities allows you to intervene, assist, discuss a process, seek replacements or more participants, look for an alternative tool, and do periodic progress reports (even if no progress has been made!). For T3, we reported progress weekly in the translation Slack channel, detailing the completed tasks and thanking those who had participated. For the translation of R4DS, we updated task completion in the GitHub repository.

Tracking and reporting allows all contributions to be recognized adequately—not only the most common roles (translators, reviewers, and editors) but also those who advise on specific topics, solve technical problems, or perform graphic design work.

The tool you select to record this information will be related to the tool you choose for the translations. For example, you can use GitHub projects and issues, as we did for R4DS and rOpenSci, or you can use a shared spreadsheet and GitHub issues, as we did for T3. Some translation management systems record the progress, but not who contributes. Whichever set of tools you select, keep your progress updated, record the necessary information to give credit where it is due, and make sure you know how long each task takes. That information will be invaluable for this and other projects.

## 7. Flexibility: Don't Be Literal, and Bring the Message Closer to Your Audience

This point is directly related to localization. Examine the examples, source codes, data, idiomatic expressions, poems, songs, metaphors, and analogies included in your source material. These items cannot be translated literally (and are usually mistranslated by artificial intelligence apps). Instead, propose a translation that makes it possible to understand the expression's meaning while remaining as faithful as possible to the original text's meaning for the target audience. You can ask a bilingual person or the author themselves for insight on the phrase’s meaning, and you may also adapt the examples using regional data and local artists and cultures.

T3 has an example using Canadian geography wherein we replaced it with a Latin American example:

<center>
<figure>
Original text: “Factual errors like believing that Vancouver is the capital of British Columbia (it’s Victoria).”<br />
Spanish example: “Factual errors like believing that Rio de Janeiro is the capital of Brazil (it’s Brasilia).”</figure>
</center>

On an R4DS code snippet to teach loops, we replaced the song “Ten Green Bottles” with “Five Little Green Frogs,” the Spanish version of the song. We also translated all the data in the exercises themselves, including the variables’ names, currency, date format, and measure units. In T3, we used a poem by María Elena Walsh on a code for teaching functions.

## 8. Linguistic Diversity

A diverse language needs a diverse translating team. Some languages have dialects or regional variations. For example, “green beans” have almost ten different names across Spanish-speaking countries. In some countries, technical texts use more anglicisms than others. With people from different countries translating and reviewing one source text, these idiomatic differences will arise during the process, and by working together you can make a decision that works best for the intended audience.

Part of the agreements you will have to make is deciding which dialect or regional variation of the language is being used (R4DS, T3, and rOpenSci use Latin American conventions for the Spanish translation) and which word you will use when a concept has more than one option. Holding a team and/or community vote on these matters is one helpful idea. You also have to decide on specific details, such as what grammatical gender to use with technical concepts that don’t have a translation (or that you decide not to translate). For example, is the R-operator la pipe (she) or el pipe (he)?

The agreements must be properly documented (see section 3) to build a translation and localization community memory that can be reused and improved upon.

## 9. Create a Bilingual Glossary

A bilingual glossary contributes to the localization memory of the community. It can be as simple as a CSV file with the list of terms in the source language and their equivalent in the target language, or it can also contain the definitions in one or more languages. There are several initiatives: for T3, we built an English-Spanish dictionary of educational technology terms¹⁰; for rOpenSci, we are creating an English-Spanish glossary of research software development terms; and The Carpentries has the glosario project, a dictionary of data science terms in more than twenty languages.

## 10. Build a Community Around the Translation

The **governance document** mentioned in section 3 describes the roles, structure, organization of the work, and all the documents needed to accomplish the translations. For example, in T3, we organized the team with one leading person, two editors, one translator per chapter, and two reviewers per chapter. We also decided to discuss translation issues on Slack. If we didn’t get a consensus, we asked the community through social media and GitHub issues. Alongside participant roles, you will need to agree on and document:

- A Space for Community Interactions: This can be a Slack/Discord channel or workspace or the GitHub/Gitlab repository of the project. You can also have synchronous meetings for working and sharing the achievements of the project and the members.
- Accessibility/Diversity Statements: For example, ensuring alt text for images, using color palettes that address color blindness, allowing open access, and using an open format compatible with assistive technology such as screen readers.
- A Code of Conduct: Ensure there is a clear way to reinforce it.
- Citation, Attributions, and License: Translators have authorship of the translated contents. In T3, we mentioned the translators and reviewers below each chapter title, and we added an “About the Translation” chapter¹¹ with a short description of the project and all the participants. We also published our Translation Guidelines¹² with all the contributors as authors¹². Finally, we added a suggested citation of the Spanish version of the book according to the relative contributions along the translation process¹¹.

Last, but not least, building a community also means prioritizing the group's well-being and having the people involved in lateral projects derived from the translation. Some methods of building community might be: besides discussing governance, working on the translation itself, having social meetings, naming the group and creating a logo for it, sharing concerns and supporting others, disseminating the translation process via social media, and receiving and sharing feedback. Without forgetting the previous tips on motivation and making sure the translation is in the spotlight, ideally the group can enjoy and learn during the process, have fun working on it, celebrate everyone’s achievements, and—why not?—make new collaborations and friends!

## Concluding Remarks

Working toward multilingual data science through translations and localizations is a crucial step in removing language barriers and ensuring that the knowledge and innovations in data science are not limited to a select group of individuals who speak a certain language. This information should be accessible to everyone! Multilingual materials and the community translation process serve to advance the field and allow for a greater, more global collaboration and exchange of ideas among data scientists from different backgrounds and regions, improving the discipline as a whole.
Now, think of your favorite data science book or material. Are you aware of the importance of other people being able to access that content? How can you help make it available to them? By working together, we can create a more inclusive and diverse community of data scientists and foster a greater sense of community and collaboration within the discipline.
Bio:

Yanina Bellini Saibene is the rOpenSci Community Manager and R-Ladies project lead. She teaches coding skill since 1993. She co-founded MetaDocencia and LatinR and is a member of The Carpentries Executive Council. She lead the multilingual project at rOpenSci and is co-editor of the translation of Teaching Tech Together. She volunteer to bring R4DS, The Carpentries lessons, R-Ladies material, and Posit Cheatsheets to Spanish-speaking audience.

Natalia Soledad Morandeira is a doctor in biological sciences and a researcher with the National Scientific and Technical Research Council (CONICET) currently working at the Institute of Research and Environmental Engineering of the National University of San Martín (Buenos Aires, Argentina). Her research topics include wetland ecology, landscape ecology, and remote sensing. She is a professor of an Ecology course for Environmental Engineering. She was co-editor of the Spanish translation of the book Teaching Tech Together and is also part of the Latin American R community. She is also a fiction writer.

References:

1.  Richter, F. English is the internet’s universal language. Statista [https://www.statista.com/chart/26884/languages-on-the-internet/](https://www.statista.com/chart/26884/languages-on-the-internet/) (2022).
2.  Carter, H and J. Groopman, “Diversity, Equity, and Inclusion in Open Source: Exploring the Challenges and Opportunities to Create Equity and Agency Across Open Source Ecosystems,” foreword by Jim Zemlin, The Linux Foundation, December 2021.
3.  Odilli Uchidiuno, J. , Ogan, A., Yarzebinski, E. & Hammer, J. Going Global: Understanding English Language Learners’ Student Motivation in English-Language MOOCs. International Journal of Artificial Intelligence in Education vol. 28 528–552 Preprint at [https://doi.org/10.1007/s40593-017-0159-7](https://doi.org/10.1007/s40593-017-0159-7) (2018).
4.  Pigott, D.. HOPL, the history of Programming Languages. Wikipedia, The Free Encyclopedia [https://en.wikipedia.org/w/index.php?title=Non-English-based_programming_languages&oldid=1130348995](https://en.wikipedia.org/w/index.php?title=Non-English-based_programming_languages&oldid=1130348995) (2006).
5.  Bellos, D. Is That a Fish in Your Ear?: Translation and the Meaning of Everything. (Macmillan, 2011).
6.  Quiroga, R. ‘The development of {datos} package for the R4DS Spanish translation’. [https://rivaquiroga.cl/es/charlas/2020-rstudio-conf.html](https://rivaquiroga.cl/es/charlas/2020-rstudio-conf.html) (2020).
7.  Multilingual Publishing. [https://ropensci.org/multilingual-publishing/](https://ropensci.org/multilingual-publishing/).
8.  Wikipedia contributors. Internationalization and localization. Wikipedia, The Free Encyclopedia [https://en.wikipedia.org/w/index.php?title=Internationalization_and_localization&oldid=1125663076](https://en.wikipedia.org/w/index.php?title=Internationalization_and_localization&oldid=1125663076) (2022).
9.              Guía para el uso de un lenguaje no sexista e igualitario en la Honorable Cámara de Diputados de la Nación Argentina. [https://www4.hcdn.gob.ar/dependencias/dprensa/guia_lenguaje_igualitario.pdf](https://www4.hcdn.gob.ar/dependencias/dprensa/guia_lenguaje_igualitario.pdf)
10. Bellini Saibene, Y. English-Spanish dictionary of educational technology terms. [https://yabellini.shinyapps.io/T3Glossary/](https://yabellini.shinyapps.io/T3Glossary/).
11. Wilson, G. 2021. “Enseñar tecnología en comunidad. Cómo crear y dar lecciones que funcionen y construir una comunidad docente a su alrededor” [Teaching Tech Together. How to create and deliver lessons that work and build a teaching community around them] (Spanish translation: Y. Bellini Saibene, N.S. Morandeira, P. Corrales, L. Acion, M. Dermit, Y. Sosa, J. Benitez Saldivar, Z. Bazurto, S. Canelón, L. Canaviri Maydana, M. Alonso, A. Bellini, P. Minotti, R. Chirinos, P. Rojas, N. Stroud, R.N. Villafañe, P. Loto, A.L. Diedrichs, Y. Terrazas-Carafa & L. Rodríguez Planes). [https://teachtogether.tech/es/](https://teachtogether.tech/es/) (Original English work published in 2019).
12. Bellini Saibene, Y, N.S. Morandeira; P. Corrales; L. Acion; M. Dermit; Y. Sosa; J. Benitez Saldivar; Z. Bazurto; S. Canelón; L. Canaviri Maydana; M. Alonso; A. Bellini; P. Minotti; R. Chirinos; P. Rojas Saunero; N. Stroud; R.N. Villafañe; P. Loto; A.L. Diedrichs; Y. Terrazas-Carafa; L. Rodríguez Planes. 2022. “Orientaciones para la traducción al español de Enseñar Tecnología en Comunidad”. doi:10.5281/zenodo.7261895
