require 'bundler/gem_tasks'
require 'rake/testtask'
require 'find'

desc 'Run tests'
task :default => [:test]

desc 'Run tests'
Rake::TestTask.new(:test) do |t|
  t.libs << 'test'
  t.libs << 'lib'
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List files in project'
task :list_files do
  Find.find(ENV["PWD"]) do |path|
    next if path.include?("/.")
    puts path if File.file?(path)
  end
end
