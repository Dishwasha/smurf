require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the smurf plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs += ['test']
  t.pattern = 'test/**/*_test.rb'
  t.verbose = false # Verbose is just dumb
end

desc 'Generate documentation for the smurf plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Smurf'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

# Jewel me

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "smurf"
    gem.summary = "Rails plugin to automatically minify JS and CSS when their bundles get cached"
    gem.description = ""
    gem.email = "gus@thumblemonks.com"
    gem.homepage = "http://github.com/thumblemonks/smurf"
    gem.authors = ["Justin 'Gus' Knowlden"]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end
