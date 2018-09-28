task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end #end greeting:hello task

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end #end greeting:hola task
end #end :greeting namespace

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end #end db:migrate task

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end #end db:seed task
end #end :db namespace

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end #end :console task
