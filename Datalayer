## GTM Implementation: 

Developer instructions to implement Google Tag Manager across all pages
GTM container tag implementation guide
The Google Tag Manager container tag consists of two code snippets, which you can find below. 

Part1: Paste this code as high in the <head> of the page as possible:
````javascript
<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-MXM65VH');</script>
<!-- End Google Tag Manager -->
````
Part2:  Additionally, paste this code immediately after the opening <body> tag:
<!-- Google Tag Manager (noscript) -->
````javascript
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-MXM65VH"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
````
Install the snippets across all pages of the domain.
If you have any troubles implementing the data layer in the head section



## Data Layer Implementation: 

To ensure maximum flexibility, portability, and ease of implementation, Google Tag Manager functions best when deployed alongside a data layer.
A data layer is an array in the global scope across the website. It contains and passes all the information we want to use in Google Tag Manager.

There are **2 ways** to add data to the data layer:

1. You initialize the data layer at page load
2. You push data to the data layer at any other time

Adding data to a data layer is the equivalent of initiating an array with data or adding data to it via its push method.

### 1. Initialize the data layer
To set up your data layer, you need to add the following code snippet to the head section of the page – before the GTM snippet. 
The snippet must be implemented across all pages you you want Google Tag Manager to run on (mostly the entire domain).

````javascript
<script>
   window.dataLayer = window.dataLayer || [];
   window.dataLayer = [{
     ... // data for initialization. More about this later.
   }]; 
</script>
````
**It is important that the array is defined before the GTM library is loaded - hence the implementation before the GTM script tag in the head.**
> Example: Data layer implemented on a web page. The correct hierarchical order of implementation looks as follows:

````javascript
<head>
   <script>
   window.dataLayer = window.dataLayer || [];
   window.dataLayer = [{
         'pageType': 'homepage' // example key-value pair for illustration
      }]; 
   </script>
   <!-- Google Tag Manager Tag -->
   ...
   <!-- End Google Tag Manager -->
</head>
<body>
   <!-- Google Tag Manager noscript tag -->
   ...
   <!-- End Google Tag Manager -->
   ...
</body>
````

### Push data to the data layer
There are 2 ways to add data to the data layer:
At page load, via data layer "initiation" (above example)
After page load, with a data layer push
Adding data to a data layer is the equivalent of initiating an array with data or adding data to it via its push method.
As in the previous example, the push method uses JSON comma-separated pairs (Format: 'name': 'value'):
````javascript
   dataLayer.push({
      'variable-name': 'variable-value' // key and value are both in quotes
   });
````
### Push multiple variables together
Instead of using the data layer push method for each variable, just like when initializing the data layer; you can push multiple variables to the data layer:

````javascript
dataLayer.push({
      'eventCategory': 'variable-value',
      'eventAction': 'variable-value',
      'eventLabel': 'variable-value',
      'event': 'send-ga-event'
   });
````  

> Example: Data layer push as an onClick event

````javascript
<a 
   href="#" 
   target="_blank"
   onclick="dataLayer.push({
      'eventCategory': 'variable-value',
      'eventAction': 'variable-value',
      'eventLabel': 'variable-value',
      'event': 'send-ga-event'
   });"
   >Test</a>
````  


> Full Example with initiation and push

````javascript

<head>
  <!-- Datalayer initiation -->
  <script>
   window.dataLayer = window.dataLayer || [];
   window.dataLayer = [{
      'pageType': 'homepage'
   }]; 
  </script>
  <!-- End Datalayer initiation -->
​
  <!-- Google Tag Manager -->
  [<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-xxxxxx');</script>]
  <!-- End Google Tag Manager -->
</head>
​
<body>
   <!-- Google Tag Manager (noscript) -->
   [<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-xxxxx"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>]
   <!-- End Google Tag Manager (noscript) -->
​
  <!-- some content -->
   … 
  <!-- Datalayer push -->
  <script>
   window.dataLayer = window.dataLayer || [];
   window.dataLayer = [{'event': 'test-event'});        
  </script>
  <!-- End Datalayer push -->
</body>
````
​
### Common pitfalls
When implementing the data layer, keep the following in mind:

The dataLayer object name is case-sensitive
When referencing the data layer you must use the proper casing used when declaring the data layer.

````javascript
Datalayer.push({'variable-name': 'variable-value'});        //Not OK
````

````javascript
dataLayer.push({'variable-name': 'variable-value'});        //OK
````
Variable names must always be enclosed in quotes
To avoid any issues it is recommended that all keys and values are enclosed in quotes.

````javascript
dataLayer.push({variable-name: 'variable-value'});        //Not OK
````

````javascript
dataLayer.push({'variable-name': 'variable-value'});        //OK
````


