# Postman exercise solutions

## Create a Collection

 - Click + sign on the left.
 - Enter any name for the collection (like **Github requests**) 

## E1 Retrieve User Profile

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve User Profile**).
 - Enter URL as https://api.github.com/users/:username
 - Click on **Params** tab. 
 - Enter path variable with **key**=*username*, **value**=*spring-projects*
 -  Click **Send**.
 - Verify that the response returns a *200 OK* status with appropriate data.


## E2 Retrieve information about a repository

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve Repository Information**).
 - Enter URL as https://api.github.com/repos/:username/:reponame .
 - Click on **Params** tab. 
 - Enter the following path variables:
 	 - **key**=*username*, **value**=*spring-projects*
	 - **key**=*reponame*, **value**=*spring-framework*
 - Click **Send**
 - Verify that the response returns a *200 OK* status with appropriate data.

## E3 Retrieve repositories for a user where user is an owner

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve repos with user type owner**).
 - Enter URL as https://api.github.com/users/:username/repos.
 - Click on **Params** tab. 
 - Enter the following path variables:
 	 - **key**=*username*, **value**=*spring-projects*
	 - **key**=*reponame*, **value**=*spring-framework*
 - Enter the following query variable:
	 - **key**=*type*, **value**=*owner*
 - Click **Send**
 - Verify that the response returns a *200 OK* status with appropriate data.

## E4 Create a repository

- Open your Github page and create a personal access token via **Settings > Developer Settings > Personal Access Token**.
 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Create Repository**).
 - Enter URL as https://api.github.com/user/repos.
 - Click on **Authorization** tab.
 - Select **Type** as *Basic Auth*.
 - Enter your Github user id as the **username** and the token obtained in step 1 as the **password**.
 - Click on **Body** tab.
 - Click the **raw** radio button and select **JSON** in the drop down.
 - Enter the following body:
```
 {
  "name": "test-repo",
  "private": true
}
```
 - Click **Send**
 - Verify that the response returns a *201 Created* status with appropriate data.
 - Go to your Github page and verify that the test-repo is created and is private.
