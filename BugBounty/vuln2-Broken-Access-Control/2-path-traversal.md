# What is Path Traversal in Broken Access Control?

Path traversal, also known as directory traversal, is a vulnerability that allows attackers to access arbitrary files on the server running an application. These files might include:

- Application code and data.
- Credentials for back-end systems.
- Sensitive operating system files.

In some cases, attackers may also write to arbitrary files, enabling them to modify application behavior or gain full control of the server.

**Note:**  
Verify if assets like PDFs or photos within a web folder can be accessed by modifying their parameters in the URL. If accessible, this might indicate a vulnerability.

## Methodology:

1. **Filepath Vulnerability Check**  
   - Test common filepaths (e.g., `/etc/passwd`) in parameters related to photos or other assets.  
   - If accessible, this indicates a serious vulnerability.

2. **Relative Path Insertion**  
   - If absolute paths fail, try inserting relative paths such as `../../../../etc/passwd` to bypass the directory structure.

3. **Filter Evasion with Extra Characters**  
   - If relative paths are blocked, filtering might be in place. Bypass this by adding extra characters or slashes.  
   - **Example:** `....//....//....//etc/passwd`.

4. **Null Byte Injection for File Extension Restrictions**  
   - When parameters restrict file extensions (e.g., `.jpg` or `.pdf`), use a null byte injection.  
   - **Example:** `../../../../etc/passwd%00.jpg`.  
   - The null byte truncates the file path, bypassing the filter.

5. **URL Encoding for Advanced Filters**  
   - If advanced filters block other methods, use URL encoding to bypass them.  
   - **Examples:**  
     - Single Encoding: `..%2f..%2f..%2f..%2fetc/passwd`  
     - Double Encoding: `..%25%32%66..%25%32%66..%25%32%66..%25%32%66etc/passwd`

6. **Combination of Methods**  
   - If no single technique works, combine these methods to bypass protections.  
   - **Example:** Use URL encoding with null byte injection: `..%2f..%2f..%2f..%2fetc/passwd%00.jpg`.
