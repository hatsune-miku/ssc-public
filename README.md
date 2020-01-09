# SSC by EGGTART😈

* both apt and gem require sudo
```bash
$ su
```

* ensure **ruby** version >= 2.5
```bash
$ apt uninstall ruby
$ gpg2 --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
$ curl -L https://get.rvm.io | bash -s stable
$ rvm install ruby-2.6
$ apt install ruby2.6-dev
```

* ensure **gem** is in latest version
```bash
$ apt remove gem
$ apt install gem
```

* for **chinese developer** under GFW
```bash
$ gem sources -r https://rubygems.org/
$ gem sources -a https://gems.ruby-china.com/
```

* ensure **rails** is in latest version
```bash
$ gem uninstall rails
$ gem install rails
```

* ensure **rake** is in latest version
```bash
$ gem uninstall rake
$ gem install rake
```

* ensure **bundler** version >= 2.1.2
```bash
$ gem uninstall bundler
$ gem install bundler
```

* ensure **node.js** is in latest version
```bash
$ apt remove node
$ apt remove nodejs
$ apt install npm
$ npm i n -g
$ n stable
```

* ensure **yarn** is in latest version
```bash
$ npm i yarn -g
```

* ensure build environment for **nokogiri, mysql2, etc**
```bash
# for all gems.
$ apt install build-essential

# for nokogiri.
$ apt install libxslt-dev
$ apt install libxml2-dev

# for mysql2.
$ apt install libmysqld-dev
$ apt install mysql-client
$ apt install mysql-server
$ apt install libssl-dev
```

* init this program
```bash
# this should finish in 5 min.
# if didn't, use a VPN or switch to a chinese repository.
$ bundle install

# for slower CPU(s), these can take EXTREMELY LOOOOOOOOOOONG in first run.
$ yarn install            # about 25 min on a raspberry pi.
                          # several seconds on a mbp 2018.
                          
$ RAILS_ENV=production    # in a instant

$ ./bin/webpack           # about 25 min on a raspberry pi.
                          # several seconds on a mbp 2018.

$ rake assets:precompile  # about 25 min on a raspberry pi.
                          # several seconds on a mbp 2018.

$ rake db:create          # about 5 s

$ rake db:migrate         # about 5 s
```

* finally, start the server at localhost:80
```bash
$ bundle exec rails s -e production -b 0.0.0.0 -p 80
```
