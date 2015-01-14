# Development Environment Setup

1. Install **ruby-1.9.3-p392** using rvm
```
$ rvm install 1.9.3-p392
$ rvm use 1.9.3-p392 --default
```

2. Install **postgreSQL 9.2.4**
```
$ brew install postgresql (on Mac)
```

3. Execute the following SQL commands:
```
$ CREATE ROLE player_dev LOGIN PASSWORD 'player_dev' NOSUPERUSER INHERIT CREATEDB NOCREATEROLE NOREPLICATION;

$ CREATE ROLE player_test LOGIN PASSWORD 'player_test' NOSUPERUSER INHERIT CREATEDB NOCREATEROLE NOREPLICATION;
```

4. Create database
```
$ rake db:migrate

$ rake db:setup
```

5. Start the rails server
```
$ bundle exec rails s
```
