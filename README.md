# Tracking your Resume on Git
### Pros 
- I saw someone else do it and it's way better than how I have been doing this
- allows for version control
- no need for apps like Word or Google Docs, edit on any text editor
- Actual layout control with HTML and CSS
- Allows PR's for external recomendations
### Cons 
- No immediate sharing of the document
- No live sharing of layout and presentation
- Not available to edit on mobile
- Email and phone open to the public (hate those pesky IRS spam calls, bless google phone screening)

## Technologies
- javascript/npm (not yarn), loose versions
- webpack
- html
- scss
- react? will having HTML suffice for static hosting too?
- github pages for hosting and downloading PDF. 

## Architecture
```
+-------------+                         +--> Github Pages publish 
| React(HTML) |       +---------+       |     (HTTPS, CDN)
| SCSS        | --->  | Webpack | ------+--> Static Minified Assets
| JSON        |       +---------+       |
+-------------+                         +--> PDF
                                        +--> Headless Chrome Screenshot
```

## Phase 1:
- [ ] Upload PDF from Google Docs and push up into GitHub.
- [ ] Obtain download link of said PDF and add into teikmeout.com.
- [ ] Obtain view link of said PDF.
- [ ] Create HTML file that displays this document with the view link of the PDF.
- [ ] Deploy to Github pages.

## Phase 2:
- [ ] create JSON for resume values.
- [ ] create HTML + CSS version of resume using react + webpack.
- [ ] create webpack script to create PDF.
- [ ] create webpack script to run a chromium headless browser and create a screenshot of resume.

### Scripts
- `start`: run development server
- `build`: build static assets and push into branch for Github Pages to use
- `build:pdf`: run webpack script to build PDF from static site
- `deploy`: run build script and 
- `pre-commit`: run a linting process
- `post-commit`: run a commit naming checker
