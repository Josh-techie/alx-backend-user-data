<p align="center">
<img src ="https://www.deepwatch.com/wp-content/uploads/blog-password-incorrect-1.jpeg">

---

<h1> User authentication service </h1>

- In this project entitled **0x03-user_authentication_service**, we'll explore the authentication process by manually implementing **Basic Authentication** in a simple `API`. You'll gain practical experience in managing user credentials, securing routes, and validating access to resources. By the end, you'll have a solid grasp of the principles behind Basic Authentication and its application in a web API context.

---

<h2> Resources </h2>

- You're invited to consult, read or watch these resources:
  - [Flask documentation](https://flask.palletsprojects.com/en/1.1.x/quickstart/)
  - [Requests module](https://requests.kennethreitz.org/en/latest/user/quickstart/)
  - [HTTP status codes](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)
  - [mapping declaration](https://docs.sqlalchemy.org/en/13/orm/tutorial.html#declare-a-mapping)

---

<h2> Tasks </h2>

1. **Task: User model**

   - **Description:** Create a SQLAlchemy model named User for a database table named users with specific attributes.
   - **Files:** [0x03-user_authentication_service/user.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/user.py)

2. **Task: Create user**

   - **Description:** Implement the `add_user` method in the provided DB class to add a user to the database.
   - **Files:** [0x03-user_authentication_service/db.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/db.py)

3. **Task: Find user**

   - **Description:** Implement the `find_user_by` method in the DB class to find a user based on arbitrary keyword arguments.
   - **Files:** [0x03-user_authentication_service/db.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/db.py)

4. **Task: Update user**

   - **Description:** Implement the `update_user` method in the DB class to update user attributes.
   - **Files:** [0x03-user_authentication_service/db.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/db.py)

5. **Task: Hash password**

   - **Description:** Define a `_hash_password` method to hash a password using bcrypt.
   - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

6. **Task: Register user**

   - **Description:** Implement the `register_user` method in the Auth class to register a user, hash the password, and save to the database.
   - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

7. **Task: Basic Flask app**

   - **Description:** Set up a basic Flask app with a single GET route ("/") returning a JSON payload.
   - **Files:** [0x03-user_authentication_service/app.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/app.py)

8. **Task: Register user (endpoint)**

   - **Description:** Implement the endpoint to register a user (POST /users) with error handling for existing users.
   - **Files:** [0x03-user_authentication_service/app.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/app.py)

9. **Task: Credentials validation**

   - **Description:** Implement the `valid_login` method in the Auth class to validate user credentials.
   - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

10. **Task: Generate UUIDs**

    - **Description:** Implement a `_generate_uuid` function in the auth module to generate a UUID string.
    - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

11. **Task: Get session ID**

    - **Description:** Implement the `create_session` method in the Auth class to create a session for a user.
    - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

12. **Task: Log in**

    - **Description:** Implement a login function to respond to the POST /sessions route, handling login and session creation.
    - **Files:** [0x03-user_authentication_service/app.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/app.py)

13. **Task: Find user by session ID**

    - **Description:** Implement the `get_user_from_session_id` method in the Auth class to find a user based on session ID.
    - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

14. **Task: Destroy session**

    - **Description:** Implement the `destroy_session` method in the Auth class to update a user's session ID to None.
    - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

15. **Task: Log out**

    - **Description:** Implement a logout function to respond to the DELETE /sessions route, handling session destruction.
    - **Files:** [0x03-user_authentication_service/app.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/app.py)

16. **Task: User profile**

    - **Description:** Implement a profile function to respond to the GET /profile route, providing user information based on the session ID.
    - **Files:** [0x03-user_authentication_service/app.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/app.py)

17. **Task: Generate reset password token**
    - **Description:** Implement the `get_reset_password_token` method in the Auth class to generate a reset password token.
    - **Files:** [0x03-user_authentication_service/auth.py](https://github.com/<username>/alx-backend-user-data/blob/main/0x03-user_authentication_service/auth.py)

---

<h2> Author </h2>

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
