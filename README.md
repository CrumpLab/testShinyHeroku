# testShinyHeroku
testing deploying a shiny app to heroku

1. Get a [heroku](https://www.heroku.com) account
2. Create a new app
3. Choose deployment method Github
4. Allow heroku to access Github
5. Under settings add buildpack for R

  ```http://github.com/virtualstaticvoid/heroku-buildpack-r.git#heroku-16```

6.