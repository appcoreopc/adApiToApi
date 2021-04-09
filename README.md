# adApiToApi


## Using AD to integrated app to App service. 

### New Registration App 

In this approach we will be setting up Appservice which creates App registration Id automatically - which can be helpful. 

1. create your app service 
2. next, from your appservice -> authentication -> Add identify provider and choose Microsoft Active Directory
3. by default new App registration will be selected. Give it a name or use the default. 
4. click next and you can "Add Permission or Scope" to it.


### Using exising App Registration -> more steps :) 


### Client app registration configuration 

1. Note your app service URL which can be something like this after you append it with some authorizaion info. 

https://contoso.azurewebsites.net/.auth/login/aad/callback

2. Goto Active Directory > App registrations > New registration.
3. Click create and note the AppId / Client Id. 
4. Select PI permissions > Add a permission > My APIs -> and this is where u select App Registration created above. 
5. Under Delegated permissions, select user_impersonation, and then select Add permissions.

Next, this is where this code comes into play..... getting the token which allows the client app to call the API.
