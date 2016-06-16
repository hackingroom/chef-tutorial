## Chef tutorial

#### Install chef in your workstation
    $ curl -L https://www.opscode.com/chef/install.sh | bash

#### Bootstrap a node
    $ knife bootstrap www.example.node.com -x root -P node_password -N give_a_name_to_the_node

#### Setup lab
    $ vagrant up
