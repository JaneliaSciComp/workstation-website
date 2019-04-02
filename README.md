# Workstation Static Website

## Build

Compiling this website requires Ruby 2.4.2 and Jekyll. 
On MacOS, this is best managed by installing Homebrew and RVM (Ruby Version Manager):

~~~~
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    curl -L https://get.rvm.io | bash -s stable --ruby
~~~~

Then Ruby and Jekyll:

~~~~
    rvm install ruby-2.4.2
    gem install jekyll
~~~~

After installing these, make sure you're in the website/ directory, and 
then install the required Gems like this:

~~~~
    gem install bundler
    bundle install
~~~~

To compile the site and serve it in development mode:

~~~~
    bundler exec jekyll serve
~~~~

You should then be able to view the website in your web browser: [http://localhost:4000](http://localhost:4000)

## Deployment

To deploy to production site:

~~~~
    scp -r _site/* workstation:/var/www/html
~~~~

