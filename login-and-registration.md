# Custom Events
## login 
When a user logs in, the following event should be dispatched:
 
![image.png](/.attachments/image-855dda4b-4324-46e8-9968-d7400de7d8ba.png)

````
dataLayer.push({
     event: 'login'
     eventCategory: 'Login',
     eventAction: 'Logged in'
 }); 
````
Userstate should be added to datalayer at all times 

<span style="color:red">🛈 **New comment:** This is currently not implemented:
</span> @<Apostolos Lalos> 

If user is logged in 

````
datalayer.push({
userstate: 'logged in'  
 }); 
````

If user is not logged in 

````
datalayer.push({
userstate: 'not logged in'  
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
     userstate: 'not logged in'

 }); 
````
