Angular-Dynamic-Forms
=====================

Example of Angular Form with Dynamically Generate Fields and working Validation

Problem
=======

Dynamically build forms seem to be considered an edge case for the current version of Angular.  If you use the naive implementation similar to:

	index-naive.html

you end up with some really strange results.  In your form you get something like:

	theForm.['theInput{{item.id}}'] = {...}

instead of the expected objects

	theForm.theInput1 = {};
	theForm.theInput2 = {};
	theForm.theInput3 = {};

This prevents you from writing per-field validation templates and screws with the data model synchronization.

Solution
========

Fortunately some people have started looking at this problem. See: 

	http://stackoverflow.com/questions/12044277/how-to-validate-inputs-dynamically-created-using-ng-repeat-ng-show-angular#24470458

What I present here is a more complete example of this style of system working in an angular application since I could not find such a working example.

I want to give a shout out to Al Johri from the article above for tweezing out this fix. 



