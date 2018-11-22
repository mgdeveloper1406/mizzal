# Missal.io

![build status](https://travis-ci.org/benyanke/missal.io.svg)

## Important Note
Note that all the texts have not yet been transcribed. Additionally, the API interface may 
break at any time during development, though it is mostly finalized. It will later be formalized
and documented when development and transcription is complete.

Track [this thread](https://github.com/benyanke/missal.io/issues/24) if you wish to get updates on these changes.


## Goals
This is a backend data project designed to put the content of the 1962 (and older) Roman Missals
and the translations into a usable datastructure to be called as an api. 

The primary focus will always be the /api directory as a backend datasource for other projects,
there will also be a simple frontend app using the backend data as an example of what is possible.

An example client of this backend is available at http://missal.io.

## Builds
Currently, builds only verify that every json file in the repo is valid json. In the future, there are plans to ensure the
content is valid and linted as well. 

Example linting rules might include:
 * no trailing spaces at the end of a string
 * ensure that non-optional fields are not blank
 * ensure that multi-line texts (like hymns) have the same number of lines in every provided language
 * ensure the text-block category is one of the pre-approved ones (collect, introit, offertory, etc)
 * Ensure no newline characters

Also, consider putting all files through a json formatter so that the final files in gh-pages branch look consistent.

Additionally, the index should be created in the future by the builds process, and possibly even a static
HTML frontend based on the backend, which would then be auto-committed to the gh-pages branch. In this future 
scheme, the gh-pages branch would not be manually updated, but rather generated by builds from the data branch.

## Roadmap

 * Add unreformed holyweek - and find a good way to denote this in the datastructure (perhaps add a missal-edition tag)
 * Cleanup example app at missal.io - currently it does not handle non-standard liturgies well
