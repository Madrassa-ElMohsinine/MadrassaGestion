#!/usr/bin/env rake
require_relative "config/application"

Rails.application.load_tasks

# Forcer la connexion à la base si elle échoue
begin
  ActiveRecord::Base.connection_pool
rescue ActiveRecord::ConnectionNotEstablished => e
  puts "Connection error forced handling: #{e.message}"
  ActiveRecord::Base.establish_connection
end
