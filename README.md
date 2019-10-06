Objectives :

**Jackson**

1) Convert JSON into Object or Convert Object into JSON -- Jackson library ( ObjectMapper )
2) Use : 
2.a) Rest api response comes in JSON and we need to parse it using Jackon library so we can map to Class object
2.b) Rest api request body needs to be sent in JSON for POST/PUT method so we need to convert class object into JSON and then send it.

**HttpUrlConnection Library ( default in JRE):**

It is used to invoke http request
1) Request
1.a) Set Request method : it can be GET,POST, PUT, DELETE etc
1.b) Set RequestProperty : Accept:application/json, Content:application/json
1.c) Set DoOutput to true
1.d) to send request body as JSON, we need to use getOutputStream();

2) Response
2.a) Response comes in getInputStream() as JSON string.
2.b) Using Jackson, will convert into class object

**Jersey:**

3.1) This library is used to create REST api
3.2) We need to use following annotations:


**Create RestAPI**

1) Configure Tomcat in Eclipse
2) Create Web DynamicProject
2.a)@POST, @GET, @DELETE, @PUT
2.b)@Path("add") - 
	@Consumes({MediaType.APPLICATION_JSON})
	@Produces({MediaType.APPLICATION_JSON})
  MethodName(@PathParam("id") int id) in case of @Path("delete/{id}")
3) Run Dynamic porject as "Run on Server" option so it will run on tomcat
4) Test Rest api endpoints using Postman

