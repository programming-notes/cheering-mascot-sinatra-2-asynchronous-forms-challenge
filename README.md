# Deaf Sinatra 2 Asynchronous Forms 
 
##Learning Competencies 

##Summary 

 We're going to build on the previous [Deaf Sinatra](http://socrates.devbootcamp.com/challenges/268) challenge, this time using [jQuery](http://jquery.com/) and [AJAX](http://en.wikipedia.org/wiki/Ajax_%28programming%29) to submit our form rather than the default browser behavior.

## Learning Goal

The goal here is to see and feel the difference between the traditional (synchronous) nature of HTML forms and the asynchronous nature of AJAX:

- What does synchronous / asynchronous mean?
- How can one use jQuery to make an AJAX request?
- How can one use jQuery to update the DOM?

## Objectives

### Download the Skeleton Code

You're free to start from your earlier code.  Otherwise, you can [download the skeleton code again](http://cl.ly/0Z3z432M1T2s).

### application.js

All your JavaScript should go into `public/js/application.js`.  It should look something like this at first:

```javascript
$(document).ready(function() {
  // This is called after the document has loaded in its entirety
  // This guarantees that any elements we bind to will exist on the page
  // when we try to bind to them

  // See: http://docs.jquery.com/Tutorials:Introducing_$(document).ready()
});
```

### Implement an Asynchronous Deaf Grandma

Use the following jQuery methods to implement an asynchronous version of Deaf Grandma:

* [.submit()](http://api.jquery.com/submit/)
* [.serialize()](http://api.jquery.com/serialize/)
* [jQuery.post()](http://api.jquery.com/jQuery.post/)

Read up on how to [bind to events with jQuery](http://api.jquery.com/on/) if you need to.

You'll need to do five things:

1. Bind a callback to be triggered when your form is submitted
2. Serialize the data in the form to be submitted
3. Use jQuery's AJAX API to make a `POST` request to the server
4. When the server responds, update the page accordingly (this is the asynchronous part &mdash; you don't know when the server will respond)
5. Prevent the form to be submitted from submitting in the default way

### Submit Your Code

Only your `application.js` and `index.rb` file should have changed.  Upload those to a gist and submit them!

## What is AJAX?

The "A" in AJAX stands for asynchronous.  Under this model your browser sends an HTTP request to the server from inside the current page, via JavaScript.  Because we don't know when the web server will respond to our request &mdash; it might take 100 milliseconds or it might take 2 seconds &mdash; our browser can't "freeze up" and stop everything while we wait.  Instead, we write code in a style that permits the response to return at any time and with any data.

Think of it as the difference between a video call on Skype (synchronous) and email (asynchronous).  Or the difference between a restaurant that forces you to wait to be seated versus a restaurant that takes your name and phone number and offers to call you when your table is ready.  The former is easier for everyone to understand; there are fewer moving parts and it's easier to estimate when you'll be seated. But if the wait is long it becomes frustrating.  You can't go to a nearby bar while you're waiting.

When your browser is operating synchronously it has to sit and wait for the server to respond before it can do anything else.  This is how a browser normally works, by fetching or posting to a URL (via HTTP) and waiting for the response.  When your browser is operating asynchronously, it can send off a request at any time and continue on its merry way, but has to deal with the fact that the response could come back at any moment.

In a synchronous environment it's easy to handle errors, for example.  We submit a request, we wait to see whether it succeeds or fails, and display a message accordingly.  The world is stopped as the request is being processed.

In an asynchronous environment it's much more difficult.  We submit a request, but won't know when we'll know whether it succeeded or failed.  There's a period of time where the request is "unknown," which often means an extra state we have to display in our user interface, e.g., not just "succeeded" or "failed" but "in progress", "succeeded", or "failed". 

##Releases
###Release 0 

##Optimize Your Learning 

##Resources
