require 'bundler/gem_tasks'
require 'rspec/core/rake_task'
require 'ci/reporter/rake/rspec' 

desc "Run specs"
task :spec do
  RSpec::Core::RakeTask.new(:spec=> ["ci:setup:rspec"]) do |t|
    t.rspec_opts = %w{--colour --format progress}
    t.pattern = 'spec/*_spec.rb'
  end
end

desc "Default: run specs."
task :default => [:spec]
#RSpec::Core::RakeTask.new(:spec => ["ci:setup:rspec"])
