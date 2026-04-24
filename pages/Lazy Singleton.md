TAGS:: #Singleton, #[[Creational Design Pattern]] 
STATUS:: [[eternal]] 
CREATED:: [[15th Apr 2026]]

- Lazy singleton defers the creation of an instance till it is requested for the first time. This provides optimized creation of instance.
- ```javascript
  class LazySingleton{
    private static instance:LazySingleton|null;
  
  	constructor(){}
  
  	static getInstance{
        if(this.instance===null){
          this.instance = new LazySingleton();
          return this.instance;
        }
        return this.instance.
      }
  }
  ```
- ### Use Case
	- In multi-threaded operations