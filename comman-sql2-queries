== SQL2 Query Syntax == 

SELECT [propertynames or * ] 
FROM [nodetype]
AS alias 
WHERE ISDESCENDANTNODE('alias','path/to/search')
AND
CONTAINS ('propertyname','value to match')
ORDER BY [propertyname]

== Examples == 
1. To get all Pages
SELECT * FROM [cq:Page]

2. To get All Pages at specific Path
SELECT * FROM [cq:Page]
WHERE ISDESCENDANTNODE(node, "/search/in/path")

3. Get All pages which has hero image with file reference to specific image 

SELECT * FROM [cq:Page]
WHERE ISDESCENDANTNODE('object','/content/we-retail/')
AND [jcr:content/root/hero_image/fileReference] = '/content/dam/we-retail/en/activities/hiking-camping/trekker-ama-dablam.jpg'

4. Get All Pages under path where property matches some value.

SELECT * FROM [cq:Page] AS object 
WHERE ISDESCENDANTNODE('object','/content/we-retail/')
AND [jcr:content/root/hero_image/fileReference] LIKE '%trekker-ama-dablam.jpg%'



