# What is Broken Access Control?

Access control enforces constraints on who can perform actions or access resources, relying on authentication (verifying identity) and session management (tracking user activity). It determines whether a user is authorized to carry out a requested action.

Broken access controls occur when these mechanisms fail, often due to human errors or design complexity, leading to critical security risks.

**Note:**  
Use tools like `feroxbuster` or similar domain and subdomain enumeration tools with wordlists like `Seclists` to discover subdomains that might not be accessible to normal users.

## Methodology:

1. **Admin Page and Cookie Manipulation**  
   - Use enumeration tools to locate the admin page.  
   - If the page is hidden, use `BurpSuite` to intercept network traffic and analyze cookies for manipulable parameters (e.g., `Admin=False`).  
   - **Example:** Change `Admin=False` to `Admin=True` in the cookie and test for access.

2. **User ID Manipulation**  
   - Identify user IDs from comments or other sources.  
   - Modify these in URL parameters to test for unauthorized access.  
   - Use two accounts for validation.  
   - **Example:** Change `user_id=123` to `user_id=456` to check if another user's data is accessible.

3. **Username Manipulation**  
   - Test if changing usernames in URL parameters allows access to other users’ data or assets.  
   - **Example:** Change `username=johndoe` to `username=janedoe` and check if Jane’s profile becomes accessible.

4. **Data Manipulation**  
   - Modify data such as file or image names to access restricted or personal files.  
   - **Example:** Change `/images/user123.jpg` to `/images/user456.jpg` to test access to another user's image.

5. **POST Request Analysis**  
   - Inspect login POST requests via `BurpSuite` for leaked parameters (e.g., `roleId`) that could be exploited for privilege escalation.  
   - **Example:** If the server response includes `roleId=2`, modify it to `roleId=1` to escalate privileges.

6. **TRACE Method for Server Behavior Analysis**  
   - Use the `TRACE` method to identify inappropriate behavior by inspecting changes in server requests.  
   - This helps detect misconfigurations or unauthorized access to restricted pages.
