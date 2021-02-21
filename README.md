<img src="pacmax-github-banner.png"/>

Pacmax was initially a way for lovers of [Alfred](https://alfredapp.com) to find and share their favorite workflows, snippets, and themes. It's since begun to cover more ground by adding more support for other extensions to more applications (often referred collectively here and on [Pacmax](https://pacmax.org/) as "Pacs". Read on for info on how to make use of the site's REST API, how to leave feedback, among other things!

## API

The Pacmax REST API is for anyone who'd like to work with the data points across the site.

### Parameters

The route for packages on Pacmax is `/wp/v2/pacs`. There are several usable parameters that [I](https://github.com/gitatmax/) am looking forward to adding to:

| Parameter           	| Description (package reduced to "Pac")   |
|:--------------------|:----------------------------------------------|
| `title`                    | The Pac’s title                                             |
| `update_on`          | The last date the Pac was updated            |
| `import_theme`    | One-click theme import (when available)  |
| `author_username`    | The Pac author’s GitHub username       |
| `author_name`      | The Pac author’s name                                |
| `author_github_page` | The Pac author’s GitHub profile           |
| `releases_zip_url`   | A link to download the latest release zipped |
| `download_url_master`| The most up to date source code |
| `stars`              | The number of Stars a Pac has |
| `repo_url`           | The Pac’s GitHub URL |

#### An Example Request

This example should return 100 responses, each with a title & a date it was last  updated:

`GET https://pacmax.org/wp-json/wp/v2/pacs?_fields=title,update_on&_per_page=100`

## Use the Alfred Workflow

### Setup

1. [Grab the latest release](https://github.com/maxwelljordanwhite/search-pacmax/releases)
2. Open it & select Import
3. You're all set! See Usage below.

### Usage

1. Trigger Alfred
2. Type `pm` or `pacmax` followed by a <kbd>space</kbd>
3. Type you'd like to search for (e.g. "Spotify")
4.  Lastly, smash (gently) <kbd>return</kbd>. The results of your search will open in your browser. 🙌

## Add Pacmax as a Search Engine in Your Browser

Using Google Chrome as an example, add `https://pacmax.org/?_search=%` in Chrome at [chrome://settings/searchEngines](chrome://settings/searchEngines)

## Submit a GitHub Repository to Pacmax With a Bookmarklet
Copy the following and paste it into a new bookmark:

```
javascript:(function()%7Bjavascript%3A%20(function%20()%20%7B%0A%20%20if%20(window.location.hostname%20%3D%3D%20%22github.com%22)%20%7B%0A%20%20%20%20var%20url%20%3D%20document.URL%3B%0A%20%20%20%20var%20baseUrl%20%3D%20%22https%3A%2F%2Fpacmax.org%2Fsubmit-repo%2F%22%3B%0A%20%20%20%20window.open(baseUrl%20%2B%20%22%3Frepo_url%3D%22%20%2B%20document.URL%2C%20%22_blank%22)%3B%0A%20%20%7D%20else%20if%20(window.location.hostname%20%3D%3D%20%22pacmax.org%22)%20%7B%0A%20%20%7D%20else%20%7B%0A%20%20%20%20alert(%22Sorry%2C%20this%20only%20works%20with%20GitHub%20repositories%22)%3B%0A%20%20%7D%0A%20%20console.log(%22Pacmax%20Bookmarket%20-%20V.1.0%22)%3B%0A%7D)()%3B%7D)()%3B
```

## Contribute

Have an idea that'd improve this project? I'm all ears! Issues and pull requests welcome.

## License

[MIT License © Maxwell Jordan White](LICENSE.md)
