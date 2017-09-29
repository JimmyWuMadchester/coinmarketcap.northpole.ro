Install
=======

# Minimum hardware requirements

2 vCPU

1GB RAM

30GB disk space

# Setup

```rvm install 2.1.0```

```gem install bundler```

```gem install rails```

git clone this repo

```cd coinmarketcap-api```

```bundle install```

ruby script.rb

# Deploy with capistrano

cap production deploy # This will run the generate:doc rake task

# Load the crontab

crontab crons/northpole-crontab
