require "rake/testtask"
require "bundler/gem_tasks"
require "find"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc "find . files"
task :find_file do
  Find.find('.') do |name|
    puts name unless name.include?('/.') || !File.file?(name)
  end
end
