TAGS:: #[[SDE Sheet]] 
STATUS:: [[ongoing]] 
CREATED:: [[22nd Apr 2026]]

- ## Dutch Algorithm
  collapsed:: true
	- The idea is to sort the three set of balls. Now instead of having another memory structure we wish to do it in place
	- Called the dutch algorithm because well dutch flag has 3 colors -- not to mention multiple countries have 3 colors.
	- A critical idea is not incrementing mid, when we swap the high -- for we don't know what is being returned there. Hence we just increment when we are sure the kind of ball/number that we are receiving.
	- ```c++
	  void dutchSort(vector<int>ball){
	    //we declare 3 pointers
	    int low =0,mid=0,high=ball.size()-1;
	    
	    //the key is to find the invariant
	    
	    while(mid<=high){
	      if(nums[mid]==0){
	        swap(nums[mid++],nums[low++]);
	      }
	      else if(nums[mid==2]){
	        swap(nums[mid],nums[high--]);
	      }
	      else{
	        mid++;
	      }
	    }
	  }
	  ```
- ## Buy & Sell stocks-1
	- Here again -- although we did get confused a bit -- the idea is quite simple. We start with the assumption that we have a stock. Now think about it -- the moment you find a smaller number -- you swap as if you had bought that stock instead. Why? because even if there is a greater element