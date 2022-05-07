# Pacmax

## [Please support Ukraine](https://www.unicefusa.org/stories/unicef-children-are-bearing-brunt-intensifying-crisis-ukraine/39481?form=FUNKBHMZQDQ&utm_content=Ukraine2&ms=cpc_dig_2021_Ukraine2_20210801_google_Ukraine2_delve_None&initialms=cpc_dig_2020_Ukraine2_20210801_google_Ukraine2_delve_None) 🇺🇦

Pacmax was originally a place for folks to explore & share their favorite extensions of the lovely [Alfred](https://alfredapp.com) application. It's expanded & changed shape but has always kept to its mission of raising awareness of cool add-ons for all sorts of applications. Why's this repository empty, now? A lot is coming, so check back before long for more information here on all of the ways you can interact with Pacmax!

## REST API

You can interact with Pacmax's by querying the REST API. It's early days, but I'm excited to see what you all will do with it. The root of the API can be found at https://pacmax.org/api/pacs, but we can get more specific results by drilling down into various metadata; here's what I've enabled so far: 

_Again, this is a work-in-progress—much of this will probably be revised._

To start, all of the "Pacs" (essentially categories on the site) have some overlapping items:

* `post_title`
* `permalink`

Then, we have our Pac-specific items:

* [`/alfred-workflows`](https://pacmax.org/api/alfred-workflows) (_Many of these fields are being made available to all categories very soon_)
  * `repo_url`; the URL of the project on GitHub
  * `author_username`; the author's GitHub Username
  * `releases_zip_url`; The URL to the project's latest zipped release
  * `stars`; How many Stars the project has on GitHub
  * `update_on`; When the GitHub repository was last updated
* [`/siri-shortcuts`](https://pacmax.org/api/pacs/siri-shortcuts)
  * `siri_shortcut_info`; About the Shortcut
  * `siri_shortcut_url`; The URL for grabbing the Shortcut
* [`/userscripts`](https://pacmax.org/api/pacs/userscripts)
