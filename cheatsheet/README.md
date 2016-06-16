# Bootstrap a node:
    * knife bootstrap yourlabserver.com -x user -P password -N nodename

# Create a cookbook
   * knife cookbook create apache

# Upload a cookbook
    * knife cookbook upload apache

# Add run_list to a node
    * knife node run_list add yourlabserver.com "recipe[apache]"
    * knife node run_list add yourlabserver.com "recipe[security]" -b "recipe[apache]"

# Show node information
    * knife node show yourlabserver.com -a apache.sites

# Seach node information
    * knife search node "os:linux"
    * knife search node "os:*" -a platform

# Crate data bags
    * knife data bag create users
    * knife data bag create groups

# populate a data bag alreay created with a json file
    * knife data_bag from file groups sudores.json
    * knife data_bag from file users admin.json

# Create an environment
    * knife environment from file dev.rb
    * knife environment from file prod.rb

# List environments
    * knife environment list -w

# Compare environments
    * knife environment compare dev prod
    * knife environment compare --all

# Delete environments
    * knife environment delete dev

# Show information about an environment
    * knife environment show dev
    * knife environment show prod

# Create roles
    * knife role from file chef-repo/roles/webserver.rb

# List roles
    * knife role list -w

# Delete role
    * knife role delete webserver
