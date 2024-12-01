
# What is Information Disclosure?

Information disclosure occurs when a website unintentionally exposes sensitive data, such as user details, business information, or technical details. Attackers can exploit this by interacting with the site in unexpected ways to gather useful information, potentially leading to further attacks. Even seemingly minor leaks can help attackers discover other vulnerabilities.

## Methodology:

1. **Access /robots.txt for Subdomain Discovery**  
   Check if `/robots.txt` is accessible to uncover any subdomains or directories excluded from search engine indexing that might contain sensitive information.

2. **Parameter Testing for Error Messages**  
   Pass various alphanumeric characters to website parameters and analyze the responses for error messages or information leakage that could indicate security vulnerabilities.

3. **Subdomain Enumeration with Tools**  
   Use tools like `FeroxBuster` and wordlists (e.g., `Seclists`) to perform a comprehensive subdomain enumeration for deeper discovery of hidden assets.

4. **Check for Exposed .git Files**  
   Look for exposed `.git` files on the server to identify sensitive repository information.
