TAGS:: #encryption, #SHA256 
STATUS:: [[ongoing]] 
CREATED:: [[22nd Apr 2026]]

- # Overview
	- Hash Based Message Authentication Code and Secure Hash Algorithm. Basically combining the concept of a secret key with my hashing algorithm
	- Instead of hash(message), it does two rounds of hashing -- hash(key_{2} + hash(key_{1} + message))
		- The inner key is being made by ipad(0x36 == 54) xoring it with key
		- The outer key is being made by opad(0x5c === 92) xoring it with key again creating the outer key.