## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Naman-Goyal/github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Naman-Goyal/github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact


Having trouble with Pages? Check out our documentation or contact support and we’ll help you sort it out.

{% assign orderedRepos = site.github.public_repositories | sort: 'stargazers_count' | reverse %} {% for repository in orderedRepos %} {% assign homepageLength = repository.homepage | size %} {% if homepageLength > 0 %}

{{repository.name}} | [repo]({{ repository.html_url }}) | [pages]({{ repository.homepage }})
{% else %}

{{repository.name}} | [repo]({{ repository.html_url }})
{% endif %}

{{repository.description}}
{% octicon repo-forked size:small%} {{repository.forks_count}} {% octicon star size:small %} {{repository.stargazers_count}}

{% endfor %}

