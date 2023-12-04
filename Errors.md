# ESB tracking requirement document (WEB) - Errors
This document contains tracking requirements for error events for https://www.zoo.dk/

## Table of content
[**1. Error tracking**](#error-tracking) <br/>
[1.1 Form errors](#form-errors) <br/>
[1.2 Page errors](#page-errors) <br/>
[1.3 Server errors](#server-errors) <br/>
[1.4 Checkout errors](#checkout-errors) <br/>


## Error tracking
All error events and parameters are detailed in the following

Documentation: https://www.analyticsmania.com/post/tracking-errors-with-google-tag-manager/#checkout-errors

## Form errors
When eroor occours with Registration, login, signup (newsletter), booking forms, contact and d subscription forms

````javascript
<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'formType': 'booking' // this value should depends on the type of form, e.g Registration, contact etc. 
  'formID':  214521 // some ID
  'errorType': 'form error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'formField' 'email' some descriptive value about the error
  'formLocation' 'body' // should specify either header body or footer  
  'errorMessage' : 'email not valid' // some descriptive message about the error
});
</script>
````

## Page errors
When error occours with Page load 

````javascript
<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'errorType': 'page error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'errorMessage' : '404 - page couldnt be found' // some descriptive message about the error
});
</script>
````

## Server errors
When error occours with server response 

````javascript
<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'errorType': 'server error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'errorMessage' : '503 - the server is not ready to handle the request.' // some descriptive message about the error
});
</script>
````

##  Checkout errors
When error occours with checkout flow  

````javascript
<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'errorType': 'checkout error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'errorMessage' : 'payment declined' // some descriptive message about the error eg. payment cancelled,  
});
</script>
````
