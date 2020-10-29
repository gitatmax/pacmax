# Pacmax

Pacmax was assembled as a way for [Alfred](https://alfredapp.com) lovers to find and share their favorite workflows, snippets, and themes.
This repository outlines a few features such as the Pacmax Alfred Workflow, the API for creating your own Workflow or other contraptions, and more!

## The Pacmax Search Workflow

1. [Grab the latest release](https://github.com/maxwelljordanwhite/search-pacmax/releases)
2. Open it & select Import
3. You're all set!

### Usage

1. Trigger Alfred
2. Type either `pm` or `pacmax` followed by a <kbd>space</kbd>, the word you'd like to search for, and then <kbd>return</kbd>. E.g., `pm` + <kbd>space</kbd> + `spotify` + <kbd>return</kbd>. The results for your search will open in your default browser.

## Use the Pacmax API

In hopes of increasing the accessibility of Pacmax, I’ve opened up endpoints to the site’s REST API. They are few, but I think it will be incredibly valuable for anyone interested in querying Pacmax from in their projects.

### Parameters

The route for packages on Pacmax is /wp/v2/pacs and here are several usable parameters:

| Parameter            | Description                                                   |
|:---------------------|:--------------------------------------------------------------|
| `title`              | The package’s title                                           |
| `update_on`          | The last date the package was updated                         |
| `import_theme`       | If available, provides a path for one-click theme importing   |
| `author_username`    | The package author’s GitHub username                          |
| `author_name`        | The package author’s name                                     |
| `author_github_page` | The package author’s GitHub profile                           |
| `releases_zip_url`   | A link to download the latest release zipped                  |
| `download_url_master`| The most up to date source code                               |
| `stars`              | The number of Stars a package has                             |
| `repo_url`           | The package’s GitHub URL                                      |

### An Example Request

Here’s an example request to fetch 100 packages:

`GET https://pacmax.org/wp-json/wp/v2/pacs?_fields=title,update_on&_per_page=100`

## Add Pacmax to your browser

**As a search engine;** For Chrome (more to be confirmed): Add `https://pacmax.org/?_search=%` in Chrome (more browsers to be confirmed) at [chrome://settings/searchEngines](chrome://settings/searchEngines)

**As a Bookmarklet;** Copy the following and paste it into a new bookmarkjavascript: `javascript:(function()%7Bif%20(window.location.hostname%20%3D%3D%20%22github.com%22)%7B%0A%20%20%20%20var%20url%20%3D%20document.URL%3B%0A%20%20%20%20var%20baseUrl%20%3D%20%20'https%3A%2F%2Fpacmax.org%2Fsubmit-repo%2F'%3B%0A%20%20%20%20window.open(baseUrl%20%2B'%3Frepo_url%3D'%20%2B%20document.URL%2C%20'_blank')%3B%0A%0A%7Delse%20if%20(window.location.hostname%20%3D%3D%20%22pacmax.org%22)%7B%0A%7D%0Aelse%20%7B%0A%20%20%20%20alert('Sorry%2C%20Pacmax%20Bookmarket%20%2C%20Works%20only%20on%20Github%20Repo%20home')%3B%0A%7D%0Aconsole.log(%22Pacmax%20Bookmarket%20-%20V.1.0%22)%3B%7D)()%3B`

## Contribute [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Have an idea that'd improve this project? I'm all ears! Issues and pull requests welcome.

## License

MIT License © Maxwell Jordan White
