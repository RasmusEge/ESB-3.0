# ESB 3.0 tracking requirement document (WEB) - Forms
This document contains tracking requirements for form events for https:https://stage-frontend4.europeanspermbank.com

## Table of content
[**1. Form tracking**](#form-tracking) <br/>
[1.1 Form views](#form-view) <br/>
[1.2 Form start](#form-start) <br/>
[1.3 Form submit](#form-submit) <br/>
[1.4 Form success](#form-success) <br/>

## Form tracking
All error events and parameters are detailed in the following

## Form view
#### When users views a form in the browser    

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'Form view',
 'formLocation': 'footer' // or content blok (if something exists)
 'formType': 'newsletter form' // incert dynamic value 
 'formName':'newsletter' // incert dynamic value
 'formID': '12343535' //  incert dynamic value
 });
 
````

## Form start
#### When users start filling out forms  

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'Form start',
 'formLocation': 'footer' // or content blok (if something exists)
 'formType': 'newsletter form' // incert dynamic value 
 'formName':'newsletter' // incert dynamic value
 'formID': '12343535' //  incert dynamic value
 });
 
````

## Form submit
#### When users submit forms  

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'Form submit',
 'formLocation': 'footer' // or content blok (if something exists)
 'formType': 'newsletter form' // incert dynamic value 
 'formName':'newsletter' // incert dynamic value
 'formID': '12343535' //  incert dynamic value
 });
 
````

## Form success
#### When users submit forms  

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'Form success',
 'formLocation': 'footer' // or content blok (if something exists)
 'formType': 'newsletter form' // incert dynamic value 
 'formName':'newsletter' // incert dynamic value
 'formID': '12343535' //  incert dynamic value
 });
 
````
 'formID': '12343535' //  incert dynamic value
 });
 
````


