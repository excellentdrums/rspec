require 'rubygems'
gem 'jeweler', ">= 1.4.0"
require 'rake'
require 'fileutils'
require 'pathname'

$:.unshift File.expand_path(File.join(File.dirname(__FILE__),'lib'))

require 'rspec/version'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "rspec"
    gem.version = Rspec::Version::STRING
    gem.rubyforge_project = "rspec"
    gem.summary = "pulls in the other rspec gems"
    gem.email = "dchelimsky@gmail.com;chad.humphries@gmail.com"
    gem.homepage = "http://github.com/rspec/meta"
    gem.authors = ["David Chelimsky", "Chad Humphries"]
    gem.version = Rspec::Version::STRING
    gem.add_dependency "rspec-core", ">= #{Rspec::Version::STRING}"
    gem.add_dependency "rspec-expectations", ">= #{Rspec::Version::STRING}"
    gem.add_dependency "rspec-mocks", ">= #{Rspec::Version::STRING}"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

task :clobber do
  rm_rf 'pkg'
end

task :default => [:check_dependencies]
