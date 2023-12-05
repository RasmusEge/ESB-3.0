# Login and Registration (create account) 
## login 
When a user logs in, the following event should be dispatched:

![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/74e4a114-5c9c-4926-989d-5b5486c933c6)

````
dataLayer.push({
     event: 'login'
     user_id: 122112112 // dynamic value for specific user added when user creates account the first time (this is already implemented on the current site - Hiroshi did the implementation) - users_id should be added to datalayer at all times for all events - if not there simply provide blanc 
     login_status: 'Logged in' // Userstate should be added to datalayer at all times for all events 
 }); 
````
## Registration (create account)
When a user creates an account, the following event should be dispatched:
![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/6ede9457-d486-4907-a2de-d72335eb99a6)

````
dataLayer.push({
     event: 'create_account'
     user_id: 122112112 // dynamic value for specific user added when user creates account the first time (this is already implemented on the current site - Hiroshi did the implementation) - users_id should be added to datalayer at all times for all events - if not there simply provide blanc 
    login_status: 'Logged in' // Userstate should be added to datalayer at all times for all events 
 }); 
````

Userstate should be added to datalayer at all times 

If user is logged in 

````
datalayer.push({
login_status: 'logged in'  
 }); 
````

If user is not logged in 

````
datalayer.push({
login_status: 'not logged in'  
 }); 
````

## Signup for newsletter

When the user  signs up for the newsletter, the following event should be dispatched:
![image.png](/.attachments/image-7b7e0d09-64e7-4022-9a65-357bf2845083.png)

````
dataLayer.push({
     event: 'newsletter signup'
     eventCategory: 'Signup',
     eventAction: 'newsletter',
     login_status: 'not logged in'

 }); 
````
