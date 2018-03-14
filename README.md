# testShinyHeroku
testing deploying a shiny app to heroku, notes to self

1. Get a [heroku](https://www.heroku.com) account
2. Create a new app
3. Choose deployment method Github
4. Allow heroku to access Github
5. Under settings add buildpack for R

  ```http://github.com/virtualstaticvoid/heroku-buildpack-r.git#heroku-16```

More info about the buildpack [here](https://github.com/virtualstaticvoid/heroku-buildpack-r/tree/heroku-16)

6. Create a new github repository for the shiny app
7. Create a run.R file containing the following:

  ```
  library(shiny)
  
  port <- Sys.getenv('PORT')
  
  shiny::runApp(
    appDir = getwd(),
    host = '0.0.0.0',
    port = as.numeric(port)
  )
  
  ```
8. Create an app.R file (or use the default one provided by Heroku)
9. push to github repo
10. Deploy branch on Heroku
11. view app