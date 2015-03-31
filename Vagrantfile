require 'json'
require 'yaml'

VAGRANTFILE_API_VERSION = "2"

homesteadYamlPath = File.expand_path("./homestead.yaml")

require_relative 'scripts/homestead.rb'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	Homestead.configure(config, YAML::load(File.read(homesteadYamlPath)))
end
