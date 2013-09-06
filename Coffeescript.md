CoffeeScript Memos
==================

####Check if DOM element is visible

	$(element).is(":hidden") 
	$(element).is(":visible")
[JQuery :hidden selector](http://api.jquery.com/hidden-selector/), [jQuery :visible selector](http://api.jquery.com/visible-selector/)

####Get the name of the file from an input

	$('input[type=file]').val().split('\\').pop()
	
####jQuery document ready

	$ ->
		doSomething()
		
####jQuery AJAX

	$.ajax
		url: "http://ajax.something.com"
	.done (data) ->
		console.log data

####setTimeout

	callback = ->
		# do something
	setTimeout callback, 1000		