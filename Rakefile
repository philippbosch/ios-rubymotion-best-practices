task :default => [:server]

task :server do
  sh "open http://localhost:4567/"
  sh "gollum"
end

task :static => [:generate] do
  sh "open http://localhost:4568/"
  sh "gollum-site serve --watch --port 4568"
end

task :generate do
  sh "rm -f _site/*.html && gollum-site generate"
end

task :publish => [:generate] do
  ref = File.read('.git/refs/heads/master')
  sh "cd _site && git add . && git commit -am \"Update based on #{ref}.\" && git push heroku master"
  sh "open http://ios-rubymotion.cloud.pb.io/"
end
