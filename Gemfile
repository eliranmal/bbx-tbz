source "https://rubygems.org"

# dependencies
gem "github-pages", group: :jekyll_plugins

# plugins
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# fixes bundler errors for ruby >= 3.x
# gem "webrick", "~> 1.7"