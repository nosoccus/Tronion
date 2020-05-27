# 4. Add project specific functionality to SPA
> In scope of this lab students continue practice with single page application. SPA shall be
> extended with variant specific functionality using static layouts from lab #1. As a result 
> all features shall be implemented. Code shall meet requirements from lab #3.

## Required pages and functionality:

- ### SPA shall communicate with back end via REST interface:

   * [[requirement completed - routes]](https://github.com/nosoccus/Tronion/blob/master/server/routes.py)
   * [[requirement completed - socket.io server]](https://github.com/nosoccus/Tronion/blob/master/server/poll_api/endpoints.py)
   * [[requirement completed - socket.io client]](https://github.com/nosoccus/Tronion/tree/master/client/static/scripts/polls)

- ### Data exchange shall be done in JSON format:
   * [[requirement completed]](https://github.com/nosoccus/Tronion/blob/master/client/static/scripts/room/submit_request.js)
    ```javascript
    contentType: 'application/json; charset=UTF-8',
            data: JSON.stringify({
                'name': name,
                'description': description,
                'id_user': localStorage.getItem('id_user')
            }),
            dataType: "json",
            headers: {"auth_token": localStorage.getItem('auth_token')},
            success: function (data) {
                $('#msg').html('<span style="color: green;">Room created successfully</span>');
            }
    ```
  

- ### Shall be accessible on localhost:5000 address:
    * [[requirement completed]](http://127.0.0.1:5000/)

- ### Errors nor logs in console:
    * [requirement completed]
    * _Screenshot of console:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab4/img/console.png "Console")
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab4/img/console2.png "Console")
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab4/img/pyconsole.png "Console")

- ### Loading speed less than 4 seconds 
    * [requirement completed]
    
- ### At least 2 browsers supported 
    * [requirement completed]
    
- ### No commented code
    * [requirement not completed] - Comments are useful.
    
- ### Environment shall be easily set up by checkouting git repository and executing simple commands. Step-by-step instruction shall be documented in README.md file.
    * [requirement completed]
    
- ### After navigation to any page it should be displayed after a refresh. For example, you navigate to /users, press F5, /users page shall be displayed.
    * [requirement completed]
- ### Put presentation logic in the component class: for example, don’t make arithmetical operations in the template:
    * [requirement completed - template](https://github.com/nosoccus/Tronion/blob/master/client/templates/polls/results.html)
    * [requirement completed - script](https://github.com/nosoccus/Tronion/blob/master/client/static/scripts/polls/main.js)
    * _Screenshot:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab4/img/room.jpg "Room")
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab4/img/chart.png "Chart")
