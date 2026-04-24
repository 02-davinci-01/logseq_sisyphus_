TAGS:: #[[Creational Design Pattern]], #Factory 
STATUS:: [[eternal]] 
CREATED:: [[17th Apr 2026]]

- # Definition
	- Factory method abandons the centralized factory approach, by delegating the creation of objects to the subclasses themselves.
	- There can be two major ideologies while implementing the Factory-Method:
		- Instantiation via Composition: We abandon the control of creation -- this is more along the lines of DI
		- Instantiation via inheritance: To control creation and to implement a particular flow -- GoF
- # Code
	- ```javascript
	  //writing both composition and inheritance logic. 
	  interface Beyblade{ //these are for concrete classes.
	    letItRip():string;
	  }
	  
	  abstract class BeybladeCreator {
	   	private BeybladeInstance:Beyblade;
	    createBeyblade: Beyblade;
	    
	    letItRip(){
	      this.BeybladeInstance = this.createBeyblade();
	      return BeybladeInstance.letItRip();
	    }
	  }
	  
	  //it would be good to note that the only difference between this and the abstract factory is the onus of responsibility handled by it. 
	  ```
	-
	-