# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

task :provision do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/playbook.yml -u root"
end

task :deploy_api do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/api.yml -u root"
end

task :deploy_ui do
  sh "ansible-playbook -i ./deployer/hosts ./deployer/ui.yml -u root"
end
