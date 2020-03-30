# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

task :provision do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/playbook.yml"
end

task :deploy-api do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/api.yml"
end

task :deploy-ui do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/ui.yml"
end
