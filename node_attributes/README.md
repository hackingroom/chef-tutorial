# Node - Attributes

__Attributes are specific details about a node__

### Attributes describe
* The current state of the node
* What the state of the node was at the end of the previous chef-client run
* What the state of the node should be at the end of the current chef-client run

### Attributes can be defined by
* The state of the node (ohai)
* Cookbooks (our attribute files)
* Roles
* Environments

### Attribute precedence
After the node object is rebuild in the chef run, all attributes loaded in the chef-client are then compared.
The node is updated based on attribute precedence and at the very end of the convergence(chief-client) the node object is
uploaded to the chef server

Node object defines the current state of the node(made up of attributes)
Node object is stored on the chief server so that can be searched
Node object is updated at each convergence

If there are attributes with the same names then attribute precedence determines which attribute is applied to the node and the node object.

* default
    Automatically reset at the start of every chef client run is the lowest precedence
* force_default
    Used in a cookbook or recipe to override an existing "default" attribute
* Normal
    A setting that persists in the node object
* Override
    Automatically reset at the start of every chef-client most often should be used only when required
* force_override
    Used to ensure thah an attribute defined in a cookbook(by an attribute file or by a recipe) takes precedence over an
    override attribute set by role or an environment
* Automatic
    Contains data populated bu Ohai at the beginning of every chef-client run and cannot be modified and always has the highest attribute precedence

### Node Object:
A node object is made up of the run lists which define what recipes to run during a chef-client as well as the attributes that define information about the node

### Attributes are built during the chef-client run process
* Data baout the node is collected by Ohai
* The node object previously saved during the last chef-client run
* The rebuilt node object from the current chef-client run

Once the node  object is rebuilt, all attributes are compared and then updated based on attribute precedence

At the end of every chef-client run the node object that defines the current state of the node is uploaded to the chef server to be searched
