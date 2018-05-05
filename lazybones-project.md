# Lazybones

**Setup Lazybones on your machine **

**1.Run following commands in terminal
**Get sdkman **
'''
curl -s "https://get.sdkman.io" | bash 
'''
**Initiate sdkman**
'''
* source ~/.sdkman/bin/sdkman-init.sh
'''
**Install Lazybones using sdkman **
'''
sdk install lazybones
'''



**2.Create Lazybones project
lazybones create aem-multimodule-project my-project

*Maven group ID for the generated project : com.organizationname.groupname
*Maven artifact ID for the generated reactor project : projectname
*Maven artifact ID for the generated bundle module : projectname.core
*Maven artifact ID for the generated content package module : projectname.ui.apps


