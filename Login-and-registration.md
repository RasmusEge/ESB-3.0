# ESB 4.0 tracking requirement document (WEB) - Login and Registration (create account) 
## login 
When a user logs in, the following event should be dispatched:

![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/74e4a114-5c9c-4926-989d-5b5486c933c6)

````
dataLayer.push({
     event: 'login'
     user_id: CID-122112112 // dynamic value for specific user added when user creates account the first time (this is already implemented on the current site - Hiroshi did the implementation) - users_id should be added to datalayer at all times for all events - if not there simply provide blanc 
     login_status: 'Logged in' // Userstate should be added to datalayer at all times for all events 
 }); 
````
## Registration (create account)
When a user creates an account, the following event should be dispatched:
![image](https://github.com/RasmusEge/ESB-3.0/assets/122262884/6ede9457-d486-4907-a2de-d72335eb99a6)

````
dataLayer.push({
     event: 'create_account' // event on the current site is called "free signup" where the is id passed with an ecommerce event, that should not be necessarry on this site  
     user_id: CID-122112112 // dynamic value for specific user added when user creates account the first time (this is already implemented on the current site - Hiroshi did the implementation) - users_id should be added to datalayer at all times for all events - if not there simply provide blanck 
     login_status: 'Logged in' // Userstate should be added to datalayer at all times for all events 
 }); 
````

Userstate and user_id should be added to datalayer at all times 

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


