# Postman exercise solutions

## Create a Collection

 1. Click + sign on the left.
 2. Enter any name for the collection (like **Github requests**) 

## E1 Retrieve User Profile

 1. Right click on your collection and click on **Add Request**.
 2. Enter any request name (like **Retrieve User Profile**).
 3. Enter URL as https://api.github.com/users/:username
 4. Click on **Params** tab. 
 5. Enter path variable with **key**=*username*, **value**=*spring-projects*
 6. Click **Send**.
 7. Verify that the response returns a *200 OK* status with appropriate data.

## E2 Retrieve information about a repository

 1. Right click on your collection and click on **Add Request**.
 2. Enter any request name (like **Retrieve Repository Information**).
 3. Enter URL as https://api.github.com/repos/:username/:reponame .
 4. Click on **Params** tab. 
 5. Enter the following path variables:
	 a. **key**=*username*, **value**=*spring-projects*
	 b. **key**=*reponame*, **value**=*spring-framework*
  6. Click **Send**.
  7. Verify that the response returns a *200 OK* status with appropriate data.

## E3 Retrieve repositories for a user where user is an owner

 1. Right click on your collection and click on **Add Request**.
 2. Enter any request name (like **Retrieve repos with user type owner**).
 3. Enter URL as https://api.github.com/users/:username/repos.
 4. Click on **Params** tab. 
 5. Enter the following path variables:
 
 	 a. **key**=*username*, **value**=*spring-projects*

 6.  Enter the following query variable:
 
	 a.  **key**=*type*, **value**=*owner*
 7. Click **Send**.
 8. Verify that the response returns a *200 OK* status with appropriate data.

## E4 Create a repository

 1. Open your Github page and create a personal access token via **Settings > Developer Settings > Personal Access Token**.
 2. Right click on your collection and click on **Add Request**.
 3. Enter any request name (like **Create Repository**).
 4. Enter URL as https://api.github.com/user/repos.
 5. Select request method as **POST**
 6. Click on **Authorization** tab.
 7. Select **Type** as *Basic Auth*.
 8. Enter your Github user id as the **username** and the token obtained in step 1 as the **password**.
 9. Click on **Body** tab.
 10. Click the **raw** radio button and select **JSON** in the drop down.
 11. Enter the following body:
```
 {
  "name": "test-repo",
  "private": true
}
```
12. Click **Send**
13. Verify that the response returns a *201 Created* status with appropriate data.
14. Go to your Github page and verify that the *test-repo* is created and is *private*.

## E5 Update a repository

1. Enter any request name (like **Create Repository**).
2. Enter URL as https://api.github.com/user/repos.
3. Select request method as **PATCH**
4. Click on **Authorization** tab.
5. Select **Type** as *Basic Auth*.
6. Enter your Github user id as the **username** and the token obtained in E4 Step 1 as the **password**.
7. Click on **Body** tab.
8. Click the **raw** radio button and select **JSON** in the drop down.
9. Enter the following body:
```
{
 "name": "test-repo2",
 "private": false,
 "has_issues":false
}
```
10. Click **Send**.
11. Verify that the response returns a *201 OK* status with appropriate data.
12. Go to your Github page and verify that the *test-repo* is no longer present. Instead, a repository called *test-repo2* should be created that is *public* and has *issues* disabled.