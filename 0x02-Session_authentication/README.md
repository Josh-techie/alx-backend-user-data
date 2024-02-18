<p align="center">
<img src ="https://global-uploads.webflow.com/5ef788f07804fb7d78a4127a/5fabf0be9e750266c5fd10d0_authentication.png">
</p>

---

<h1> 0x02. Session authentication </h1>

- This project, entitled `0x02. Session Authentication`, delves into implementing a Session Authentication system without relying on external modules or frameworks. The focus is on understanding the mechanisms behind session authentication, including the use of cookies. The project builds upon the concepts covered in the previous project `0x00. Basic Authentication`

> By the end of this project you should be able to answer these questions:

- What authentication means
- What session authentication means
- What Cookies are
- How to send Cookies
- How to parse Cookies

---

<h1> Ressources </h1>

- [Flask-HTTPAuth-Documentation](https://flask-httpauth.readthedocs.io/en/latest/)
- [REST API Authentication Mechanisms](https://www.youtube.com/watch?v=501dpx2IjGY)
- [HTTP Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cookie)
- [Flask](https://palletsprojects.com/p/flask/)
- [Flask Cookie](https://flask.palletsprojects.com/en/1.1.x/quickstart/#cookies)

---

<h2> Tasks</h2>

**0: Et moi et moi et moi!**

- **Description:** Copy all the work from the previous `0x06. Basic authentication` project into this new folder. Ensure that all mandatory tasks of the previous project are completed at 100% because this project, as well as the rest of the track, will be based on it.

- **Files:** [app.py](./api/v1/app.py), [views/users.py](./api/v1/views/users.py)

**1: Empty session**

- **Description:** Create a class `SessionAuth` that inherits from `Auth`. Initially, this class will be empty.

- **Files:** [session_auth.py](./api/v1/auth/session_auth.py), [app.py](./api/v1/app.py)

**2: Create a session**

- **Description:** Update the `SessionAuth` class by adding a class attribute `user_id_by_session_id` initialized as an empty dictionary. Implement an instance method `create_session` that generates a Session ID for a given user ID. The Session ID is stored in the `user_id_by_session_id` dictionary. Return None for invalid inputs.

- **File:** [session_auth.py](./api/v1/auth/session_auth.py)

**3: User ID for Session ID**

- **Description:** Enhance the `SessionAuth` class with an instance method `user_id_for_session_id` that retrieves a User ID based on a given Session ID. Return None for invalid inputs.

- **File:** [session_auth.py](./api/v1/auth/session_auth.py)

**4: Session cookie**

- **Description:** Update `auth.py` in the `api/v1/auth` directory by adding a method `session_cookie` that extracts the Session ID cookie value from a given request. The cookie name is defined by the `SESSION_NAME` environment variable.

- **File:** [auth.py](./api/v1/auth/auth.py)

**5: Before request**

- **Description:** Modify the `@app.before_request` method in `app.py` to exclude the URL path `/api/v1/auth_session/login/` from authentication checks. If no authorization header or session cookie is present, abort with a 401 error.

- **File:** [app.py](./api/v1/app.py)

**6: Use Session ID for identifying a User**

- **Description:** Enhance the `SessionAuth` class with an overloaded instance method `current_user` that identifies a User based on the Session ID stored in the cookie. Retrieve the User instance from the database and set the session cookie in the response.

- **Files:** [session_auth.py](./api/v1/auth/session_auth.py), [views/session_auth.py](./api/v1/views/session_auth.py), [views/**init**.py](./api/v1/views/__init__.py)

**7: New view for Session Authentication**

- **Description:** Create a new Flask view that handles all routes for the Session authentication. In the file `api/v1/views/session_auth.py`, create a route `POST /auth_session/login` (= `POST /api/v1/auth_session/login`). Slash-tolerant. Use `request.form.get()` to retrieve email and password parameters.

- **Files:** [session_auth.py](./api/v1/auth/session_auth.py), [views/session_auth.py](./api/v1/views/session_auth.py), [views/**init**.py](./api/v1/views/__init__.py)

**8: Logout**

- **Description:** Update the `SessionAuth` class by adding a new method `destroy_session` that handles user logout by deleting the Session ID. Implement a new route `DELETE /api/v1/auth_session/logout` in `session_auth.py`.

- **Files:** [session_auth.py](./api/v1/auth/session_auth.py), [views/session_auth.py](./api/v1/views/session_auth.py)

**9: Expiration?**

- **Description:** Add an expiration date to Session IDs. Create a new class `SessionExpAuth` that inherits from `SessionAuth`. Implement methods for creating, retrieving, and destroying sessions based on expiration. Create `SessionDBAuth` that inherits from `SessionExpAuth`.

- **Files:** [session_exp_auth.py](./api/v1/auth/session_exp_auth.py), [session_db_auth.py](./api/v1/auth/session_db_auth.py), [app.py](./api/v1/app.py)

**10: Expiration?**

- **Description:** Create a new class `SessionExpAuth` that inherits from `SessionAuth`. Add an expiration date to Session IDs. Implement methods for creating, retrieving, and destroying sessions based on expiration. Create `SessionDBAuth` that inherits from `SessionExpAuth`.

- **Files:** [session_exp_auth.py](./api/v1/auth/session_exp_auth.py), [session_db_auth.py](./api/v1/auth/session_db_auth.py), [app.py](./api/v1/app.py)

---

<h1> Author </h1>

- [`@Josh-techie`]() | Software Engineer Student

  > Reach out to me if you need any help or have any questions.

  <a href="mailto:youssef.abouyahia@e-polytechnique.ma">
  	<img alt="Feel free to contact me" src="https://img.shields.io/badge/-Ask_me_anything-blue?style=flat&logo=Gmail&logoColor=white&link=mailto:youssef.abouyahia@e-polytechnique.ma&color=3d85c6" />
  </a>
  <span> | </span>
    <a href="https://www.linkedin.com/in/youssef-abouyahia/">
        <img alt="Linkedin Profile" src="https://img.shields.io/badge/-Linkedin-0072b1?style=flat&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/youssef-abouyahia/" />
    </a>
    <span> | </span>
    <a href="https://twitter.com/JoesephAb">
        <img alt="Twitter Profile" src="https://img.shields.io/badge/-Twitter-0072b1?style=flat&logo=Twitter&logoColor=white&link=https://twitter.com/JoesephAb&color=1DA1F2" />
    </a>
