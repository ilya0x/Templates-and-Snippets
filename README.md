[//]: # "TITLE"

# Templates and Snippets _(Templates-and-Snippets)_

<!----------------------------------------------------------->

[//]: # "BANNER"

![banner](images/banner.png)

<!----------------------------------------------------------->

[//]: # "BADGES"

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)
[![MIT-license](https://img.shields.io/badge/License-MIT-brightgreen.svg?style=flat-square)](https://github.com/ilya0x/Templates-and-Snippets/blob/main/LICENSE.txt)

<!----------------------------------------------------------->

[//]: # "SHORT DESCRIPTION"

Templates and snippets for Python, Mojo, HTML, CSS, SASS, and Markdown.

<br>

> This repository is updated on regular basis.

> Added: `notes.md` in each [templates](templates/) folder with ideas for
> snippets and templates content, with some notes on each language.

<h3>Todo</h3>

- [ ] Separate each language into its own repository of notes, templates and
  snippets. Link language icons on profile to corresponding repository.
- [ ] Add YAML templates and snippets

<br>

<!----------------------------------------------------------->

[//]: # "LONG DESCRIPTION"

<!----------------------------------------------------------->

[//]: # "TABLE OF CONTENTS"

<h2>Table of Contents</h2>

- [Templates and Snippets _(Templates-and-Snippets)_](#templates-and-snippets-templates-and-snippets)
  - [Background](#background)
  - [Install](#install)
  - [Usage](#usage)
  - [Snippets](#snippets)
  - [Templates](#templates)
  - [Security](#security)
  - [Maintainer](#maintainer)
  - [Thanks](#thanks)
  - [License](#license)

<!----------------------------------------------------------->

[//]: # "BACKGROUND"

## Background

Python programmers tend to not enjoy working with HTML and CSS - and who can
blame them? Most of it is reused from project to project with just some basic
changes. Intensive HTML and CSS work is for designers, not programmers. Inspired
by [@NeuralNine](https://github.com/NeuralNine)'s and others dislike of HTML and
CSS, this repository will grow to contain as many useful HTML, CSS and SASS
templates as possible.

[Emmet](https://docs.emmet.io) is a great web-developer’s toolkit that takes the
snippets idea to a whole new level. This project's goal is to expand on Emmet
snippets to eliminate as much HTML and CSS work as possible, maximizing Python
programmers' use of time on actually programming in Python.

To further facilitate fast Python programming, there is an ever-expanding list
of Python templates for various frameworks and modules. As I expand my
repertoire, I will be adding additional templates to the collection.

I have also just added [Mojo](https://www.modular.com/mojo) templates to this
collection. As I learn the Mojo language I will be adding more templates and
snippets for it.

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!--------------------------------------------------->

[//]: # "INSTALL"

## Install

This project does not require any additional installations.

> I use and recommend Visual Studio Code

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "USAGE"

## Usage

This is only a documentation, templates, and code snippets package.

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "Snippets"

## Snippets

Go to `Settings -> User Snippets`, open the appropriate language's json file and
paste the content of the matching snippets file bellow:

![css3-logo](images/css3.png) [css.json](snippets/css.json)

![html5-logo](images/html5.png) [html.json](snippets/html.json)

![markdown-logo](images/markdown.png) [markdown.json](snippets/markdown.json)

🔥 [mojo.json](snippets/mojo.json)

> [Mojo🔥](https://www.modular.com/mojo) — the programming language for all AI developers

![python-logo](images/python.png) [python.json](snippets/python.json)

![sass5-logo](images/sass-5.png) [sass.json](snippets/sass.json)

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "Templates"

## Templates

- All templates include extensive notes about each line of code and what is
  required to be entered/edited by the user.
- Each template can be called via its Snippet; the snippets do not contain the
  extensive notes and automatically take the cursor to the sections requiring
  input from user.

![html5-logo](images/html5.png) HTML:

- <i>generic</i>:
  - [index-simple.html](templates/html/generic/index-simple.html)
  - [index-long.html](templates/html/generic/index-long.html)
- Flask framework:
  - [base.html](templates/html/flask/base.html)
  - [index.html](templates/html/flask/index.html)
- Django framework:
  - [base.html](templates/html/django/base.html)
  - [header.html](templates/html/django/header.html)
  - [footer.html](templates/html/django/footer.html)
    <br>

![css3-logo](images/css3.png) CSS:

- [styles.css](templates/styles/stylesheets/styles.css)
  <br>

![sass5-logo](images/sass-5.png) SASS:

- [template.sass](templates/style/sass/template.sass)
  <br>

![markdown-logo](images/markdown.png) Markdown:

- [README.md](templates/markdown/README.md) - Setup according to
  [standard-readme](https://github.com/RichardLitt/standard-readme) standard
  style, including NOTES. <br>

![python-logo](images/python.png) Python:

- <i>generic</i>:
  - [main.py](templates/python/generic/main.py)
  - [app.py](templates/python/generic/app.py)
- Flask:
  - [run.py](templates/python/flask/run.py)
  - [config.py](templates/python/flask/config.py)
- Django:
  - [manage.py](templates/python/django/manage.py) - This is a command-line
    utility to interact with the Django project.
  - [settings.py](templates/python/django/settings.py) - Project settings.
  - [urls.py](templates/python/django/urls.py) - Defines the app’s URL patterns.
  - [admin.py](templates/python/django/admin.py) - Configures the Django admin
    interface for managing app models.
  - [apps.py](templates/python/django/apps.py) - App configuration and metadata.
  - [models.py](templates/python/django/models.py) - Defines the app’s data models.
  - [views.py](templates/python/django/views.py) - Contains the views or
    controller functions for handling HTTP requests.
  - [forms.py](templates/python/django/forms.py) - Includes form classes if the
    app requires custom forms.
- PyGame:
  - [game-name.py](templates/python/pygame/game-name.py)
- PySide6:
  - [appwindow.py](templates/python/pyside6/appwindow.py)
  - [main.py](templates/python/pyside6/main.py)
- PyTorch:
  - [main.py](templates/python/pytorch/main.py)
  - [model.py](templates/python/pytorch/model.py)
  - TorchAudio:
    - [app.py](templates/python/pytorch/torchaudio/app.py)
      <br>

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "SECURITY"

## Security

- Templates contain placeholder IP addresses and ports. You will need to replace
  them for your specifications.
- Same goes for placeholder usernames and passwords.

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "API"

<!----------------------------------------------------------->

[//]: # "MAINTAINER"

## Maintainer

[@ilya0x](https://github.com/ilya0x)

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "THANKS"

## Thanks

[@RichardLitt](https://github.com/RichardLitt) for the
[standard-readme](https://github.com/RichardLitt/standard-readme) standard style
creation.

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->

[//]: # "CONTRIBUTING"

<!----------------------------------------------------------->

[//]: # "LICENSE"

## License

MIT License

SEE LICENSE IN <a href="https://github.com/ilya0x/Templates-and-Snippets/blob/main/LICENSE.txt">LICENSE.txt</a>

<br>
<br>

[Back to Table of Contents](#table-of-contents)
<br>
<br>

<!----------------------------------------------------------->
