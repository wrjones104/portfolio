# wjones.dev Portfolio Portal

This repository serves as the central hub and landing page for wjones.dev. It acts as the root domain host for my personal brand and developer portfolio.

## Architecture

This setup utilizes GitHub Pages to route traffic. This repository holds the CNAME record for wjones.dev.

Any other public repository on my GitHub account that has GitHub Pages enabled will automatically be routed as a subdirectory of this main domain.

* Root: wjones.dev (This repository)
* Project: wjones.dev/ap-tracker (Hosted from the ap-tracker repository)
* Project: wjones.dev/presentation (Hosted from the presentation repository)

## Dynamic Content Loading

The index file uses vanilla JavaScript to fetch my latest public repositories via the GitHub API. 

It filters out the root repository to avoid looping and checks if a repository has GitHub Pages enabled. If Pages are enabled, the project card links directly to the live wjones.dev/project-name URL. If not, it links to the standard GitHub repository URL.

## Tech Stack
* HTML5 / Vanilla JS
* Tailwind CSS
* GitHub REST API