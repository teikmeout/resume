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
- github pages for hosting?

## Architecture
```
+-------------+                         +--> Github Pages publish 
| React(HTML) |       +---------+       |     (HTTPS, CDN)
| SCSS        | --->  | Webpack | ------+--> Static Minified Assets
| JSON        |       +---------+       |
+-------------+                         +--> PDF
                                        +--> Headless Chrome Screenshot
```

## Expected Functionality
- [ ] written in react, scss?? maybe just html and scss...
- [ ] uses webpack to spit out static website and/or PDF
- [ ] uses Chrome headless to implement screenshot image of resume and push into assets

## Scripts
- `start`: run development server
- `build`: build static assets and push into branch for Github Pages to use
- `build:pdf`: run webpack script to build PDF from static site
- `deploy`: run build script and 
- `pre-commit`: run a linting process
- `post-commit`: run a commit naming checker

