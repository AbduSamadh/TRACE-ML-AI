Trace - files to publish

Upload everything in this folder, keeping the layout, to any static web host
that serves over https (GitHub Pages, Netlify, Cloudflare Pages, a school
web server). index.html is the page; models/ holds the pose and hand models
so the page never fetches anything from another site.

Include the hidden file .nojekyll: on GitHub Pages it stops the site
generator from skipping files. To check the upload, open
<your site>/models/pose/model.json - it should show text, not a 404.
If models/ is missing the page still works, using the public copy instead;
add ?debug to the address to see which copy it used.

It must be served over https (or from localhost). Browsers refuse the
camera to a page opened straight from disk, and to plain http.

The camera also needs the page to have its own address: embedded inside
another site's frame, only the Drawing model will work.
