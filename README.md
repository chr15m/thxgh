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
		--repos will print JSON formatted list of repositories.

Download contributions graph SVG for a user:

	$ ./bin/thxgh --contributions chr15m > chr15m-contributions.svg

Get language statistics and pinned repositories for a user:

	$ ./bin/thxgh --stats chr15m
	{
	  "languages": [
	    {
	      "count": 29, 
	      "percent": 23, 
	      "language": "JavaScript"
	    }, 
	  ...
	  ], 
	  "timestamp": "2017-05-18T09:52:18.093690", 
	  "stats": [], 
	  "contributions-year": 2254,

	}

Get list of repositories for a user:

	$ ./bin/thxgh --repos
	[
	  {
	    "fork": true, 
	    "open_issues_count": 0, 
	    "watchers": 0, 
	    "description": "Mathematical expression evaluator in JavaScript", 
	    "name": "js-expression-eval", 
	    "forks": 0, 
	    "created_at": "2012-12-01T05:39:44Z", 
	    "forks_count": 0, 
	    "updated_at": "2013-01-13T10:58:59Z", 
	    "html_url": "https://github.com/chr15m/js-expression-eval", 
	    "language": "JavaScript", 
	    "clone_url": "https://github.com/chr15m/js-expression-eval.git", 
	    "watchers_count": 0, 
	    "full_name": "chr15m/js-expression-eval", 
	    "ssh_url": "git@github.com:chr15m/js-expression-eval.git", 
	    "open_issues": 0, 
	    "stargazers_count": 0, 
	    "id": 6950716, 
	    "size": 137
	  }, 
	  ...
	]

