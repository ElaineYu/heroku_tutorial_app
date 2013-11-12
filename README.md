Getting Started with Heroku

https://devcenter.heroku.com/articles/getting-started-with-ruby

Commands

####Login to Heroku
heroku login

#### Create web.rb (add code)
touch web.rb

#### Create Gemfile:
touch Gemfile

Even if your app has no gem dependencies, you should still create an empty Gemfile in order that it appear as a Ruby app.

####  Create Procfile:
touch Procfile

Add this: 

	web: bundle exec ruby web.rb -p $PORT

A Procfile a text file in the root directory of your application, to explicitly declare what command should be executed to start a web dyno. 



