# Chef workstation: Organization Starter Kit

* __Security considerations for validation.pem__
  - It should be removed first when the chef-client convergence runs
  - if chef-client locks then  is located on node if node is compromised then your entire infrastructure is compromised
  - chef-client (super market cookbook) provided this funcionality
  - Can always write your own recipe to remove validation.pem and run it first in the run_list
  ```ruby
     file "/etc/chef/validation.pem" do
        action :delete
     end
  ```
