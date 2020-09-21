# Buttonbase Initial Deployment

<!-- https://github.com/Requarks/wiki-heroku/issues/22 -->

Using [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli):

```
heroku login
heroku git:remote -a buttonbase
heroku stack:set container
```

In the Heroku dashboard: `Resources > Add-Ons`, add the Heroku Postgres add-on, then:

```
git push heroku 2.x:main
```

This deploys the `2.x` branch to Heroku by renaming it to `main` on the remote. The branch rename to `main` is necessary for Heroku to automatically deploy.

Below follows the original Requarks/wiki-heroku README:

## Heroku Deploy for Wiki.js

This repo is an Heroku app definition for Wiki.js.  
For information about Wiki.js, check out the following links:

- [Official Website](https://wiki.js.org/)
- [GitHub Repository](https://github.com/Requarks/wiki)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/requarks/wiki-heroku/tree/2.x)

If you want to modify the configuration beyond what's available through environment variables, then:
* Clone this repo
* Make and commit your configuration changes
* `git remote add heroku https://git.heroku.com/my-wiki.git`
* `git push heroku`, or if you are on a branch, `git push heroku mybranch:master`
