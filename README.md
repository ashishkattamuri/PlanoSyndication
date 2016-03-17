## PlanoSyndication Exercise README

#### Background
At PlanOmatic we have various data feeds that our clients access via URL.  Since the feeds are very large .txt files,
We have tasks that generate them every few hours and save them to our database under the table Syndication.
We are in the process of creating our second generation software and would like your help migrating a couple
of our feeds to a Rails API.

#### Install
1. Clone this repo onto your local machine.

2. `$ cd planomatic_syndication` in root folder.

3. Run `$ bundle` to install gems.

4. If you don't already have it installed, install MySQL onto your machine and start MySQL server.

5. Run `$ rake db:drop db:create db:migrate db:seed` to create, migrate and seed the database correctly.  Note: If there is a problem, you may have to change the username/password in this repos config/database.yml

6. Run `$ rails s` and you should be able to see this application on localhost:3000.

#### Exercise
Your task is to create routes for a couple of our data feeds.
Specifically, I would like you to create a couple routes, a syndications_controller and a Syndication model where all your logic is stored.
You can find our syndication records under the table syndications, where each record has a name, body and created_at.
The name of the syndication record is how you identify which feed that record belongs to, and the body is what the route should respond with.
There are multiple records in the database, so please be sure to respond to the routes with the most recent feed, based on created_at.

###### Tour URLs
route: `localhost:3000/syndication/tour_urls`
column name: tour_urls.txt

###### Tour Slides Descriptions
route: `localhost:3000/syndication/tour_slides_descriptions`
column name: tour_slides_descriptions.txt
