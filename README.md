Step 1: Install Command line tools on terminal
xcode-select --install
Step 2: Install Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
Step 3: Install rbenv
brew update
brew install rbenv ruby-build
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile
Step 4: Install Ruby
rbenv install 2.3.0
rbenv global 2.3.0
ruby -v
Step 5: Install Rails
gem install rails -v 5.0.3
rbenv rehash
Step 6: Checking
ruby -v
# ruby 2.3.0

rails -v
# Rails 5.0.3




§<!-- Creating a new project with rails with the name of the project -->
´´´rails new ProjectName´´´

§<!-- after creating the project we need to add bootstap on it, in order for it to be responsive. follow the instruction in https://github.com/twbs/bootstrap-sass-->


$rails routes
                  Prefix Verb   URI Pattern                    Controller#Action
              pages_home GET    /pages/home(.:format)          pages#home
        new_user_session GET    /users/sign_in(.:format)       devise/sessions#new
            user_session POST   /users/sign_in(.:format)       devise/sessions#create
    destroy_user_session DELETE /users/sign_out(.:format)      devise/sessions#destroy
       new_user_password GET    /users/password/new(.:format)  devise/passwords#new
      edit_user_password GET    /users/password/edit(.:format) devise/passwords#edit
           user_password PATCH  /users/password(.:format)      devise/passwords#update
                         PUT    /users/password(.:format)      devise/passwords#update
                         POST   /users/password(.:format)      devise/passwords#create
cancel_user_registration GET    /users/cancel(.:format)        devise/registrations#cancel
   new_user_registration GET    /users/sign_up(.:format)       devise/registrations#new
  edit_user_registration GET    /users/edit(.:format)          devise/registrations#edit
       user_registration PATCH  /users(.:format)               devise/registrations#update
                         PUT    /users(.:format)               devise/registrations#update
                         DELETE /users(.:format)               devise/registrations#destroy
                         POST   /users(.:format)               devise/registrations#create
