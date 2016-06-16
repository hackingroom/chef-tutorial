## Chef tutorial

#### Install chef in your workstation
    $ curl -L https://www.opscode.com/chef/install.sh | bash

#### Setup lab
    $ vagrant up

#### Bootstrap a node(in this case our vagrant nodes) :sheep:
    $ knife bootstrap www.example.node.com -x user -P password -N nodename
