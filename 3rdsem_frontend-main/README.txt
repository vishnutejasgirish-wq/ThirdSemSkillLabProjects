DAY 1 DEMOS - Web Foundations & Git
====================================

HOW TO RUN
- Open the 3rdsem folder in VS Code.
- Right-click index.html -> "Open with Live Server"
  (no Live Server? Right-click -> Open Containing Folder -> double-click index.html)
- To explain: show the page in the browser AND the same file in VS Code side by side.
- Each file has "TRY THIS" comments: change that line, Ctrl+S, refresh.

WHICH DEMO GOES WITH WHICH SLIDE
01-skeleton-skin-brain.html  -> Skeleton, Skin, Brain   (delete <style> / onclick)
02-html-elements.html        -> Eight tags + Semantic tags
03-forms.html                -> Forms (submit empty, type "abc" as email)
04-css-three-ways.html       -> A CSS rule / three ways (needs 04-external.css)
05-selectors.html            -> Selectors
06-specificity.html          -> Specificity battle (delete rules one by one)
07-box-model.html            -> Box model + box-sizing
08-flexbox-playground.html   -> Flexbox (change justify-content, align-items)
09-responsive.html           -> Responsive + Squeeze test (pink = phone, blue = laptop)
10-display-position.html     -> display vs visibility, relative vs absolute
11-grid-vs-flex.html         -> Grid vs Flexbox
12-bootstrap.html            -> Bootstrap (needs internet)
spot-the-bug.html            -> Spot the bug
portfolio/                   -> finished portfolio (answer key for 4:30)

SPOT-THE-BUG ANSWERS (don't show students)
1. <link href="styles.css">  -> file doesn't exist (404 in Network tab). No CSS loads.
2. href="#Projects" but id="projects"  -> ids are case-sensitive, link doesn't jump.
3. <img> has no alt text.
4. <label for="mail"> but <input id="email">  -> clicking the label does nothing.

GIT DEMO (run inside a COPY of the portfolio folder)
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  git config --global init.defaultBranch main
  git init
  git status
  git add .
  git commit -m "Add profile page structure and styles"
  git log --oneline
  (edit the h1) -> git status -> git diff -> git add . -> git commit -m "Update heading"
  git branch feature-dark-theme
  git checkout feature-dark-theme
  (add to style.css:  body { background: #111827; color: white; })
  git add .
  git commit -m "Add dark colour theme"
  git checkout main                 <- refresh browser: dark theme disappears
  git checkout feature-dark-theme   <- refresh: it comes back
  git checkout main
  git merge feature-dark-theme
  git log --oneline
