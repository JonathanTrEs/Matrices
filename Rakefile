#Fichero de Rakefile para Guard

$:.unshift File.dirname(__FILE__) + 'lib'
$:.unshift './lib', './spec'

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new
task :default => :spec

desc "Pruebas unitarias de la clase Fraccion"
task :p do
	sh "rspec -I. spec/matriz_spec.rb"
end

desc "Pruebas unitarias de la clase Fraccion"
task :doc do
	sh "rspec -I. spec/matriz_spec.rb --format documentation"
end

desc "Pruebas unitarias de la clase Fraccion"
task :html do
	sh "rspec -I. spec/matriz_spec.rb --format html"
end
