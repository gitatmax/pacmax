# Pacmax Search

<img src="icon.png" width="100px" title="Search Pacmax">

Pacmax was assembled as a way for [Alfred](https://alfredapp.com) lovers to find and share their favorite workflows, snippets, and themes.
With this workflow you can quickly get to and filter results on Pacmax's Explore page!

## Setting Up

1. [Grab the latest release](https://github.com/maxwelljordanwhite/search-pacmax/releases)
2. Open it & select Import
3. You're all set!

## Usage

1. Trigger Alfred
2. Type either `pm` or `pacmax` followed by a <kbd>space</kbd>, the word you'd like to search for, and then <kbd>return</kbd>. E.g., `pm` + <kbd>space</kbd> + `spotify` + <kbd>return</kbd>. The results for your search will open in your default browser.

## Make Your Own

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

### Example Request

Here’s an example request to fetch 100 packages:

`GET https://pacmax.org/wp-json/wp/v2/pacs?_fields=title,update_on&_per_page=100`

## Contribute [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Have an idea that'd improve this project? I'm all ears! Issues and pull requests welcome.

## License

MIT License © Maxwell Jordan White
