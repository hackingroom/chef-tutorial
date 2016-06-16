# Data Bags

A data bag is a global variable that is stored in JSON data and accessible from he chef server. A data bag is indexed for searching
and can be loaded bu a recipe or accessed during search

### types of data stored in a data bag
* Users to be added to the system
* Admins to be added to sudo
* API/DB credentials (More secure and better than environment attributes for credentials)
* Much more
