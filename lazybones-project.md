# Lazybones
Lazybones is useful and flexible way of create aem projects. Unlike projects from maven archetype; lazybones project doesn't contain any sample content.

### Setup ###

**1.Run following commands in terminal
**Get sdkman **


curl -s "https://get.sdkman.io" | bash 

** Initiate sdkman **


source ~/.sdkman/bin/sdkman-init.sh


** Install Lazybones using sdkman **

sdk install lazybones



### Creat Project ###

lazybones create aem-multimodule-project my-project

-Maven group ID for the generated project : com.organizationname.groupname
-Maven artifact ID for the generated reactor project : projectname
-Maven artifact ID for the generated bundle module : projectname.core
-Maven artifact ID for the generated content package module : projectname.ui.apps




