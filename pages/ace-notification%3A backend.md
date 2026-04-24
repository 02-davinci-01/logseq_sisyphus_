TAGS:: #aceCloud #rxjs 
STATUS:: [[ongoing]] 
CREATED:: [[10th Apr 2026]]

- # SSE implementation
	- The idea behind the SSE implementation for notification is simple: to provide real-time-updates to users. Majorly it has 3 components:
		- **@SSE Decorator** : A native nestJS decorator that keeps an HTTP stream open, and expects an Observable i.e. A dynamic event emitting entity from rxjs.
		- **Subject** : A rxjs entity which acts both as an observable -- i.e. can be consumed, and a operator?