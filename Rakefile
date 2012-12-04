desc "Launch preview environment"
task :preview => [:clean, "compass:run"] do
  system "jekyll --auto --server"
end

desc "Build site"
task :build => [:clean, "compass:run"] do |task, args|
  system "jekyll"
end

task :clean do
  system "rm -rf _site"
end

namespace :compass do
  desc 'Clean and compile'
  task :run => ["compass:clean", "compass:compile"]

  desc 'Delete temporary compass files'
  task :clean do
    system "rm -fR css/*"
  end

  desc 'Compile sass scripts'
  task :compile => [:clean] do
    system "compass compile"
  end
end
