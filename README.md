👋 

This is a barebones python environment with Streamlit.

Thanks to [emunozlorenzo](https://github.com/emunozlorenzo/Deploying-Streamlit-with-Heroku) and [Gilbert Tanner](https://gilberttanner.com/blog/deploying-your-streamlit-dashboard-with-heroku) for previous documentation.

If you have problems, probably check the [Streamlit posts with the Heroku tag](https://discuss.streamlit.io/tag/heroku).

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

Steps:

  - Get a Heroku account 
  - Install [Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-python)
      - `brew tap heroku/brew && brew install heroku`
  - Authenticate the CLI locally: `heroku login` 
  - For a good starter streamlit configuration, clone this repo into eg. "my-project-name"
    - `git clone git@github.com:christopherfrance/streamlit-on-heroku.git my-project-name`
  - `cd my-project-name`
  - Edit `setup.sh` to use your email address.
  - Run it locally:
    - Install python dependencies: `pip install -r requirements.txt`
    - Run streamlit app in the browser locally: `streamlit run app.py`
  - Deploy to Heroku using git: 
    - Create the remote heroku projet: `heroku create`
    - Commit your work: `git add . && git commit -m "Initial commit!"`
    - Push the code to Heroku: `git push heroku master`
    - It should install requirements automatically on push, and give you a live URL!
  - Create your normal repository on github (Don't rely on Heroku to work like a normal repository.)
    - Make your new repo the origin for your new project: 
      - `git remote rm origin`
      - `git remote add origin [address of your new project]`
    - Push to github `git push origin master`
  - If you need to configure Heroku
    - `heroku config:set KEY=VALUE`
    - Read about the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)