# Use Postman to interact with the GitHub API

Github provides a REST API which allows users to interact with Github programatically, access information about users, repositories, and do much more. You can read more about the Github API [here](https://docs.github.com/en/rest/reference).  In this exercise, you will be using Postman to execute some of the Github API methods.

## General Instructions
The following are some general instructions to work on these exercises. 
 - Use https://api.github.com as the base URL for each API method.
 - Execute each method via Postman and save the response in a text file.


## E1 Retrieve User Profile
Execute the [Get a user](https://docs.github.com/en/rest/reference/users#get-a-user) API method for the username *spring-projects*.

**Time**: ~ 15 minutes
**Level of difficulty**: Low

## E2 Retrieve information about a repository

Execute the [Get a Repository](https://docs.github.com/en/rest/reference/repos#get-a-repository) API method for username *spring-projects* and repository *spring-framework*.

**Time**: ~ 15 minutes
**Level of difficulty**: Low

## E3 Retrieve repositories for a user where user is an owner

Execute the  [List Repositories for User](https://docs.github.com/en/rest/reference/repos#list-repositories-for-a-user) API method for username *spring-projects*.

**Time**: ~ 15 minutes
**Level of difficulty**: Low

## E4 Create a repository

Execute the [Create Repository for authenticated user](https://docs.github.com/en/rest/reference/repos#create-a-repository-for-the-authenticated-user) API method via Postman. Create repository called **test-repo** which is **private**.   Go to your Github page and verify that the test-repo is created and is private.

**Time**: ~ 30 minutes
**Level of difficulty**: Medium

## E5 Update a repository

Execute the [Update Repository for authenticated user](https://docs.github.com/en/rest/reference/repos#update-a-repository) API method via Postman. Update the testrepo repository created in E4 as follows:

 - Change the repository name to **test-repo2**
 - Make repository **public**
 - Disable **issues** for the repository

Go to your Github page and verify that the **test-repo** is no longer present. Instead, you should see a **test-repo2** repository that is public and has issues disabled.

**Time**: ~ 30 minutes
**Level of difficulty**: Medium