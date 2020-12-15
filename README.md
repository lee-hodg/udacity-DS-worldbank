# Description

This is a simple app that uses bootstrap, jquery, flask and plotly to display some data from the Worldbank.

It was completed as part of the Udacity DS Nanodegree

# Webapp

It is live [here](https://udacity-ds-worldbank.herokuapp.com/)

# Local Deployment

## Create a virtualenv

Create the virtualenv

```bash
python3 -m venv worldbankvenv
```

Activate it

```bash
source worldbankenv/bin/activate
```

Install requirements

```bash
pip3 install -r requirements.txt
```

In `worldbank.py` uncomment the line `app.run(host='127.0.0.1', port=3001, debug=True)`
and then run the app with

```bash
python worldbank.py
```

from inside the `web_app` directory.

# Remote deployment

Install the Heroku client

```bash
curl https://cli-assets.heroku.com/install-ubuntu.sh | sh
https://devcenter.heroku.com/articles/heroku-cli#standalone-installation
heroku —-version
```

Login to Heroku (create an account there if you don't have one already)

```bash
heroku login
```

Now create the app on Heroku

```bash
heroku create my-app-name
```

You should see heroku listed if you run

```bash
git remote -v
```

Output:

```bash
git remote -v
grv='git remote -v'
gr='git remote'
g=git
heroku  https://git.heroku.com/udacity-ds-worldbank.git (fetch)
heroku  https://git.heroku.com/udacity-ds-worldbank.git (push)
origin  https://github.com/lee-hodg/udacity-DS-worldbank (fetch)
origin  https://github.com/lee-hodg/udacity-DS-worldbank (push)

```
as well as the `origin` to this github repo.

Deploying to heroku is as simple as

```bash
git push heroku master
```

After making changing to the app ensure to commit them, and push to your personal github repo
(if you forked this) and also re-deploy to heroku as above.

**Remember:** comment out the `app.run` line.
