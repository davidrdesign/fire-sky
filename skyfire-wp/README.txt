SKYFIRE LANDING PAGE — WORDPRESS INSTALLATION
=============================================

WHAT'S IN THIS PACKAGE
-----------------------
  skyfire-landing.php   Full-page WordPress page template
  README.txt            This file

REQUIREMENTS
------------
  - WordPress 5.0 or later
  - Any active theme (classic or block)

HOW TO INSTALL
--------------
1. Copy skyfire-landing.php into your active theme folder.
   Example paths:
     wp-content/themes/your-theme/skyfire-landing.php
     wp-content/themes/your-child-theme/skyfire-landing.php

2. In WordPress Admin, go to Pages → Add New (or open an existing page).

3. In the right sidebar under "Page Attributes", set Template to
   "Skyfire Landing Page".

4. Publish or update the page.

5. Visit the page — it will render as a full-screen standalone experience,
   completely independent of your theme's header and footer.

NOTES
-----
- The template is fully self-contained. All styles and scripts are inline;
  no additional files are needed.
- The only external dependencies are Google Fonts (Inter, Geist, JetBrains
  Mono), which load from the network. The page degrades gracefully
  if fonts are unavailable.
- No plugins required.

EDITING
-------
All content lives in skyfire-landing.php. The hero copy is inside
<header class="hero">. The two SVG diagrams are searched via
class="hero-svg" and class="access-svg". The live demo animation
is in the <script> block near the bottom of the file.
