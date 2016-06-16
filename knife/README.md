# Chef workstation Knife

__knife is the command line tool used to provide an interface between your local chef-repo and the chef-server__
* Creating cookbooks
* Uploading cookbooks to chef servers
* Managing roles and run_list
* Searching chef-server node objects data
* Bootstrap nodes
* Essentially everything to do as a devops admin

## Using knife to bootstrap a node
```$ knife bootstrap <address> -x user -P password -N nodename```

* For statring in this course we will define a node name
* In production it is best practice not to define -N and let the FQDN work as the node name
