<h1 align="center"> Auto like Instagram pics </h1>

Bot to automatically like your friend's Instagram posts, and notify you on your Email.

### Practical use cases

 - You are like me. You don't have time to check social media and you want to give attention to someone so that she notices you.
 - You are in a relationship. Your girlfriend is constantly nagging you for not being the 'first-one' to like her Instagram pics.

 How does it work?

 This script runs Instagram API every 15mins (cronjob) and checks for any new Instagram post for a paticular `user_id`. If a new post is found it likes the post and sends a notification to your configured Slack channel using Slack Webhooks.

Installation

 - clone the folder
 - `npm install`
 - create a `.env` file (you must set `accessToken`, `user_id` (Target user id) from [Instagram Developer API](https://www.instagram.com/developer) and `email_id`.
 
 This would assure that your keys are secured and index.js file is untouched.
 - `npm start` (run the app)

Like all the recent instagram post (test)

     GET http://localhost:3000/run

 Using node-cron (local cron)

 - `npm start` (run the app)
 - `node cron.js &` create a node-cron that sends GET to the app every 15 min
 - `ps` to list background processes
 - `kill <process id>` to stop the node-cron
 
 
Docker Setup
===================

 - Docker >= 17.x, docker-compose >= 1.x
 - Specify environment values in docker-compose.yml.
 - Run `docker-compose up`
