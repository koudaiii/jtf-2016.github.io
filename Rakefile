namespace :deploy do
  puts "Building... "
  system "bundle exec middleman build"
  puts "Deploy to gh-pages"
  system "bundle exec middleman deploy"
end
