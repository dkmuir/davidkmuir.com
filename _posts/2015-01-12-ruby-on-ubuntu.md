---
published: false
---

## Semi-sane Ruby Config

I'm not much of a ruby user, but I recently tried setting up Redmine on an older 12.04 install and finally figured out how to get things working with Ruby 1.9

The general gist is:

    sudo apt-get install ruby1.9.3
    sudo update-alternatives --config ruby
    #select 1.9.1 (should be option 2)
    sudo update-alternatives --config gem
    #select 1.9.1 (again should be option 2)
    #add the following to ~/.profile
    export GEM_PATH=$(ruby -e 'puts Gem.user_dir')
    #then run
    source ~/.profile
    
You should now have a newer version of ruby, and gems will also get installed into the user's folder.