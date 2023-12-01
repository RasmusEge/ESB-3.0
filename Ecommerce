# Copenhagen ZOO tracking requirement document (WEB) Ecommerce 
This document contains datalayer tracking requirements for ecommerce events on https://www.zoo.dk/


## Table of content
[**1. Ecommerce tracking**](#ecommerce-tracking) <br/>
[1.1 Items array](#items-array) <br/>
[1.2 Select Item](#select-item) <br/>
[1.3 View Item](#view-item) <br/>
[1.4 Add to cart](#add-to-cart) <br/>
[1.5 View cart](#view-cart) <br/>
[1.6 Remove from cart](#remove-from-cart) <br/>
[1.7 Begin checkout](#begin-checkout) <br/>
[1.8 Add Contact info](#add-contact-info) *<br/>
[1.9 Add ZOO-event info](#add-zoo-event-info) *<br/>
[1.10 Add ZOO-card info](#add-zoo-card-info) *<br/>
[1.11 Add All info](#all-info-added) *<br/>
[1.12 Add Payment info](#add-payment-info) <br/>
[1.13 Purchase](#purchase) <br/>



## Ecommerce tracking
Detailed below are all ecommerce events and parameters for
checkout 1 - without zoo-card in the basket
checkout 2 - with a zoo-card in the basket

(*) Not sure the google API will accept these as ecommerce events, as they are custom and fall outside of the GA4 Ecommerce recommended event naming schema. If it isn't possible to collect these events in the ecommerce API, they should be sent as From_tracking events instead [https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/blob/main/Form_tracking] 

Google documentation: [https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag)

## Items array
#### Items array is used throughout all ecommerce events and includes all items in a purchase for both chekout 1 and 2    
````javascript
items: [
    {
      item_id: "SKU_12345",
      item_name: "ZOO-kort_voksen",
      affiliation: "CPH-ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100, // The discount per item
      index: 0,
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      price: 500.00, // The sale price is the per item list price (600.00) minus discount (100.00)
      quantity: 2
    },
   
    {
      item_id: "SKU_12345",
      item_name: "Billet_barn",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 1,
      item_category: "ZOO-billet",
      item_category2: "Barn",
      price: 200.00,
      quantity: 2
    }
     {
      item_id: "SKU_123456", // Id from backend 
      item_name: "Boerne-foeselsdag", // name from backend 
      discount: 500,
      index: 2,
      item_category: "ZOO-event",
      item_category2: "Barn",
      price: 275.00,
      quantity: 12
    }
         {
      item_id: "SKU_12345343", // Id from backend 
      item_name: "ZOO-camp 3 dage 10-12 aar", // name from backend 
      discount: 500,
      index: 3,
      item_category: "ZOO-event",
      item_category2: "Barn",
      price: 275.00,
      quantity: 12
    }

]
````

## Select item
#### Send event when user clicks on a product

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/3eacf1db-9a68-4ead-be29-52068b40b075)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'select_item',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
          }]    
     }
});
````

## View Item

#### Send event when a user a loads a productpage

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/93581eb9-6bc7-41ca-a74c-c13800c7e643)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'view_item',
  ecommerce: {
   items: [{ 
            // insert items array with dynamic values   
          }]    
     }
});
````

## Add to cart
#### Send event when a user succesfully adds product to cart

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/1ace11b2-1529-4b09-beb8-7e3f025b7b7f)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_to_cart',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
         }]    
     }
});  
````

## View cart
#### Send event when user views cart

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/22793fc5-bf2a-4111-a4c8-bd9ce2698828)
![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/e34ce553-9a61-49b2-8007-bad7f5458b93)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'view_cart',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
         }]    
     }
});
````

## Remove from cart
#### Send event when user removes product from cart

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/b27d2317-bc44-4b80-b9d1-59d5a0d7a8cd)
![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/5afcf372-e860-401e-86fd-4ad120550bfb)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'remove_from_cart',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Begin checkout
#### Send event when user starts checkout flow

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/4aaaf1dc-7fd0-43e9-843c-d0140a0b70dc)
![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/fa4c5f61-c94d-4208-b799-0cff874914ef)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'begin_checkout',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add contact info
#### Send event when user has successlfully added contact info 

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/625787b1-5d43-4194-bdce-80738f875835)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_contact_info',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add ZOO-event info
#### Send event when user has successlfully added all Zoo-event info 

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/9404f23f-8444-4cff-8c35-4dfb75590be1)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_zoo-event_info',
  zoo-event: 'boernefoedselsdag, ZOO camp' // incert dynamic varible(s)
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add ZOO-card info 
#### Send event when user has successlfully added all Zoo-event info 

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/95109b40-c32d-49ba-959f-d38c9253aaf2)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_zoo-card_info',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## All info added
#### Send event when user has successlfully added all info in all checkout forms exept for payment info

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/95109b40-c32d-49ba-959f-d38c9253aaf2)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_all-info',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add payment info 
#### Send event when user has successfully added payment info

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/c602a7e6-4196-431d-a6fb-2ca7d1c9423c)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_payment_info',
    ecommerce: {
    payment_type: "creditcard" // eller FF (forbrugsforeningenskort) 
      items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Purchase 
Send event when user has successfully made a purchase

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/58c261b5-5b1c-453c-981f-035946b60aa0)

````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'purchase',
    ecommerce: {
    currency: 'DKK',
    value: 116.47,
    tax: 7.18,
    shipping: 10.00
    transaction_id: 'p115-20202000',
    coupon: 'gavekort', // if there
      items: [{      
        item_id: "SKU_12345",
        item_name: "ZOO-kort_voksen",
        coupon: "gavekort",
        discount: 100, // The discount per item
        index: 0,
        item_category: "ZOO-Kort",
        item_category2: "Voksen",
        price: 500.00, // The sale price is the per item list price (600.00) minus discount (100.00)
        quantity: 2 // The number of items sold
        }]    
     }
});
````

 
