require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "easy_diff"
  gem.homepage = "http://github.com/Blargel/easy_diff"
  gem.license = "MIT"
  gem.summary = %Q{Recursive diff, merge, and unmerge for hashes and arrays.}
  gem.description = %Q{Easy Diff enhances the functionality of Hash, allowing recursive diff, merge, and unmerge of arbitrarily constructed hashes.
  This is perfect for people who need to do diffs on not only plain text files but also data as Hash or JSON objects. Unmerge
  is included with diff and merge to more easily allow versioning of arbitrary data.}
  gem.email = "LargeBagel@gmail.com"
  gem.authors = ["Abner Qian"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  #  gem.add_runtime_dependency 'jabber4r', '> 0.1'
  #  gem.add_development_dependency 'rspec', '> 1.2.3'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new
