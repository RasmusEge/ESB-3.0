# ESB 3.0 tracking requirement document (WEB) | Ecommerce 
This document contains datalayer tracking requirements for ecommerce events on https://stage-frontend4.europeanspermbank.com (also to be used on the live site)


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
Detailed below are all ecommerce events and parameters for the checkout journey, from view item to purchase 

Generic Google documentation: [https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag)

## Items array
#### Items array is used throughout all ecommerce events and includes all items in a purchase for both chekout 1 and 2    
````javascript
items: [
    {
      item_id: "SKU_12345", //Example - must be uniqie ID for product
      item_name: "Jatin IUI MOTO20+", // dynamic value for name
      affiliation: "ESB",
      index: 0,
      item_category: "brown", // dynamic value for eye color
      item_category2: "strawberry blond", // dynamic value for hair color
      item_category3: "180", // dynamic value for height
      item_category4: "dutch/danish", // dynamic value for ethnicity
      item_category5: "fair", // dynamic value for skintone 
      item_category6: "libra", // dynamic value for Zodiac
      item_category7: "ISJD", // dynamic value for personality 
      price: 7312.75, // Dynamic value for price 
      quantity: 2
    },
   
    {
      item_id: "SKU_123425", // dynamic ID-value for product
      item_name: "Pregnancy slot", // dynamic value for name
      affiliation: "ESB",
      index: 1,
      price: 3259.37, // Dynamic value for price 
      quantity: 1
    }, 

    {
      item_id: "SKU_123415", // dynamic ID-value for product
      item_name: "GeneXmatch", // dynamic value for name
      affiliation: "ESB",
      index: 1,
      price: 3259.37, // Dynamic value for price 
      quantity: 1
    }
         {
      item_id: "SKU_123415", // dynamic ID-value for product
      item_name: "3 years storage", // dynamic value for name
      affiliation: "ESB",
      index: 1,
      price: 3012.37, // Dynamic value for price 
      quantity: 1
    }

]
````

## Select item
#### Send event when user clicks on a donor and when a user chooses a donor

![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/529951fa-ef8d-4023-ae66-abf0c19e21e0)
![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/eecbce72-80a8-45bf-b8f3-643885c0b8cb)

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

 