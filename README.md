# How to automate static site previews for Github Pages: a demo
Writeup here: https://daiyi.co/blog/pr-previews-for-github-pages/

A feature of modern hosting platforms (e.g. Vercel) that I miss with gh-pages is getting automatic site previews on each PR. Here is my attempt at a hack. 

It works by using github actions to build the site on each commit to a pull request, and pushing the result to the `/pull/{pr-number}` folder on the `gh-pages` branch. This means the preview can be accessed at `https://github.io/username/project/pull/{pr-number}`. When a PR is closed, another action deletes the folder.

Live demo of [an open PR](https://github.com/daiyi/gh-pages-pr-previews/pull/2) with a site preview, and [a closed PR](https://github.com/daiyi/gh-pages-pr-previews/pull/1) with preview cleaned up.

