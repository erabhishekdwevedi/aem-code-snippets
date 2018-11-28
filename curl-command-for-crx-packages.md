# Curl Command For CRX Packages / AEM Package / Package Manager

#Help Menu

```curl -u admin:admin http://localhost:4502/crx/packmgr/service.jsp?cmd=help ```

## List All Packages
```curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service.jsp?cmd=ls```

## Create a package on Author
```
curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service/.json/etc/packages/my_packages/testpackage?cmd=create -d packageName=1 -d groupName=my_packages
```

## Build Package

```curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service/.json/etc/packages/my_packages/1.zip?cmd=build```

## Download Package to Local Machine
```curl -u admin:admin http://localhost:4502/etc/packages/my_packages/1.zip > 1.zip```

## Install Package 
```curl -u admin:admin -F package=@"1.zip" http://localhost:4503/crx/packmgr/service/.json/?cmd=upload```

## Install Package on Publish
```curl -u admin:admin -X POST http://localhost:4503/crx/packmgr/service/.json/etc/packages/my_packages/1.zip?cmd=build```

## Uninstall Package

```curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service/.json/etc/packages/my_packages/1.zip?cmd=uninstall```

## Force Upload Package
```curl -u admin:admin -F force=true -F install=true -F package=@"1.zip" http://localhost:4503/crx/packmgr/service/.json/?cmd=upload```

## Delete Package
```curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service/.json/etc/packages/my_packages/1.zip?cmd=delete```
