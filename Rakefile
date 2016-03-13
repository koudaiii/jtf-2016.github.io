require 'rake'

task default: [:deploy]

desc "Deploy"
task :deploy do
  puts "Building... "
  system "bundle exec middleman build"
  puts "Deploy to gh-pages"
  system "bundle exec middleman deploy > /dev/null 2>&1"
end
