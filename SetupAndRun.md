Install
=======

@Mess110 has very minimum instructions in his original repository. I will add my note to it so it can be followed step by step easily.

# Minimum hardware requirements

This is the suggested requirements by @Mess110:
2 vCPU
1GB RAM
30GB disk space

I've used Azure to get a vitual machine running for this project. You should be able to size up and down the Azure VM as you like.

# Setup

Freshly from the new VM, there are a few more steps needed rather suggested by @Mess110.

1. (Install RVM)[https://github.com/rvm/ubuntu_rvm]
2. ```rvm install 2.1.0``` (Using RVM to install ruby 2.1.0)
3. ```gem install bundler``` (Install Bundler)
4. ```git clone https://github.com/JimmyWuMadchester/coinmarketcap.northpole.ro.git``` (Git clone this repo)
5. ```cd coinmarketcap-api```
6. ```bundle install```

# Running the crawler as an one-off

```ruby script.rb```

You can check the log file under ```./logs/script.log```
You can also find all the downloaded JSON objects under ```./public/api/```

# Deploy with capistrano

```cap production deploy``` # This will run the generate:doc rake task

# Load the crontab

Set up a task scheduler for running the crawler every 5 mins.
```crontab crons/northpole-crontab```
