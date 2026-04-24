TAGS:: #[[Creational Design Pattern]], #Singleton 
STATUS:: [[eternal]] 
CREATED:: [[16th Apr 2026]]

- Here the idea is to prevent race conditions or state mutation while we were acquiring the lock. Hence we check twice whether the instance exists or not.
- ```javascript
  class DoubleLockSingleton{
    private static instance:DoubleLockSingleton|null;
  
  	constructor(){}
  	
  	if(this.instance==null){
        //acquire lock -- but in this process some other thread might've created the instance
        if(this.instanc)
      }
  }
  ```