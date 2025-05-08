# Customer Service

This lab tests the student's ability to discover hidden paths in web applications, analyze encrypted passwords, and detect unauthorized access, thereby understanding:

- Recognition of undocumented web paths (Broken Access Control)
- Analysis of MD5 passwords and use of dictionaries to crack them
- Simulation of login attempts on insecure forms
- Conditional flag retrieval based on specific credentials

## Machine Specifications 🖥️

- **System:** Ubuntu Server without GUI
- **Web Server:** Apache
- **Main site path:** `/var/www/html/index.html`
- **Vulnerable hidden path:** `/var/www/html/admin/admin.php`
- **Vulnerability type:** Broken Access Control (unprotected path)
- **Form:** Login with MD5 hash comparison in PHP

- **Available users (with MD5 hashed passwords):**

    | First Name | Last Name   | Email                     | Plaintext Password |
    |------------|-------------|---------------------------|--------------------|
    | Romeo      | Rodriguez   | romeo@fake.4geeks         | starwars           |
    | Alex       | Wilson      | alexwilson@fake.4geeks    | sunshine           |
    | Elisa      | Smith       | elismith94@fake.4geeks    | bubbles            |
    | John       | Logan       | jlogan@fake.4geeks        | g0dmode            |

- **Flag visible only when logged in as `john`:**

    ```text
    4GEEKS{Th1s_1s_p455w0rd_cr4ck!ng}
    ```

### Machine Credentials

```bash
servername: customer-service-lab
username: student
password: 4geeks-lab
```

## Expected Steps for the Student

1. **Perform network reconnaissance to identify the machine.**
   - Use tools like `nmap`, `netdiscover`, or `arp-scan`.
   - Detect an IP with port **80 (HTTP)** open.

2. **Access the website from the browser.**
   - Enter the detected IP in the browser to load the public landing page.

3. **Discover hidden paths using brute force.**
   - Use tools like `gobuster`, `ffuf`, or `dirb` to detect `/admin/`.

4. **Access the vulnerable file `admin.php`.**
   - Review the form code and the user table with MD5 hashed passwords.

5. **Crack the password hashes.**
   - Use `john`, `hashcat`, `crackstation`, or dictionaries like `rockyou.txt`.

6. **Simulate login attempts.**
   - Attempt to log in as each user until successful access is achieved.

7. **Identify the flag by logging in as `john`.**
   - Only this user will display the flag upon entering the correct password.
