# chi-js-test-automation
This repository hosts the presentation given on May 13, 2025 at the Chicago JS Meetup.

It was created using [Marp](https://marp.app/). The main content can be found in the `presentation.md` document. The presentation itself can be located in the `slide-deck` directory

## Running Locally

To build the slides locally:

1. Install `marp` ([marp cli docs](https://github.com/marp-team/marp-cli?tab=readme-ov-file#marp-teammarp-cli))
	```sh
	npm install -g @marp-team/marp-cli
	```
2. run the following command 
	```sh
	marp presentation.md --theme theme.css -o 'slide-deck/presentation.html'
	```

## TODOs
 - [x] Add summary and details for running this on this readme
 - [ ] Customize the theme to match web site