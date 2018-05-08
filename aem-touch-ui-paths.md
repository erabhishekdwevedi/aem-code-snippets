# Customizing AEM Touch UI 

You can use Sling Resource Merger to customize AEM Touch UI.
The default UI is defined under /libs/* directory , We need to overlay just the required node to /apps and customize as per our requirments.

Some useful Sling Resource Merget Properties

To hide children defined in libs
```
sling:hideChildren 
String[]
values can be name of children nodes or * for hiding all nodes.
```

To hide properties defined in libs.

```
sling:hideProperties
String[]
values can be e.g. ["jcr:description","xyz:prop2"] or * 
```

* AEM Default Landing page
```
/libs/cq/core/content/
/libs/cq/core/content/  - Navigation 
/libs/cq/core/content/
/libs/cq/core/content/welcome/favicon.ico/jcr:content - Logo
```

