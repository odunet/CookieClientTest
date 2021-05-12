# Static Page used to test movement of Cookie to and from Express App

## Implementation
* The **From** button sends a POST request to the client with the expected payload. That is the {email: "email", password: "password"} Response: JSON obeject with the user details and the Token. Token stored in both:
1) Header: {'x-auth-token'}
2) cookie: {'x-auth-token'}

* The **To** button sends a Get request to the client **@route: /api/testCookieResponse**. Response object: JSON {message: "Cookie Recieved"}, the cookie stored in client shouls also be logged in server using **req.cookies['x-auth-token']**.