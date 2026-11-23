# Portfolio v1

Personal portfolio of Maxence Bonamy.

Static website presenting the author and a list of personal programming projects, each with an animated preview and the technologies it uses. This is the first version of the portfolio and is not hosted anywhere.

## Table of contents

- [Portfolio v1](#portfolio-v1)
	- [Table of contents](#table-of-contents)
	- [How it works](#how-it-works)
	- [Tech stack](#tech-stack)
	- [Repository structure](#repository-structure)
	- [Prerequisites](#prerequisites)
	- [Installation](#installation)
	- [Running locally](#running-locally)
	- [Useful scripts](#useful-scripts)
	- [License](#license)

## How it works

1. **Home**: `index.html` shows the title and a canvas animation (plasma effect) drawn by `js/plasma.js`.
2. **Projects**: `projects.html` lists 12 projects. Each card has a GIF preview, the technologies used and a link to its GitHub repository.
3. **Contact**: `contact.html` gives a short presentation and links to GitHub, Instagram, Facebook, LinkedIn, Twitter and e-mail.
4. **Legal notice**: `legal.html` contains the legal information of the site.
5. **Navigation**: the menu is shared by all pages. On small screens, `js/menu.js` toggles it with a `clicked` class on the `body`.

## Tech stack

| Layer | Technologies |
| --- | --- |
| Pages | HTML |
| Styles | SCSS compiled to CSS (`css/style.css`) |
| Scripts | JavaScript (Canvas API, no dependency) |
| Icons | Font Awesome (loaded from its kit, requires a network connection) |
| Assets | WebP images, GIF previews, local fonts (`Klik-Light`, `Miedinger`) |

## Repository structure

```
.
├── assets/
│   ├── font/           Local fonts
│   ├── gif/            Project previews
│   └── img/            Pictures and technology icons
├── css/                SCSS sources and compiled style.css
├── js/
│   ├── menu.js         Mobile menu toggle
│   └── plasma.js       Canvas background animation
├── index.html          Home
├── projects.html       Projects
├── contact.html        Contact
└── legal.html          Legal notice
```

SCSS is split by concern (`util`, `menu`, `button`, `section`, `glitch`) and imported from `css/style.scss`. The pages load the compiled `css/style.css`, which is committed.

## Prerequisites

- A web browser
- [Sass](https://sass-lang.com/install) only if you edit the `.scss` files

## Installation

```bash
git clone git@github.com:maxencebonamy/Portfolio-V1.git
cd Portfolio-V1
```

There are no dependencies to install.

## Running locally

Open `index.html` in a browser, or serve the folder with any static server, for example:

```bash
python3 -m http.server 8000
```

The site is then available at <http://localhost:8000>.

## Useful scripts

The repository has no package manager or script file. The only build step is the SCSS compilation:

| Command | Effect |
| --- | --- |
| `sass css/style.scss css/style.css` | Compile the styles |
| `sass --watch css/style.scss css/style.css` | Recompile on every change |

## License

This project is licensed under the [MIT License](LICENSE).
