# Milestone 1 Blockers

# Blocker 
## September 4, 2016

I’m working to completing my first mile stone and I’ve hit a road block: can’t start a default Laravel application on EB. I keep seeing the “something went wrong” message in the UI. Locally, the application is configured to deploy on a Vagrant box (Ubuntu) and all is well: not the case on EB. When I run the application through Shippable CI the build is fine.

I’ve ssh’ed into the EB server and started to look around inside the application. The first thing I’ve noticed, and it is an oddity, not .env file. To solve that problem I’ll just copy the default config and generate a new one. Next, I need to generate a new set up application keys and I should be good to go.

The next blocker will be getting the RDS connection strings set in my EB container as environment variables. I then need to somehow read them into the application.

# Blocker 
## September 5, 2016

I've been going back and forth trying to pick a CI service to use: Semaphore/Shippable. I received the green light from both I'd be treated as a student for the duration of the semester. Ok, so I've noticed it is not super fast to dig into error logs with the first CI, second CI reports directly into the UI: enter speed. I think it is by far faster to get the CI report directly on screen, I've got a lot of other things to do. On to my blocker, I cannot for the life of my get either CI to auto deploy my code to EB while assuming the IAM role created for each. I've spent a lot of time debugging this issues and really need to move on. At this point, the bug is going into the icebox and I'll fix it at a later time as it is not a show stopper.   