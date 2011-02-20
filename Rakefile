require 'bundler'
Bundler::GemHelper.install_tasks

require 'yard'
require 'rspec/core/rake_task'

task :default => [:spec]

desc "run spec tests"
RSPec::Core::RakeTask.new('spec') do |t|
  t.pattern = 'spec/**/*_spec.rb'
end

desc 'Generate Documentation'
YARD::Rake::YardocTask.new do |t|
  t.files = ['lib/**/*.rb', '-', 'LICENSE']
  t.options = ['--main', 'README', '--no-private']
end