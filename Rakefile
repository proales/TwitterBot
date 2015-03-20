# require 'bundler'
# Bundler::GemHelper.install_tasks

# require "chatterbot/version"

# require 'rspec/core'
# require 'rspec/core/rake_task'
# RSpec::Core::RakeTask.new(:spec) do |spec|
#   spec.pattern = FileList['spec/**/*_spec.rb']
# end

# RSpec::Core::RakeTask.new(:rcov) do |spec|
#   spec.pattern = 'spec/**/*_spec.rb'
#   spec.rcov_opts = %w{--exclude .bundler,.rvm}
#   spec.rcov = true
# end

# task :default => :spec

# require 'rdoc/task'
# Rake::RDocTask.new do |rdoc|
#   rdoc.main = "README.rdoc"
#   rdoc.rdoc_files.include("README.rdoc", "lib/**/*.rb")
#   rdoc.rdoc_dir = 'rdoc'
#   rdoc.title = "'chatterbot #{Chatterbot::VERSION}'"
# end

# task :console do
#   require 'irb'
#   require 'irb/completion'
#   require 'chatterbot' # You know what to do.
#   ARGV.clear
#   IRB.start
# end

require 'rspec/core/rake_task'
task :default => :spec
RSpec::Core::RakeTask.new

require 'active_record'
require 'sqlite3'
ActiveRecord::Base.establish_connection(
   :adapter   => 'sqlite3',
   :database  => 'test.db'
)

ActiveRecord::Migration.class_eval do
  create_table :articles do |t|
        t.string :scoop_id
  end
  
  create_table :accounts do |t|
        t.string :name
        t.string :topic
        t.string :section
        t.string :subsection
        t.string :all
        t.string :geofacet
        t.string :perfacet
        t.string :orgfacet
        t.string :desfacet
   end
end

# ActiveRecord::Migration.class_eval do
#   create_table :accounts do |t|
#         t.string :name
#         t.string :topic
#         t.string :section
#         t.string :subsection
#         t.string :all
#         t.string :geofacet
#         t.string :perfacet
#         t.string :orgfacet
#         t.string :desfacet
#    end
# end






