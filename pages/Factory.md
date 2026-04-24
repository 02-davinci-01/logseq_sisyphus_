TAGS::  #[[Creational Design Pattern]] 
STATUS:: [[ongoing]] 
CREATED:: [[15th Apr 2026]]

- The factory pattern defines an interface for creating objects while allowing the classes to decide their own concrete implementation. A centralized factory which instantiates classes which hold the concrete implementation
- ### Problem
	- The bottleneck with the standard factory is the centralized creating class, which violates the OCP principal
- ## Code
	- ```javascript
	  //basic implementation using beyblade
	  //define a common interface for all beyblade
	  
	  interface Beyblade{
	    type:string;
	    animal:string;
	  }
	  
	  class Pegasus implements Beyblade{
	    private type="air";
	    private animal="horse";
	  
	  	constructor(){}
	  }
	  
	  class Ldrago implements Beyblade{
	    private type = "fire";
	    private animal = "dragon";
	  
	  	constructor(){}
	  }
	  
	  class BeybladeFactory {
	    
	    //static method for class level access
	    static create(name:string){
	      switch(type){
	        case "ldrago":
	          return new Ldrago();
	        
	        case "pegasus":
	          return new Pegasus();
	      }
	    }
	  }
	  ```
-
- # Types of Factory
	- ## [[Abstract Factory]]
	- ## [[Factory-Method]]