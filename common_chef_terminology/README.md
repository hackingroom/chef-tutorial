# Common Chef Terminology

* __Recipes__:
    Fundamental configuration element within an organization
* __Cookbook__:
    Defines a scenario and is the fundamental unit of configuration and policy distribution
* __Chef-Client__:
    Agent that runs locally on the node that is registered with the chef server
* __Convergence__:
    Occurs when chef-client configures the system/node based on the information collected from chef server
* __Configuration Drift__:
    Occurs when the node state does not reflect the updated state of policies/configurations on the chef server
* __Resources__:
    A statement of configuration policy within a scope
    Describe the desired state of an element in the infrastructure and steps needed to configure
* __Provider__:
    Defines th steps thar are needed to bring the piece of the system from its current state to the desired state
* __Attributes__:
    Specific details about the node, used used by chef-client to understand current state of the node, the state of the node
    on the previous chef-client run, and the state of the node at the end of the client.
* __Data-bags__:
    Global variables stored as JSON data and is accessible from the chef server
* __Workstation__:
    A computer configured with knife and used to synchronize with the chef-repo and interact with chef-server
* __client.rb__:
    Configuration file fot chef-client locayed at /etc/chef/client.rb on each node
* __Ohai__:
    Tool used to detect atributes on a node an then provide attributed to chef-client at the start of every chef-client run
* __Node Object__:
    Consist of run-list and node attributes that describe states of the node
* __Chef-Repo__:
    Located on the workstation and installed with the starter kit, should be syncronyzed with version control system and stores
    Cookbooks, roles, data bags, environments, and configuration files
* __Organization__:
    Used in chef enterprise server to restrict access to objects, nodes environments, roles, data-bag etc
* __Environments__:
    Used to organize environments(Prod/Staging/Dev/QA) generally used with cookbook versions
* __Idempotence__:
    Means a recipe can run multiple times on the same system and the results will always be identical
