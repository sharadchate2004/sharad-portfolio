# Portfolio Website

A responsive, single-page portfolio built with plain HTML, CSS and JavaScript. No build tools, no frameworks, no installs.

## Run it in Visual Studio Code

1. Unzip the folder and open it in VS Code (`File > Open Folder`).
2. Install the **Live Server** extension (by Ritwick Dey).
3. Right-click `index.html` and choose **Open with Live Server**.

You can also just double-click `index.html` to open it in a browser.
(Python alternative: run `python -m http.server 8000` in this folder and visit http://localhost:8000.)

## Folder structure

```
portfolio/
├── index.html          all page content (text, links, sections)
├── css/style.css       all styling; colours and fonts are variables at the top
├── js/main.js          nav, scroll animations, image slider, contact form
├── assets/
│   ├── images/         profile.svg, project-1..3.svg (placeholders)
│   └── resume.pdf      placeholder: replace with your resume
└── README.md
```

## Editing your content

| To change...            | Edit...                                                       |
|-------------------------|---------------------------------------------------------------|
| Name, headline, bio     | `index.html` (search for "Your Name" and each section's text) |
| Email, LinkedIn, GitHub | `index.html`, `#contact` section, and `RECEIVER` in `js/main.js` |
| Profile photo           | Save as `assets/images/profile.jpg`, then change the `src` in the hero `<img>` |
| Project cards           | Copy/paste an `<article class="card project">` block in `#projects` |
| Project screenshots     | Put images in `assets/images/` and update each `<img src>` |
| Skills                  | The `<li>` items inside `#skills`                             |
| Experience timeline     | The `<li>` items inside `#experience`                         |
| Resume                  | Replace `assets/resume.pdf` (keep the same file name)         |
| Colours / fonts         | The `:root { ... }` variables at the top of `css/style.css`   |
| Animation speed         | The `transition` and `animation` values in `css/style.css`    |

## Making the contact form send email

The form currently opens the visitor's email app with the message filled in (works anywhere, needs no server). To receive messages directly, create a free form at formspree.io or web3forms.com, then set the form's `action` and `method="POST"` in `index.html` and remove the `submit` handler in `js/main.js`.

## Deploying

Drag the folder onto Netlify Drop, or push it to GitHub and enable GitHub Pages.
