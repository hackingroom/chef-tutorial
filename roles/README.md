# Roles

__A role is a way to difine certain patterns and processes that exist across nodes in an organization
as belonging to a single job function__


* Up until this point we have assigned recipes to be run for each node
    - Instead of updating run_list for a node all we have to do is update a role on the server
    - Prevents us form having to manually touch all nodes that need the change

* A role is essentially a listing of recipes and attributes that are to be executed on a node

* Instead of assigning a run list for each node we assign the node a role

* A base role can be assigned inside of a roles run_list

## Role management with knife
* knife role create role_name
* Chef-repo/roles/rolename.rb
* knife role from file chef-repo/roles/rolename.rb
* knife role list -w (views a list of roles on a chef server)
* knife role delete role_name
