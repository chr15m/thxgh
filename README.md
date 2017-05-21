CLI for GitHub user contrib graph & statistics

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
	  "stats": [
	    [
	      "Repositories",
	      "135"
	    ],
	    [
	      "Stars",
	      "481"
	    ],
	    [
	      "Followers",
	      "109"
	    ],
	    [
	      "Following",
	      "294"
	    ]
	  ],
	  "contributions-year": 2254
	}

Get list of repositories for a user:

	$ ./bin/thxgh --repos
	[
	  {
	    "fork": false,
	    "open_issues_count": 0,
	    "watchers": 0,
	    "description": "CLI for GitHub user contrib graph & language stats",
	    "name": "thxgh",
	    "forks": 0,
	    "created_at": "2017-05-18T02:02:21Z",
	    "forks_count": 0,
	    "updated_at": "2017-05-18T11:44:09Z",
	    "html_url": "https://github.com/chr15m/thxgh",
	    "language": "Hy",
	    "clone_url": "https://github.com/chr15m/thxgh.git",
	    "watchers_count": 0,
	    "full_name": "chr15m/thxgh",
	    "ssh_url": "git@github.com:chr15m/thxgh.git",
	    "open_issues": 0,
	    "stargazers_count": 0,
	    "id": 91637951,
	    "size": 13
	  },
	  ...
	]

