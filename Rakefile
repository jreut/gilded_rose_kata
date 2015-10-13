require 'rspec/core/rake_task'
require 'flog_cli'

RSpec::Core::RakeTask.new(:spec)

desc 'Flog report'
task :flog do
  f = FlogCLI.new methods: true, group: true, all: true, blame: true
  f.flog 'lib/gilded_rose.rb'
  f.report
end

task default: :flog

require 'rake/testtask'
Rake::TestTask.new
