/*
bundle exec rake build
//key-register//
bundle exec rake release
*/
#create gem
bundle gem app
bundle config

#github
cd app
git add --all
git commit -m "crate. change.gitignore"
git remote add origin git@github.com:takagotch/app.git
git push -u origin master

#install gem
cd app
bundle exec rake install

#login account 
https://rubygems.org/sign_up

#register api-key-account
curl -u takagotch https://rubygems.org/api/v1/api_key.yaml > ~/.gem/credentials; chmod 0600 ~/.gem/credentials

#release gem
cd app
bundle exec rake release



