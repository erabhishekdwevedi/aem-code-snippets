# Sample code to create node in JCR with some properties.

```

@Reference
ResourceResolverFactory resolverFactory;
ResourceResolver resolver = null;

Map<String, Object> param = new HashMap<String, Object>();
param.put(ResourceResolverFactory.SUBSERVICE, "systemuser");
resolver = resolverFactory.getServiceResourceResolver(param);

Map<String,Object> properties = new HashMap<String,Object>();
properties.put("jcr:primaryType", "nt:unstructured");
properties.put("sling:resourceType", "apps/project/component/componentname");

Resource root = resolver.getResource("/content/myproject");
resolver.create(root, "name of node", properties);

resolver.commit();

resolver.close();
```

**Note: You will also need to create _system user_, assign permission and map to service in osgi configuration

