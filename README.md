# Workstation Static Website

Compiling this website requires Ruby 2.4.2 and Jekyll.

On MacOS, this is best managed by installing Homebrew and RVM (Ruby Version Manager):

~~~~
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    curl -L https://get.rvm.io | bash -s stable --ruby
    source /Users/$USER/.rvm/scripts/rvm
~~~~

Follow RVM's instructions to add the .rvm init script to your .bashrc or .bash_profile file.

Then install Ruby and Jekyll:

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

To build the static site content without serving on a dev instance, you can do this:
~~~~
    bundler exec jekyll build
~~~~

