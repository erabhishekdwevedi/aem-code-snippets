#Using HTL with Java Class 


###HTL Code
```
  <div data-sly-use.objectName="com.project.core.MyUseClass">
    	<p> Value from ${objectName.valueFromMyUseClass}
   </div>
```

###Java Code 
* It must extends WCMUsePojo or implments Use Interface.
* Java Class can be local or OSGi based

```
package com.project.core;

import com.adobe.cq.sightly.WCMUsePojo;

public class MyUseClass extends WCMUsePojo {

	public String valueFromMyUseClass = null;

	@Override
	public void activate() throws Exception {
  
   valueFromMyUseClass = "Hello I am from Use Class";		
	
  }

}

```
##You can also pass parameters from HTL to Java Class as arguments.

### HTL Code with parameter
```
  <div data-sly-use.objectName="{ 'com.project.core.MyUseClass' @parameter1='John' , parameter2='Doe'}">
    	<p> Value from ${objectName.combinedValue}
   </div>
```

###Java Code to accept Parameter from HTL
* It must extends WCMUsePojo or implments Use Interface.

```
package com.project.core;

import com.adobe.cq.sightly.WCMUsePojo;

public class MyUseClass extends WCMUsePojo {

	public String valueFromMyUseClass = "Welcome";

	@Override
	public void activate() throws Exception {
  
   String parameter1FromHTL = get("parameter1",String.class);
   String parameter2FromHTL = get("parameter2",String.class);
   
   combinedValue = valueFromMyUseClass + parameter1FromHTL + parameter2FromHTL ;		
	
  }

}

```
