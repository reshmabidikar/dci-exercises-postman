# Postman exercise solutions

## Create a Collection

 - Click + sign on the left.
 - Enter any name for the collection (like **Github requests**) 

## E1 Retrieve User Profile

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve User Profile**).
 - Enter URL as https://api.github.com/users/:username
 - Click on **Params** tab. 
 - Enter path variable: *username:*
 -  Click **Send**.
 - Verify that the response includes the following information:


## E2 Retrieve information about a repository

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve Repository Information**).
 - Enter URL as https://api.github.com/repos/:username/:reponame .
 - Click on **Params** tab. 
 - Enter the following path variables:
 	 - username:
	 - reponame:
 - Click **Send**
 - Verify that the response includes the following information:

## E3 Retrieve repositories for a user where user is an owner

 - Right click on your collection and click on **Add Request**.
 - Enter any request name (like **Retrieve repos with user type owner**).
 - Enter URL as https://api.github.com/users/:username/repos.
 - Click on **Params** tab. 
 - Enter the following path variables:
	 - username:
	 - reponame:
 - Enter the following query variable:
	 - 	 *type*:*owner*
 - Click **Send**
 - Verify that the response includes the following information:

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
 - Verify that the response includes the following information: 
 - Go to your Github page and verify that the test-repo is created and is private.
