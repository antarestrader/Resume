
tasks_path = File.join(File.dirname(__FILE__),"tasks")
rake_files = Dir["#{tasks_path}/*.rake"]
rake_files.each{|rake_file| load rake_file }

task :default => [:compile]

desc "Make all tylesheets and html (default)"
task :compile => [:stylesheets, :html]

desc "compile stylesheets with compass"
task :stylesheets do
  sh "compass"
end

desc "compile HAML to HTML"
task :html do
  sh "haml resume.html.haml resume.html"
end