#Getting Started with Heroku

https://devcenter.heroku.com/articles/getting-started-with-ruby

##Commands

####Login to Heroku:

	heroku login

#### Create web.rb:

	touch web.rb

Add this:

	require 'sinatra'

	get '/' do
		"Hello, world"
	end

#### Create Gemfile

Even if your app has no gem dependencies, you should still create an empty Gemfile in order that it appear as a Ruby app.:

	touch Gemfile

Add this:

	source "https://rubygems.org"
	ruby "2.0.0" #Or ruby "1.9.3"
	gem 'sinatra', '1.1.0'


#### Create Procfile:

A Procfile a text file in the root directory of your application, to explicitly declare what command should be executed to start a web dyno. 

	touch Procfile

Add this: 

	web: bundle exec ruby web.rb -p $PORT


#### Run in command line:
<code> bundle install <code>
#### Install and Run 
<code> foreman start <code>
####  Run 
<code> heroku create <code> 
#### Run 
<code> git push heroku master <code>
#### Ensure one dyno is running
<code> heroku ps:scale web=1 <code>
#### Check the state of app's dyno
<code> heroku ps <code>
#### Open app in browser 
<code>heroku open</code>

