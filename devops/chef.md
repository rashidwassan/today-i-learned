# Chef
Progress Chef is a configuration management tool written in Ruby and Erlang. It uses a pure-Ruby, domain-specific language for writing system configuration "recipes". Chef can be integrated with various cloud services as well.

Advantages of Chef
- Complete Automation
- Increased uptime
- Improved performance
- Ensure compliance
- Prevent errors
- Reduced cost

## Chef Components
Chef Workstation: Computers where the configurations are created, tested or changed.
Chef Server: Middle man between node and chef workstation. Cookbooks are stored here. It can be local or remote.
Node: Is the system which requires the configurations.

System Administrators were used to manage, troubleshoot, and monitor servers and networks.
In 2005 a new CMT (configuration management tool)  was built, called marionette. Now known as Chef.
CMT is a tool to automate admin tasks.
It is an IaC (infrastructure as code).
Puppet was used befo4re Chef, now it is mostly replaced.
Configuration Management Tools are of two types
Pull Based: Chef, Puppet. Node will pull the recipe.
Push Based: Ansible, SaltStack. Server will push the recipe.
Ohai is a simple database containing current configuration.
Knife CLI tool, which is responsible for data transmissions in Chef Infrastructure.
Idempotency avoidance of running redundant code again & again.
Bootstrap is a term used for the node-server connection process.
Chef Supermarket place to get ready-made cookbooks and recipes.
Recipe is a file where you write Ruby code.

Setting up Chef and Creating and Executing Recipes: 
Install Chef by copying the download link of the installer for Ubuntu.
Use wget to download the installer.
Use yum to install the Chef.
which chef to see where it is located.

Creating recipes and cookbooks:
mkdir cookbooks to create a parent directory for cookbooks.
cd cookbooks
chef generate cookbook test-cookbook generates new cookbook (apparently a directory) with essential initial files.
(optional) yum install tree -y to install tree which will help in understanding directory hierarchy.
chef generate recipe test-recipe (in test-cookbook directory), it creates a new recipe, apparently a .rb file.
cd ..  to go back
vi test-cookbook/recipes/test-recipe.rb command will open the editor for making changes or write code into the recipe.
Add some ruby code for automation. (see example down below).
chef exec ruby -c test-cookbook/recipes/test-recipe.rb checks the recipe syntax (desired output: Syntax OK).
chef-client -zr “recipe[test-cookbook::test-recipe]” will perform the operations according to0 recipe code.

Chef Attributes According to Priority (increasing order):
default
force-default
normal
override 
Force_override
automatic 


Example recipes:



file '/myfile' do
content 'Welcome to 19SW'
action :create
end

*********


package 'tree' do
action :install
end

file '/myfile2' do
content 'This is My Second Project code'
action :create
owner 'root'
group 'root'
end

*********
package 'httpd' do
action :install
end

file '/var/www/html/index.html' do
content 'Welcome to 19SW'
action :create
end


service 'httpd' do
action [:enable, :start]
end
