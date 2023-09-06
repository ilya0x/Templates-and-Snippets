[//]: # "TITLE"

# Templates and Snippets _(Templates-and-Snippets)_

[STATUS]: # "Required"
[NOTE]: # "Title must match repository, folder and package manager names - or it may have another, relevant title with the repository, folder, and package manager title next to it in italics and in parentheses."

<!----------------------------------------------------------->

[//]: # "BANNER"
[STATUS]: # "Optional"
[NOTE]: # "Must not have its own title, must link to local image in current repository, must appear directly after the title."

![banner](images/banner.png)

<!----------------------------------------------------------->

[//]: # "BADGES"
[STATUS]: # "Optional"
[NOTE]: # "Must not have its own title, must be newline delimited."

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

<!----------------------------------------------------------->

[//]: # "SHORT DESCRIPTION"
[STATUS]: # "Required"
[NOTE]: # "less than 120 characters, match the description in the packager manager's description field, Must match GitHub's description"

Templates and snippets for Python, HTML, CSS & SASS, and Markdown.

<!----------------------------------------------------------->

[//]: # "LONG DESCRIPTION"
[STATUS]: # "Optional"
[NOTE]: # "Must not have its own title. If any of the folder, repository, or package manager names do not match, there must be a note here as to why."
[NOTE]: # "This should describe your module in broad terms, generally in just a few paragraphs. Ideally, someone who's slightly familiar with your module should be able to refresh their memory without hitting 'page down'. As your reader continues through the document, they should receive a progressively greater amount of knowledge."

<!----------------------------------------------------------->

[//]: # "TABLE OF CONTENTS"
[STATUS]: # "Required; optional for READMEs shorter than 100 lines."
[NOTE]: # "Comments"

## Table of Contents

- [<b>Security</b>](#security)
- [<b>Background</b>](#background)
- [<b>Install</b>](#install)
- [<b>Usage</b>](#usage)
- [<b>Snippets</b>](#snippets)
- [<b>Templates</b>](#templates)
- [<b>Maintainers</b>](#maintainers)
- [<b>Thanks</b>](#thanks)
- [<b>License</b>](#license)

<!----------------------------------------------------------->

[//]: # "SECURITY"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Security

- Templates contain placeholder IP addresses and ports. You will need to replace them for your specifications.
- Same goes for placeholder usernames and passwords.

<!----------------------------------------------------------->

[//]: # "BACKGROUND"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Background

Python programmers tend to not enjoy working with HTML and CSS - and who can blame them? Most of it is reused from project to project with just some basic changes. [Emmet](https://docs.emmet.io/cheat-sheet/) is a great web-developer’s toolkit that takes the snippets idea to a whole new level. This project's goal is to create complete file templates and expand on Emmet snippets to eliminate as much HTML and CSS work as possible, maximizing Python programmers' use of time on actually programming in Python.

I will be updating this repository on regular basys.

<!----------------------------------------------------------->

[//]: # "INSTALL"
[STATUS]: # "Required by default, optional for documentation repositories."
[NOTE]: # "Comments"

## Install

This project does not require any additional installations.

<!----------------------------------------------------------->

[//]: # "USAGE"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Usage

This is only a documentation, templates, and code snippets package.

<!----------------------------------------------------------->

[//]: # "Snippets"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Snippets

Go to Settings > User Snippets, open the appropriate language's json file and paste the content of the matching snippets file bellow:

![python-logo](images/python.png) [python.json](https://github.com/ilya0x/Templates-and-Snippets/blob/main/snippets/python.json)

![html5-logo](images/html5.png) [html.json](https://github.com/ilya0x/Templates-and-Snippets/blob/main/snippets/html.json)

![css3-logo](images/css3.png) [css.json](https://github.com/ilya0x/Templates-and-Snippets/blob/main/snippets/css.json)

![sass5-logo](images/sass-5.png) [sass.json](https://github.com/ilya0x/Templates-and-Snippets/blob/main/snippets/sass.json)

![markdown-logo](images/markdown.png) [markdown.json](https://github.com/ilya0x/Templates-and-Snippets/blob/main/snippets/markdown.json)

<!----------------------------------------------------------->

[//]: # "Templates"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Templates

![python-logo](images/python.png) Python:

- <i>generic</i>:
  - [main.py]()
  - [app.py]()
- Flask:
  - [run.py]()
  - [config.py]()
- Django:
  - [manage.py]() - This is a command-line utility to interact with the Django project.
  - [settings.py]() - Project settings.
  - [urls.py]() - Defines the app’s URL patterns.
  - [admin.py]() - Configures the Django admin interface for managing app models.
  - [apps.py]() - App configuration and metadata.
  - [models.py]() - Defines the app’s data models.
  - [views.py]() - Contains the views or controller functions for handling HTTP requests.
  - [forms.py]() - Includes form classes if the app requires custom forms.
- PyGame:
  - [game-name.py]()
- PySide6:
  - [appwindow.py]()
  - [main.py]()
- PyTorch:
  - [main.py]()
  - [model.py]()
  - TorchAudio:
    - [app.py]()
      <br>

![html5-logo](images/html5.png) HTML:

- <i>generic</i>:
  - [index-simple.html]()
  - [index-long.html]()
- Flask framework:
  - [base.html]()
  - [index.html]()
- Django framework:
  - [base.html]()
  - [header.html]()
  - [footer.html]()
    <br>

![css3-logo](images/css3.png) CSS:

- [styles.css](templates/styles/stylesheets/styles.css)
  <br>

![sass5-logo](images/sass-5.png) SASS:

- [template.sass](templates/style/sass/template.sass)
  <br>

![markdown-logo](templates/images/markdown.png) Markdown:

- [README.md](https://github.com/ilya0x/Templates-and-Snippets/blob/main/templates/markdown/README.md)
  - Setup according to [standard-readme](https://github.com/RichardLitt/standard-readme) standard style.

<!----------------------------------------------------------->

[//]: # "API"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

<!----------------------------------------------------------->

[//]: # "MAINTAINER"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Maintainer

[@ilya0x](https://github.com/ilya0x)

<!----------------------------------------------------------->

[//]: # "THANKS"
[STATUS]: # "Optional"
[NOTE]: # "Comments"

## Thanks

[@RichardLitt](https://github.com/RichardLitt) for the [standard-readme](https://github.com/RichardLitt/standard-readme) standard style creation.

<!----------------------------------------------------------->

[//]: # "CONTRIBUTING"
[STATUS]: # "Required"
[NOTE]: # "Comments"

<!----------------------------------------------------------->

[//]: # "LICENSE"
[STATUS]: # "Required"
[NOTE]: # "Comments"

## License

MIT License

SEE LICENSE IN <a href="https://github.com/ilya0x/Templates-and-Snippets/blob/main/LICENSE.txt">LICENSE.txt</a>

<!----------------------------------------------------------->
