# Setup (Windows)
* Install RubyInstaller: https://rubyinstaller.org/downloads/
  * Choose the Ruby+Devkit option
  * When prompted, enable MSYS2 installation
  * At the end, allow installer to initialize MSYS2 Devkit (`ridk install`)

# Setup (macOS)
* Update Homebrew: `brew update`
* Use Ruby version manager
  * Install rbenv if it isn't installed: `brew install rbenv`
  * Upgrade rbenv if it's already installed: `brew upgrade rbenv`
* Setup rbenv integration to your shell
  * `rbenv init`
* Install and use Ruby version 2.5.3
  * `rbenv install 2.5.3`
  * `rbenv global 2.5.3`

# Setup continued (All OS)
* Install bundler
  * `gem install bundler -v 1.17.1`
  * Note: Windows 10 and bundler version 2.0.1:
    * bundler version 2.0.1 (the default on 2019-01-23) on Windows 10 with computer 'Austin' didn't install, even though I saw the message `Successfully installed bundler-2.0.1`.
    * Running `bundle install` afterwards resulted in: `find_spec_for_exe': can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)`
    * Installing bundler version 1.17.1 gets around this problem
* Clone this repo
* `cd` into this project folder
* Install gems
  * `bundle install`

# Development
* In the project directly, start the Jekyll server: `bundle exec jekyll serve`
* Go to http://localhost:4000

# Deployment
* Push to master branch on GitHub. This will trigger continuous deployment to update the remote site on Netlify.