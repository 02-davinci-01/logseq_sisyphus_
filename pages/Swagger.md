- Converts code metadata into a standard API description then renders a UI on top of it.
- ## NestJS and Swagger
	- When we write @Get(), metadata is already added to the particular function. Something like:
	  
	  ```javascript
	  @Controller()
	  
	  @Get()
	  async getAllUser(){}
	  
	  //what nestJS stores is 
	  //Controller level metadata
	  Reflect.defineMetadata('path','user',UserController);
	  Reflect.defineMetadata('isController',true,UserController);
	  
	  //Function level
	  Reflect.defineMetadata('method','GET',UserController.prototype.getAllUser);
	  Reflect.defineMetadata('path','/',UserController.prototype.getAllUser);
	  ```
	- This metadata is then arranged into OpenAPI JSON which then rendered to the UI
	- The benefit is that as it is attached to code -- it doesn't go stale.