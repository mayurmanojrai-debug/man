SHREE KRISHNA EDUTECH — RENDER-SAFE VERSION
==============================================

This package fixes the broken-image problem visible after deployment.

What was fixed:
- Logo and hero image are embedded directly in index.html, so they do not depend on Render resolving the assets folder.
- Course SVGs are embedded directly in index.html.
- Gallery cards using third-party image hosts now have a local fallback instead of becoming broken images.
- Original assets folder is still included for backup/future editing.

RENDER SETTINGS
---------------
For a Render Static Site:
- Root Directory: the folder containing index.html
- Build Command: leave blank
- Publish Directory: .

If deploying from GitHub, make sure index.html, style.css, script.js and the complete assets folder are committed and pushed.

The screenshot issue was caused by the browser displaying image ALT text, which means the image URL could not be loaded. The large text beginning “Students learning technology...” in the hero is the image's ALT text, not part of the design.
