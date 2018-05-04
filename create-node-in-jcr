###Sample Pseudo-Code to Create Node in JCR with some properties

@Reference
ResourceResolverFactory resolverFactory;
ResourceResolver resolver = null;

Map<String, Object> param = new HashMap<String, Object>();
param.put(ResourceResolverFactory.SUBSERVICE, "bomwriter");
resolver = resolverFactory.getServiceResourceResolver(param);

Map<String,Object> properties = new HashMap<String,Object>();
properties.put("jcr:primaryType", "nt:unstructured");
properties.put("sling:resourceType", "apps/project/component/componentname");

Resource root = resolver.getResource("/content/myproject");
resolver.create(root, "name of node", properties);

resolver.commit();

resolver.close();


// It is sample code 
