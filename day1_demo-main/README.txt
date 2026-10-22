DAY 1 DEMOS - Web Foundations & Git
====================================

HOW TO RUN
- Open the day1-demos folder in VS Code.
- Right-click index.html -> "Open with Live Server" (or just double-click any file).
- index.html links to every demo in teaching order.
- Only 12-bootstrap.html and the picsum.photos images need internet.

WHICH DEMO GOES WITH WHICH SLIDE
01-skeleton-skin-brain.html  -> "Skeleton -> Skin -> Brain"  (buttons switch CSS and JS off)
02-html-elements.html        -> "Eight tags" + "Semantic tags" (coloured outlines show each area)
03-forms.html                -> "Forms" (submit it empty or with a bad email)
04-css-three-ways.html       -> "A CSS rule" (inline / internal / external; needs 04-external.css)
05-selectors.html            -> "Selectors" (click a selector, matching elements light up)
06-specificity.html          -> "Specificity battle" (tick rules on/off)
07-box-model.html            -> "Box model" + "box-sizing" (sliders, live width maths)
08-flexbox-playground.html   -> "Flexbox" (drop-downs for every property)
09-responsive.html           -> "Responsive" + "Squeeze test" (header turns red/orange/blue at 600px / 900px)
10-display-position.html     -> "Three pairs" (display vs visibility, relative vs absolute)
11-grid-vs-flex.html         -> "Three pairs" (Grid vs Flexbox)
12-bootstrap.html            -> "Bootstrap"
spot-the-bug.html            -> "Spot the bug" (4 bugs, answers in the code comments)
portfolio/                   -> the finished portfolio students should reach by 4:30

GIT DEMO (run inside a COPY of the portfolio folder)
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  git config --global init.defaultBranch main
  git init
  git status
  git add .
  git commit -m "Add profile page structure and styles"
  git log --oneline
  (edit the h1) -> git status -> git diff -> git add . -> git commit -m "Update heading with role"
  git branch feature-dark-theme
  git checkout feature-dark-theme
  (add to style.css:  body { background:#111827; color:#e5e7eb; }  .card { background:#1f2937; border-color:#374151; })
  git add .
  git commit -m "Add dark colour theme"
  git checkout main                 <- refresh browser: dark theme disappears
  git checkout feature-dark-theme   <- refresh: it comes back
  git checkout main
  git merge feature-dark-theme
  git log --oneline
