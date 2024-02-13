<p align="center">
<img src ="https://www.joshualowcock.com/wp-content/uploads/2022/01/birthday-privacy-meme.png">
</p>

---

<p align="center">
<h1> Personal data </h1>
</p>

- This project focuses on handling personal data securely and responsibly. The tasks involve implementing features like obfuscating Personally Identifiable Information (PII) in log messages, creating a custom log formatter, setting up a logger with redaction for PII fields, connecting to a secure database, and implementing password encryption and validation.

---

<h2> Resources </h2>

To successfully navigate through this project, make sure to read or watch the following resources:

- [What Is PII, non-PII, and Personal Data?](https://piwik.pro/blog/what-is-pii-personal-data/)
- [Logging documentation](https://docs.python.org/3/library/logging.html)
- [Bcrypt package](https://github.com/pyca/bcrypt/)
- [Logging to Files, Setting Levels, and Formatting](https://www.youtube.com/watch?v=-ARI4Cz-awo)
- [Uncovering Password Habits](https://www.digitalguardian.com/blog/uncovering-password-habits-are-users-password-security-habits-improving-infographic)

---

<h1> Tasks </h1>

1. **Regex-ing**

   - **Task:** Write a function called `filter_datum` in `filtered_logger.py` that returns the log message obfuscated.
   - **File:** [filtered_logger.py](./filtered_logger.py)

2. **Log formatter**

   - **Task:** Copy the given code into `filtered_logger.py`. Update the class to accept a list of strings `fields` as a constructor argument. Implement the `format` method to filter values in incoming log records using `filter_datum`.
     > For the user data refer to [user_data.csv](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/misc/2019/11/a2e00974ce6b41460425.csv?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20240213%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240213T230709Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=37deb17bb6c148bb3ecae2f8359d2711950fd06e33d7057f1fbe90bbf1de9b36)
   - **File:** [filtered_logger.py](./filtered_logger.py)

3. **Create logger**

   - **Task:** Implement a `get_logger` function in `filtered_logger.py` that returns a `logging.Logger` object. The logger should be named "user_data" and only log up to `logging.INFO` level. It should have a `StreamHandler` with `RedactingFormatter` as formatter.
   - **File:** [filtered_logger.py](./filtered_logger.py)

4. **Connect to secure database**

   - **Task:** Implement a `get_db` function in `filtered_logger.py` that returns a connector to the database (`mysql.connector.connection.MySQLConnection` object). Use environment variables to obtain database credentials.
   - **File:** [filtered_logger.py](./filtered_logger.py)

5. **Read and filter data**

   - **Task:** Implement a `main` function in `filtered_logger.py` that obtains a database connection using `get_db`. Retrieve all rows in the users table and display each row under a filtered format.
   - **File:** [filtered_logger.py](./filtered_logger.py)

6. **Encrypting passwords**

   - **Task:** Implement a `hash_password` function in `encrypt_password.py` that expects one string argument (`password`) and returns a salted, hashed password. Use the bcrypt package.
   - **File:** [encrypt_password.py](./encrypt_password.py)

7. **Check valid password**
   - **Task:** Implement an `is_valid` function in `encrypt_password.py` that expects two arguments (`hashed_password` of `bytes` type and `password` of `string` type) and returns a boolean. Use bcrypt to validate the provided password matches the hashed password.
   - **File:** [encrypt_password.py](./encrypt_password.py)

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
