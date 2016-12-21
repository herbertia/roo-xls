source 'https://rubygems.org'

# Specify your gem's dependencies in roo-xls.gemspec
gemspec

gem "spreadshiit", "> 0.9.0", github: 'herbertia/spreadsheet', branch: 's-v1.1.4'


if ENV['TRAVIS']
  gem 'roo', '>= 2.0.0beta1', github: 'roo-rb/roo'
else
  gem 'roo', '>= 2.0.0beta1', path: ::File.expand_path('../../roo', __FILE__)
end

group :test do
  # additional testing libs
  gem 'webmock'
  gem 'shoulda'
  gem 'rspec', '>= 3.0.0'
  gem 'simplecov', '>= 0.9.0', :require => false
  gem 'coveralls', :require => false
end

group :local_development do
  gem 'terminal-notifier-guard', require: false if RUBY_PLATFORM.downcase.include?('darwin')
  gem 'guard-rspec', '>= 4.3.1' ,require: false
  gem 'guard-bundler', require: false
  gem 'guard-preek', require: false
  gem 'guard-rubocop', require: false
  gem 'guard-reek', git: 'https://github.com/pericles/guard-reek', require: false
  gem 'pry'
  gem 'transpec'
end
