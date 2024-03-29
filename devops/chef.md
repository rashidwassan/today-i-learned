# Chef
Progress Chef is a configuration management tool written in Ruby and Erlang. It uses a pure-Ruby, domain-specific language for writing system configuration "recipes". Chef can be integrated with various cloud services as well.

- System Administrators were used to manage, troubleshoot, and monitor servers and networks.
- In 2005 a new CMT (configuration management tool)  was built, called marionette. Now known as Chef.
- CMT is a tool to automate admin tasks.
- It is an IaC (infrastructure as code).
- Puppet was used befo4re Chef, now it is mostly replaced.
- Ohai is a simple database containing current configuration.
- Knife CLI tool, which is responsible for data transmissions in Chef Infrastructure.
- Idempotency avoidance of running redundant code again & again.
- Bootstrap is a term used for the node-server connection process.
- Chef Supermarket place to get ready-made cookbooks and recipes.
- Recipe is a file where you write Ruby code.

### Advantages of Chef
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

### Configuration Management Tools are of two types
- Pull Based: Chef, Puppet. Node will pull the recipe.
- Push Based: Ansible, SaltStack. Server will push the recipe.

### Setting up Chef and Creating and Executing Recipes: 
- Install Chef by copying the download link of the installer for Ubuntu.
- Use wget to download the installer.- 
- Use yum to install the Chef.
- which chef to see where it is located.

### Creating recipes and cookbooks:
- 'mkdir cookbooks' to create a parent directory for cookbooks.
- cd cookbooks
- chef generate cookbook test-cookbook generates new cookbook (apparently a directory) with essential initial files.
- (optional) yum install tree -y to install tree which will help in understanding directory hierarchy.
- chef generate recipe test-recipe (in test-cookbook directory), it creates a new recipe, apparently a .rb file.
- cd ..  to go back
- vi test-cookbook/recipes/test-recipe.rb command will open the editor for making changes or write code into the recipe.
- Add some ruby code for automation. (see example down below).
- chef exec ruby -c test-cookbook/recipes/test-recipe.rb checks the recipe syntax (desired output: Syntax OK).
- chef-client -zr “recipe[test-cookbook::test-recipe]” will perform the operations according to0 recipe code.

### Example recipes:

This recipe creates a file and adding 'Welcome to 19SW' as content.
```
file '/myfile' do
content 'Welcome to 19SW'
action :create
end
```

This recipe is for installing 'tree' package.
```
package 'tree' do
action :install
end
```

This recipe creates a file and changes owners.
```
file '/myfile2' do
content 'This is My Second Project code'
action :create
owner 'root'
group 'root'
end
```

Recipe for installing apache server.
```
package 'httpd' do
action :install
end
```

This is the recipe for creating an html file.
```
file '/var/www/html/index.html' do
content 'Welcome to 19SW'
action :create
end
```

Recipe for starting apache server.
```
service 'httpd' do
action [:enable, :start]
end
```

## Chef as IaC
- Before IaC - VMs were managed manually and infrastructure was scaled up and down all manually, even the settings were also manually managed.
- But now as IaC, we define our infrastructure as JSON or YAML file. Since there are only few files, these can be moved to more systems easily.
- Efficient, error-free, affordable. VCS support. Chef is one of the most common IaC tools.
- Pros: Saves a lot of money, faster & more efficient, consistency and accountability.
- Cons: Configuration drift, Re-execution takes a lot of time, & Understanding the code.
- IaC or Infrastructure as Code means managing the infrastructure using code. 

## Chef Attributes
- An attribute is a specific detail about a node. Attributes are used by Chef Infra Client to understand:
- The current state of the node
- What the state of the node was at the end of the previous Chef Infra Client run
- What the state of the node should be at the end of the current Chef Infra Client run
- Attributes are key value pairs and are used like variables in programming.
### Chef Attributes According to Priority (increasing order):
- default
- force-default
- normal
- override 
- force_override
- automatic 

## Bootstraping in Chef
Bootstrapping is the process to connect the node the first time to the Chef server, or to attach it again if the node lost the connectivity to the Chef server. To be able to bootstrap a node, your workstation needs to have the Chef Development Kit installed.

### Setting up Chef Workstation:
- First, we will have to navigate to Chef's official website and get the link of Chef workstation setup file for Linux.
- Using wget command, download the setup file in your ec2 instance.
- use yum install xyz.deb to install chef workstation.
- create some cookbooks and recipes (optional).
  
### Setting up Chef Server:
- On the same machine where workstation is installed.
- knife ssl check (to check if workstation is connected to server or not)
- visit manage.chef.io and create an account.
- Download chef-starter.zip after signing up.
- Chef-starter contains chef-repo (.chef, cookbooks, roles).
- Download WinSCP and login to your Linux machine (server).
- Copy chef-repo to server using WinSCP (drag & drop).
- Now the chef-repo/.chef/ contains config.rb which has the URL.
- To check chef-server-URL
  ```
  cat config.rb 
  ```

### Checking The Connection
To check the connection, run:
```
 knife ssl check
```
- it should give o/p 'successfully verified certificates from 'api.chef.io''.

### At this point, our workstation is connected to server.

## Setting Up a Node (connecting node with server)
- Make sure the node should be in same availability zone.
- Now and onwards, we will be working in chef-repo.
- Create a new Linux machine (node) in same availability zone.
- Add these commands in advanced details while creating machine.
  ```
  #!bin/bash
  sudo su
  yum update -y
  ```
- Although we have to connect node with workstation, the bootstraping command will always be run on workstation.
Now go to workstation and run 
  ```
  [chef-repo]# knife bootstrap <PrivateIP> --ssl-user ec2-user -- sudo -i node-key.pem -N node1
  ```
- Remember that the node-key.pem has been downloaded from node1 and transferred to chef workstation.
  
### Checking if Node is connected to server
```
[chef-repo]# knife node list
```
Displays the nodes connected to the server.

## Now: Workstation -> Server -> Node

### Cookbooks Directory
- We should have only one cookbooks directory to avoid confusions, the best place is to store cookbooks in chef-repo/cookbooks as we cannot delete this directory.

## Uploading cookbooks to chef server from workstation

To upload cookbook from workstation to server, use:
```
[chef-repo]# knife cookbook upload <cookbook-name>
```
To check if the upload was successful:
```
[chef-repo]# knife cookbook list
```

## Run List
We might have lots of recipes on our server and not all the nodes require all the repositories. To avoid overheads, we can set run lists for each node, associating specific recipes to it.
To attach a recipe to a node:
```
[chef-repo]# knife node run_list set node1 "recipe[cookbookName::recipeName]"
```
To check the run list of a node:
```
[chef-repo]# knife node show node1
```

## Updating Node
Now we will get the access of node and run chef-client in order to sync changes.

## Scheduling the process on node
To schedule chef-client updates
```
[node-1]# vi etc/crontab
```
To update every minute: Add this as the last line:
```
* * * * * root chef-client
```

### We will always have to manually upload the cookbook updates to server
