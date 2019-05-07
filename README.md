# ![LOGO](logo.png) Movie Reviews **flow**ground Connector

## Description

A generated **flow**ground connector for the Movie Reviews API (version 2.0.0).

Generated from: https://api.apis.guru/v2/specs/nytimes.com/movie_reviews/2.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:20+03:00

## API Description

With the Movie Reviews API, you can search New York Times movie reviews by keyword and get lists of NYT Critics' Picks.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### get_critics__resource_type__json

#### Input Parameters
* `resource-type` - _required_ - all | full-time | part-time | [reviewer-name]

Specify all to get all Times reviewers, or specify full-time or part-time to get that subset. Specify a reviewer's name to get details about a particular reviewer.


### get_reviews_search_json

#### Input Parameters
* `query` - _optional_ - Search keywords; matches movie title and indexed terms

To limit your search to exact matches only, surround your search string with single quotation marks (e.g., query='28+days+later'). Otherwise, responses will include partial matches ("head words") as well as exact matches (e.g., president will match president, presidents and presidential).
  
  If you specify multiple terms without quotation marks, they will be combined in an OR search.
  
  If you omit the query parameter, your request will be equivalent to a reviews and NYT Critics' Picks request.

* `critics-pick` - _optional_ - Set this parameter to Y to limit the results to NYT Critics' Picks. To get only those movies that have not been highlighted by Times critics, specify critics-pick=N. (To get all reviews regardless of critics-pick status, simply omit this parameter.)

    Possible values: Y, N.
* `reviewer` - _optional_ - Include this parameter to limit your results to reviews by a specific critic. Reviewer names should be formatted like this: Manohla Dargis.

* `publication-date` - _optional_ - Single date: YYYY-MM-DD

Start and end date: YYYY-MM-DD;YYYY-MM-DD

The publication-date is the date the review was first published in The Times.

* `opening-date` - _optional_ - Single date: YYYY-MM-DD

Start and end date: YYYY-MM-DD;YYYY-MM-DD

The opening-date is the date the movie's opening date in the New York region.

* `offset` - _optional_ - Positive integer, multiple of 20
* `order` - _optional_ - Sets the sort order of the results.

Results ordered by-title are in ascending alphabetical order. Results ordered by one of the date parameters are in reverse chronological order.

If you do not specify a sort order, the results will be ordered by publication-date.


### get_reviews__resource_type__json

#### Input Parameters
* `resource-type` - _required_ - Specify all to retrieve all reviews, including NYT Critics' Picks.

Specify picks to get NYT Critics' Picks currently in theaters.


    Possible values: all, picks.
* `offset` - _optional_ - Positive integer, multiple of 20
* `order` - _optional_ - Sets the sort order of the results.

Results ordered by-title are in ascending alphabetical order. Results ordered by one of the date parameters are in reverse chronological order.

If you do not specify a sort order, the results will be ordered by publication-date.

    Possible values: by-title, by-publication-date, by-opening-date.

## License

**flow**ground :- Telekom iPaaS / nytimes-com-movie-reviews-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
