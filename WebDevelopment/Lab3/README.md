# 3. Basic single page application with user management
> In scope of this lab students should practice working with front end frameworks. A single page
> application should be created based on a part of static templates from the previous lab.

## Requirements:

- ### Student shall choose a front end framework, setup the local environment, define routing and implement components.

   * [[requirement completed]](https://github.com/nosoccus/Tronion/tree/master/client/static/scripts). There are several frameworks in the project:
   
    [_**jQuery**_](https://api.jquery.com/) - is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.
    
    [_**Socket.io**_](https://socket.io/) - Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server.
    
    
    
- ### Following functionality shall be covered:

  * Login: [[requirement completed]](http://127.0.0.1:5000/login)
    * [Templates](https://github.com/nosoccus/Tronion/blob/master/client/templates/login/login.html) | [Scripts](https://github.com/nosoccus/Tronion/blob/master/client/static/scripts/login/login_request.js) | [Back-end](https://github.com/nosoccus/Tronion/blob/master/server/user_api/endpoints.py)
    * _Screenshot of login:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab3/img/login.png "Login")

  * Logout: [[requirement completed]](http://127.0.0.1:5000/logout)
    * [Templates](https://github.com/nosoccus/Tronion/blob/master/client/templates/login/logout.html) | [Scripts](https://github.com/nosoccus/Tronion/blob/master/client/static/scripts/login/logout_request.js) | [Back-end](https://github.com/nosoccus/Tronion/blob/master/server/user_api/endpoints.py)
    * _Screenshot of logout:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab3/img/logout.png "Logout")

  * User roles: [[requirement completed]]
    * [Templates](https://github.com/nosoccus/Tronion/blob/master/client/templates/room/manage.html) | [DB](https://github.com/nosoccus/Tronion/blob/master/create_db.sql) | [Back-end](https://github.com/nosoccus/Tronion/blob/master/server/room_api/endpoints.py)
    * _Screenshot of user roles:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab3/img/user.png "User roles")
  
  * User CRUD: [[requirement completed]]
    * [Templates](https://github.com/nosoccus/Tronion/tree/master/client/templates) | [Scripts](https://github.com/nosoccus/Tronion/tree/master/client/static/scripts) | [Back-end](https://github.com/nosoccus/Tronion/tree/master/server)
    * _Screenshot of user roles:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab3/img/register_crud.png "CRUD")
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab3/img/manage_crud.png "CRUD")
