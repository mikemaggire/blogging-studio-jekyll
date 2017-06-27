# frozen_string_literal: true
source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# references : gem groups http://bundler.io/v1.3/groups.html

# Happy Jekylling!
gem "jekyll", "3.5.0"

# required by windows to ensure proper --watch
gem 'wdm', '~> 0.1.0' if Gem.win_platform?

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-sitemap"
end
