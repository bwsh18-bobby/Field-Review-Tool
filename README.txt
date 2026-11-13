PAVEMENT REVIEW — ONE LINK FOR ALL PROJECTS
============================================

This folder is a small website:
  index.html                 the project picker (the link you share)
  <city>_pavement_review.html  one map per city

PUT IT ONLINE (pick one)
------------------------
A) Netlify Drop (quickest, free):
   1. Go to https://app.netlify.com/drop and sign in (free account keeps the site permanent).
   2. Drag this whole folder onto the page.
   3. Copy the link it gives you (you can rename it under Site settings → Change site name).
   To update later: open the site in Netlify → Deploys → drag the folder again. The link stays the same.

B) GitHub Pages (free):
   1. Create a repository, upload all files in this folder (Add file → Upload files).
   2. Settings → Pages → Source: "Deploy from a branch", branch "main", folder "/ (root)" → Save.
   3. The link appears at the top of the Pages settings after a minute.

C) Your organization's web server: copy the folder to any location it serves as a normal web page.
   (SharePoint document libraries and Google Drive usually download .html files instead of showing them.)

Share only the index.html link. Everyone opens the same link, picks a city, and the ☰ button in
each map returns to the list.

REVIEWS
-------
Reviews are saved in each person's browser, separately per project. The online link is a different
place from a downloaded copy of a map, so to move reviews from a downloaded file:
open the old file → 📁 Data → Export JSON, then open the project from the link → 📁 Data → Import JSON.
Updating the files on the website does not erase anyone's reviews, as long as the file names stay the same.

ADDING OR UPDATING A CITY
-------------------------
Ask Claude (with the pavement-review-map skill) to build the city's map for the site, or run:
  python build_map.py <city shapefile> --city "<City>" --projects-link index.html --out <this folder>/<city>_pavement_review.html
  python build_site.py <this folder>
then upload the folder again.
