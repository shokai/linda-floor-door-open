Linda Floor Door Open
=====================
open door with Arduino Floor-sensor and RocketIO::Linda

* watch Tuples ["sensor", "floor", Number]
* write a Tuple ["door", "open"]

Dependencies
------------
- Ruby 1.8.7 ~ 2.0.0
- [LindaBase](https://github.com/shokai/linda-base)


Install Dependencies
--------------------

    % gem install bundler foreman
    % bundle install


Run
---

set ENV var "LINDA_BASE" and "LINDA_SPACE"

    % export LINDA_BASE=http://linda.example.com
    % export LINDA_SPACE=test
    % bundle exec ruby linda-floor-door-open.rb

or

    % LINDA_BASE=http://linda.example.com LINDA_SPACE=test bundle exec ruby linda-floor-door-open.rb


Install as Service
------------------

for launchd (Mac OSX)

    % sudo foreman export launchd /Library/LaunchDaemons/ --app linda-floor-door-open -u `whoami`
    % sudo launchctl load -w /Library/LaunchDaemons/linda-floor-door-open-open-1.plist
