# API Test Cases

**Application / Website:** https://jsonplaceholder.typicode.com
**Environment:** Public API / Test



## TC-01: GET users API returns successful response

**Preconditions:**  
API endpoint is available

**Steps:**
1. Open Postman
2. Create a GET request to https://jsonplaceholder.typicode.com/users
3. Click Send

**Expected Result:**  
Request returns status code 200.  
Response body contains a list of user objects.

**Actual Result:**  
Request returned status code 200 OK.  
Response body contains a list of user objects.

**Status:**  
Pass


## TC-02: GET posts API returns successful response

**Preconditions:**  
API endpoint is available

**Steps:**
1. Open Postman
2. Create a GET request to https://jsonplaceholder.typicode.com/posts
3. Click Send

**Expected Result:**  
Request returns status code 200.  
Response body contains a list of post objects with fields `userId`, `id`, `title`, and `body`.

**Actual Result:**  
Request returned status code 200 OK.  
Response body contains an array of posts made by users, each with fields `userId`, `id`, `title`, and `body`.

**Status:**  
Pass


## TC-03: GET posts API with query parameter returns filtered results

**Preconditions:**  
API endpoint is available

**Steps:**
1. Open Postman
2. Create a GET request to https://jsonplaceholder.typicode.com/posts?userId=1
3. Click Send

**Expected Result:**  
Request returns status code 200.  
Response body contains only posts where `userId` equals 1.

**Actual Result:**  
Request returned status code 200 OK.  
Response body contains only posts made by `userId` 1.

**Status:**  
Pass


## TC-04: POST posts API creates a new post

**Preconditions:**  
API endpoint is available

**Steps:**
1. Open Postman
2. Create a POST request to https://jsonplaceholder.typicode.com/posts
3. In the request body, select **raw -> JSON** and enter:
```json

{
  "title": "Test Post",
  "body": "This is a test post",
  "userId": 1
}
```
**Expected Result:**
Request returns status code 201 Created.
Response body contains the post object with title, body, userId, and a new id.

**Actual Result:**
Request returned status code 201 Created.
Response body contains all four fields: title, body, userId, and id.

**Status:**
Pass


## TC-05: DELETE posts API deletes a post

**Preconditions:**  
A post with `id=1` exists on the API

**Steps:**
1. Open Postman
2. Create a DELETE request to https://jsonplaceholder.typicode.com/posts/1
3. Click Send

**Expected Result:**  
Request returns status code 200 OK or 204 No Content.  
The post with `id=1` is removed from the data (or API returns confirmation).

**Actual Result:**  
Request returned status code 200 OK.  
Response body was empty `{}`, indicating the post was deleted.

**Status:**  
Pass