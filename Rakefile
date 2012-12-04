desc "Launch preview environment"
task :preview => [:clean, "compass:compile"] do
  system "jekyll --auto --server"
end

desc "Build site"
task :build => [:clean, "compass:compile"] do |task, args|
  system "jekyll"
end

task :clean do
  system "rm -rf _site"
  system "rm -fR css/*"
end

namespace :compass do
  desc 'Compass Watch'
  task :watch do
    system "compass watch"
  end

  desc 'Compile sass scripts'
  task :compile => [:clean] do
    system "compass compile"
  end
end
