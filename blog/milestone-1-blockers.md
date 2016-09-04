# Milestone 1 Blockers

# Bloker 1

I’m working to completing my first mile stone and I’ve hit a road block: can’t start a default Laravel application on EB. I keep seeing the “something went wrong” message in the UI. Locally, the application is configured to deploy on a Vagrant box (Ubuntu) and all is well: not the case on EB. When I run the application through Shippable CI the build is fine.

I’ve ssh’ed into the EB server and started to look around inside the application. The first thing I’ve noticed, and it is an oddity, not .env file. To solve that problem I’ll just copy the default config and generate a new one. Next, I need to generate a new set up application keys and I should be good to go.

The next blocker will be getting the RDS connection strings set in my EB container as environment variables. I then need to somehow read them into the application.