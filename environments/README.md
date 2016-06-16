# Environments: what are environments?

An environment is a way to map an organization real-life workflow to what can be confiured and managed using the Chef Server

Apply different cookbook versions to specific environments (dev/prod/staging/qa)

Define Environment level attributes

Environment allow sharing of cookbooks within an organization

### Creating Environments
* Environment information can be stored in JSON files or .rb files
* Environment will be located in chef-repo/environments

* Example dev.rb (development environment file)
```ruby
  name "dev"
  description "development environment"
  cookbook "security", "=0.1.0"
  cookbook "motd", "=0.2.0"
  cookbook "apache", "=0.2.0"
  override_attributes({
          "author" => {
              "name" => true
          }
  })
```

### Environment Attributes
Two types of attributes precedence can be set on the environment level
* A default attribute defined in the environment will take precedence over a default attribute defined in a cookbook attribute file
* Override has higher precedence than default, force_default, and normal


### Environments: Methods of assigning a node to an environment
* Modify the client.rb file with an environment variable
* Knife-flip to do it from the workstation
* Assign it manually on the node

