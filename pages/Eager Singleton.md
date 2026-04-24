TAGS:: #[[Creational Design Pattern]], #Singleton 
STATUS:: [[eternal]] 
CREATED:: [[16th Apr 2026]]

- Eager singleton instantiates an instance of the class at the time of loading the class. The most basic form of singleton pattern. Has a lot of overhead
- ```javascript
  class EagerSingleton{
    private static instance: EagerSingleton|null;
  
  	constructor(){}
  	
  	static getInstance(){
        return this.instance;
      }
  }
  ```