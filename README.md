CLI for GitHub user contrib graph & language stats

[This tool is intended to facilitate the archiving of your public data hosted on GitHub](https://help.github.com/articles/github-terms-of-service/#5-scraping).

Currently supports:

 * User's contributions graph.
 * User's language statistics.
 * User's yearly contributions count.

### Install

	pip install thxgh

(hint: use `--user` to install into `~/.local/bin/`)

### Run

See usage help:

	$ ./bin/thxgh 
	Usage: ./bin/thxgh [--contributions|--stats] github-username
		--contributions will print the SVG contributions graph to stdout.
		--stats will print JSON formatted statistics for the user to stdout.

Download contributions graph SVG for a user:

	$ ./bin/thxgh --contributions chr15m > chr15m-contributions.svg

Get language statistics for a user:

	$ ./bin/thxgh --stats chr15m
	{
	  "languages": [
	    {
	      "count": 29, 
	      "percent": 23, 
	      "language": "JavaScript"
	    }, 
	    {
	      "count": 24, 
	      "percent": 19, 
	      "language": "PureData"
	    }, 
	    {
	      "count": 17, 
	      "percent": 14, 
	      "language": "Python"
	    }, 
	    {
	      "count": 15, 
	      "percent": 12, 
	      "language": "Clojure"
	    }, 
	    {
	      "count": 10, 
	      "percent": 8, 
	      "language": "C"
	    }, 
	    {
	      "count": 6, 
	      "percent": 5, 
	      "language": "Hy"
	    }, 
	    {
	      "count": 4, 
	      "percent": 3, 
	      "language": "Java"
	    }, 
	    {
	      "count": 4, 
	      "percent": 3, 
	      "language": "PHP"
	    }, 
	    {
	      "count": 3, 
	      "percent": 4, 
	      "language": "C++"
	    }, 
	    {
	      "count": 3, 
	      "percent": 4, 
	      "language": "Shell"
	    }
	  ], 
	  "timestamp": "2017-05-18T09:52:18.093690", 
	  "stats": [], 
	  "contributions-year": 2254
	}

