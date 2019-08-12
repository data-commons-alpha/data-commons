---
title: Research Questions
tags: [data_questions, research_questions]
keywords: reference, library, research, questions, data
last_updated: August 12, 2019
summary: "The Research Questions Page is designed to list current and potential research questions that need to be answered.  If you are interested in helping with the analysis or providing data to the commons, please contact us @ <email>."
sidebar: mydoc_sidebar
permalink: mydoc_research_questions.html
folder: mydoc
---

## Ongoing Research Questions 
There are currently no ongoing projects or research questions being answered in the IVMF Data Commons.

## Potential Research Questions
(1) Do veterans use IVMF resources upon leaving military service?

(1b) Do veterans who use IVMF resources return to their home of record?

(1c) How successful are veterans who use IVMF resources upon returning to their home of record or other location?

(1d) Does a veteran returning to their home of record make them more likely or less likely to successed, given it is in a location where IVMF resources are offered?  



# About content reuse
You can embed content from one file inside another using includes. Put the file containing content you want to reuse (e.g., mypage.html) inside the \_includes/custom folder and then use a tag like this:

{% raw %}
```
{% include custom/mypage.html %}
```
{% endraw %}

With content in your \_includes folder, you don't add any frontmatter to these pages because they will be included on other pages already containing frontmatter.

Also, when you include a file, all of the file's contents get included. You can't specify that you only want a specific part of the file included. However, you can use parameters with includes.

{% unless site.output == "pdf" %}
See the following Jekyll cast for more info about using parameters with includes:

<iframe width="640" height="480" src="https://www.youtube.com/embed/kzpGqdEMbIs" frameborder="0" allowfullscreen></iframe>
{% endunless %}

# Page-level variables

You can also create custom variables in your frontmatter like this:

{% raw %}
```yaml
---
title: Page-level variables
permalink: page_level_variables/
thing1: Joe
thing2: Dave
---
```
{% endraw %}

You can then access the values in those custom variables using the `page` namespace, like this:

{% raw %}
```
thing1: {{page.thing1}}
thing2: {{page.thing2}}
```
{% endraw %}


I use includes all the time. Most of the includes in the \_includes directory are pulled into the theme layouts. For those includes that change, I put them inside custom and then inside a specific project folder.

{% include links.html %}
