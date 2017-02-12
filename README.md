# CJTozer.github.io

To set up:

* Git clone the repo
  * Make sure the current branch is the `blog` branch (it should be by default)
* Run `npm install`
* Use `hexo` (`npm install -g hexo-cli`) to generate content

To test locally:

* Run `hexo server`

To deploy:

* Run (`hexo clean` then) `hexo deploy -g`, which will generate and upload the latest site to the `master` branch of this repo.

To create a new draft:

* Run `hexo new draft <post-name>`

To publish that draft:

* Run `hexo publish <post-name>`

To go straight to a published post:

* Run `hexo new post <post-name>`
