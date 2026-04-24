TAGS:: #javascript, #NestJS 
STATUS:: [[ongoing]] 
CREATED:: [[9th Apr 2026]]

- **Observable** : the stream of value
- **Operator** : that operate on the stream of value
- **Subscribe** : those which subscribe. duh!? More like for ever value emitted by observable run this function.
-
- # Subscribe and execution
	- ```javascript
	  //the idea being that there is not execution that happens till we subscribe
	  //and each subscription would be its own execution context
	  
	  obs.subscribe(fn1);
	  obs.subscribe(fn2);
	  //these would have their own independent execution context.	
	  ```
	- ### Hot and Cold observable
	  collapsed:: true
		- By default, the moment we ==subscribe== to an ==observable== 3 we start a new execution context but it is possible that we don't want a new execution context
		- For that we use ==subject==,(which can act both as an observable and an observer i.e. it can both push value -- like an observable and it can also be subscribed to.
		- ```javascript
		  const sub = new Subject();
		  
		  sub.subscribe(console.log);
		  sub.subscribe((x)=>{console.log(x*2)});
		  
		  sub.next(1);
		  ```