# AndriodApp
🔐 Windows Forms Login System – Project Report

 📌 Project Title:

**Windows Forms Login Interface with User Authentication – Form2.cs**

 👨‍💻 Developer:

*Individual Project*

 🎯 Objective:

To implement a lightweight and functional login interface for a Windows Forms application that supports:

* User authentication
* Dynamic user registration
* Seamless transition to the main application (Form3)

 🧰 Technologies Used:

| Component            | Technology                                  |
| -------------------- | ------------------------------------------- |
| Programming Language | C# (.NET)                                   |
| Framework            | Windows Forms (.NET Framework or .NET Core) |
| IDE                  | Visual Studio 2022                          |
| Data Handling        | In-memory `Dictionary<string, string>`      |

 🛠️ Core Features:

✅ **Login Functionality**

* Users input their **username and password**.
* The system authenticates credentials using a local dictionary.
* If the credentials are valid, the user is navigated to `Form3`.
* Otherwise, an error message is shown (`"Invalid credentials"`).

✅ **User Registration**

* New users can register using the "Add User" button.
* Username/password pairs are stored in an in-memory dictionary.
* Prevents duplicate usernames.

 ✅ **UI Components Involved**

* `TextBox txtUsername`: Input for username.
* `TextBox txtPassword`: Input for password.
* `Button btnLogin`: Triggers authentication.
* `Button btnAddUser`: Registers new user.

 🔄 Workflow:

1. **Startup**:

   * `Form2` loads the login interface.

2. **Login**:

   * If user clicks **Login**, the app:

     * Validates credentials.
     * Proceeds to `Form3` if successful.
     * Shows error if not.

3. **Add User**:

   * If user clicks **Add User**:

     * Adds username and password to the dictionary if not already present.
     * Alerts if user already exists.

 ⚠️ Limitations & Considerations:

* 🔒 **Credentials are stored in-memory**:

  * Passwords are not encrypted.
  * Data is lost when the app closes.
  * Not suitable for production — use persistent secure storage (e.g., SQLite + encryption) for real apps.

* ⚙️ **No input validation**:

  * Does not check for empty usernames/passwords.
  * No password complexity or strength enforcement.

* 📦 **Tight coupling** to `Form3`:

  * `Form2` directly instantiates `Form3`, which might not scale well in larger apps.

 💡 Suggested Enhancements:

* 🔐 Use a secure persistent store (e.g., database + hashing).
* 🧾 Add logging or audit trails for logins.
* 🎨 Improve the UI with styling, error highlighting, and input placeholders.
* 🛡 Add brute-force prevention or captcha.
 ✅ Conclusion:

The **Windows Forms Login System** provides a basic yet functional user authentication interface suitable for learning or small-scale apps. It demonstrates event-driven programming in C#, form navigation, and simple credential handling. With minor security and UX enhancements, this project can serve as a solid foundation for more advanced applications.

