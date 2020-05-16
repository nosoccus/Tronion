# LAB 2. Client-server interaction in scope of SPA
> In scope of this lab students should practice fetching data from the back-end using AJAX.
> Student shall create application which makes requests to API (back-end from the previous 
> course can be reused) and displays parsed response

## Requirements:

- ### Pure JS, no jQuery or other libraries:

   * [[requirement completed]](https://github.com/nosoccus/Tronion/tree/master/client/static/scripts)
    ```javascript
    document.getElementById("join_button").onclick = function e() {
        e.preventDefault();
        var isLoggedIn = localStorage.getItem('loggedin');

        if (isLoggedIn == 1) {
            location.replace('/join');
        } else {
            location.replace('/login');
        }
    };
   ```
  
  
- ### window.fetch or XMLHttpRequest can be used for AJAX calls:

   * [[requirement completed]](https://github.com/nosoccus/Tronion/tree/master/client/static/scripts)

   ```javascript
  $(document).on('submit', '#room-form', function (e) {
    e.preventDefault();

    var name = $('#name').val();
    var description = $('#description').val();

    if (name != "" && description != "") {

        $.ajax({
            method: "POST",
            url: '/create_room',
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
            },
            statusCode: {
                400: function (data) {
                    $('#msg').html('<span style="color: red;">Bad request parameters</span>');
                    if (data.message == 'token expired' || 'Invalid token, please try again'){
                        localStorage.setItem('auth_token', 0);
                        location.replace('/login');
                    }
                }
            },
            error: function (err) {
                console.log(err);
            }
        });

    } else {
        $('#msg').html('<span style="color: red;">All fields are required</span>');
    }

  });
  ```
  
  
- ### At least 3 API endpoints are used:

   * [[requirement completed]](https://github.com/nosoccus/Tronion/blob/master/server/routes.py) (list of all endpoints, there are many 😉)
    ```python
   @app.route('/login')
    def login():
    return render_template('login/login.html')


  @app.route('/logout')
    def logout():
    return render_template('login/logout.html')


  @app.route('/register')
    def registration():
    return render_template('registration/registration.html')
  ```
  
  
- ### SPA shall communicate with back end via REST interface:

   * [[requirement completed]](https://github.com/nosoccus/Tronion/blob/master/server/routes.py)
  
  
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
  

- ### No errors nor logs in console:

   * [requirement completed]
   
   * _Screenshot of console:_
![alt-текст](https://github.com/nosoccus/Tronion/raw/master/WebDevelopment/Lab2/img/console.png "Console")


- ### Loading speed less than 4 seconds:

   * [requirement completed]


- ### At least 2 browsers supported:

   * [requirement completed]
   
   
- ### No commented code:

   * [requirement completed]
