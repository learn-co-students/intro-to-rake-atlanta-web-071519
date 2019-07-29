namespace :greeting do 

desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs hola to the terminal'
task :hola do 
  puts "hola de Rake!"
end

end


task :environment do 
  require_relative './config/environment'
end

desc 'drop into the Pry console'
task :console => :environment do 
 Pry.start
end

namespace :db do 

  #  "migrating" our database by applying SQL statements that alter that database.
  # '=>' needs access to the environment file
  desc 'migrate changes to your database'
  task :migrate => :environment do 
    Student.create_table
  end
  
  # here is where you would put test data in order to test your code
  desc 'seed the database with some dummy tasks'
  task :seed do 
    require_relative './db/seeds.rb'
  end

end




