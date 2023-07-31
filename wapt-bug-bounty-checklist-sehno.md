# Bug Bounty Checklist for Web App

> Written by @sehno on
> [github.](https://github.com/sehno/Bug-bounty/blob/master/bugbounty_checklist.md)

## Table of Contents

* [Recon on wildcard domain](#"Recon_on_wildcard_domain")
* [Single domain](#Single_domain)
* [Information Gathering](#Information)
* [Configuration Management](#Configuration)
* [Secure Transmission](#Transmission)
* [Authentication](#Authentication)
* [Session Management](#Session)
* [Authorization](#Authorization)
* [Data Validation](#Validation)
* [Denial of Service](#Denial)
* [Business Logic](#Business)
* [Cryptography](#Cryptography)
* [Risky Functionality - File Uploads](#File)
* [Risky Functionality - Card Payment](#Card)
* [HTML 5](#HTML)

## <a name="Recon_on_wildcard_domain">Recon on wildcard domain</a>

- [ ] Run amass<br/>
- [ ] Run subfinder<br/>
- [ ] Run assetfinder<br/>
- [ ] Run dnsgen<br/>
- [ ] Run massdns<br/>
- [ ] Use httprobe<br/>
- [ ] Run aquatone (screenshot for alive host)<br/>

## <a name="Single_domain">Single Domain</a><br/>

### Scanning<br/>

- [ ] Nmap scan<br/>
- [ ] Burp crawler<br/>
- [ ] ffuf (directory and file fuzzing)
- [ ] hakrawler/gau/paramspider<br/>
- [ ] Linkfinder<br/>
- [ ] Url with Android application<br/>

### Manual checking<br/>

- [ ] Shodan<br/>
- [ ] Censys<br/>
- [ ] Google dorks<br/>
- [ ] Pastebin<br/>
- [ ] Github<br/>
- [ ] OSINT<br/><br/>

### <a name="Information">Information Gathering</a>
- [ ] Manually explore the site<br/>
- [ ] Spider/crawl for missed or hidden content<br/>
- [ ] Check for files that expose content, such as robots.txt, sitemap.xml, .DS_Store<br/>
- [ ] Check the caches of major search engines for publicly accessible sites<br/>
- [ ] Check for differences in content based on User Agent (eg, Mobile sites, access as a Search engine Crawler)<br/>
- [ ] Perform Web Application Fingerprinting<br/>
- [ ] Identify technologies used<br/>
- [ ] Identify user roles<br/>
- [ ] Identify application entry points<br/>
- [ ] Identify client-side code<br/>
- [ ] Identify multiple versions/channels (e.g. web, mobile web, mobile app, web services)<br/>
- [ ] Identify co-hosted and related applications<br/>
- [ ] Identify all hostnames and ports<br/>
- [ ] Identify third-party hosted content<br/>
- [ ] Identify Debug parameters<br/>

### <a name="Configuration">Configuration Management</a>

- [ ] Check for commonly used application and administrative URLs<br/>
- [ ] Check for old, backup and unreferenced files<br/>
- [ ] Check HTTP methods supported and Cross Site Tracing (XST)<br/>
- [ ] Test file extensions handling<br/>
- [ ] Test for security HTTP headers (e.g. CSP, X-Frame-Options, HSTS)<br/>
- [ ] Test for policies (e.g. Flash, Silverlight, robots)<br/>
- [ ] Test for non-production data in live environment, and vice-versa<br/>
- [ ] Check for sensitive data in client-side code (e.g. API keys, credentials)<br/>

### <a name="Transmission">Secure Transmission</a>

- [ ] Check SSL Version, Algorithms, Key length<br/>
- [ ] Check for Digital Certificate Validity (Duration, Signature and CN)<br/>
- [ ] Check credentials only delivered over HTTPS<br/>
- [ ] Check that the login form is delivered over HTTPS<br/>
- [ ] Check session tokens only delivered over HTTPS<br/>
- [ ] Check if HTTP Strict Transport Security (HSTS) in use<br/>

### <a name="Authentication">Authentication</a>
- [ ] Test for user enumeration<br/>
- [ ] Test for authentication bypass<br/>
- [ ] Test for bruteforce protection<br/>
- [ ] Test password quality rules<br/>
- [ ] Test remember me functionality<br/>
- [ ] Test for autocomplete on password forms/input<br/>
- [ ] Test password reset and/or recovery<br/>
- [ ] Test password change process<br/>
- [ ] Test CAPTCHA<br/>
- [ ] Test multi factor authentication<br/>
- [ ] Test for logout functionality presence<br/>
- [ ] Test for cache management on HTTP (eg Pragma, Expires, Max-age)<br/>
- [ ] Test for default logins<br/>
- [ ] Test for user-accessible authentication history<br/>
- [ ] Test for out-of channel notification of account lockouts and successful password changes<br/>
- [ ] Test for consistent authentication across applications with shared authentication schema / SSO<br/>

### <a name="Session">Session Management</a>
- [ ] Establish how session management is handled in the application (eg, tokens in cookies, token in URL)<br/>
- [ ] Check session tokens for cookie flags (httpOnly and secure)<br/>
- [ ] Check session cookie scope (path and domain)<br/>
- [ ] Check session cookie duration (expires and max-age)<br/>
- [ ] Check session termination after a maximum lifetime<br/>
- [ ] Check session termination after relative timeout<br/>
- [ ] Check session termination after logout<br/>
- [ ] Test to see if users can have multiple simultaneous sessions<br/>
- [ ] Test session cookies for randomness<br/>
- [ ] Confirm that new session tokens are issued on login, role change and logout<br/>
- [ ] Test for consistent session management across applications with shared session management<br/>
- [ ] Test for session puzzling<br/>
- [ ] Test for CSRF and clickjacking<br/>

### <a name="Authorization">Authorization</a>
- [ ] Test for path traversal<br/>
- [ ] Test for bypassing authorization schema<br/>
- [ ] Test for vertical Access control problems (a.k.a. Privilege Escalation)<br/>
- [ ] Test for horizontal Access control problems (between two users at the same privilege level)<br/>
- [ ] Test for missing authorization<br/>

### <a name="Validation">Data Validation</a>
- [ ] Test for Reflected Cross Site Scripting<br/>
- [ ] Test for Stored Cross Site Scripting<br/>
- [ ] Test for DOM based Cross Site Scripting<br/>
- [ ] Test for Cross Site Flashing<br/>
- [ ] Test for HTML Injection<br/>
- [ ] Test for SQL Injection<br/>
- [ ] Test for LDAP Injection<br/>
- [ ] Test for ORM Injection<br/>
- [ ] Test for XML Injection<br/>
- [ ] Test for XXE Injection<br/>
- [ ] Test for SSI Injection<br/>
- [ ] Test for XPath Injection<br/>
- [ ] Test for XQuery Injection<br/>
- [ ] Test for IMAP/SMTP Injection<br/>
- [ ] Test for Code Injection<br/>
- [ ] Test for Expression Language Injection<br/>
- [ ] Test for Command Injection<br/>
- [ ] Test for Overflow (Stack, Heap and Integer)<br/>
- [ ] Test for Format String<br/>
- [ ] Test for incubated vulnerabilities<br/>
- [ ] Test for HTTP Splitting/Smuggling<br/>
- [ ] Test for HTTP Verb Tampering<br/>
- [ ] Test for Open Redirection<br/>
- [ ] Test for Local File Inclusion<br/>
- [ ] Test for Remote File Inclusion<br/>
- [ ] Compare client-side and server-side validation rules<br/>
- [ ] Test for NoSQL injection<br/>
- [ ] Test for HTTP parameter pollution<br/>
- [ ] Test for auto-binding<br/>
- [ ] Test for Mass Assignment<br/>
- [ ] Test for NULL/Invalid Session Cookie<br/>

### <a name="Denial">Denial of Service</a>
- [ ] Test for anti-automation<br/>
- [ ] Test for account lockout<br/>
- [ ] Test for HTTP protocol DoS<br/>
- [ ] Test for SQL wildcard DoS<br/>

### <a name="Business">Business Logic</a>
- [ ] Test for feature misuse<br/>
- [ ] Test for lack of non-repudiation<br/>
- [ ] Test for trust relationships<br/>
- [ ] Test for integrity of data<br/>
- [ ] Test segregation of duties<br/>

### <a name="Cryptography">Cryptography</a>
- [ ] Check if data which should be encrypted is not<br/>
- [ ] Check for wrong algorithms usage depending on context<br/>
- [ ] Check for weak algorithms usage<br/>
- [ ] Check for proper use of salting<br/>
- [ ] Check for randomness functions<br/>

### <a name="File">Risky Functionality - File Uploads</a>
- [ ] Test that acceptable file types are whitelisted<br/>
- [ ] Test that file size limits, upload frequency and total file counts are defined and are enforced<br/>
- [ ] Test that file contents match the defined file type<br/>
- [ ] Test that all file uploads have Anti-Virus scanning in-place.<br/>
- [ ] Test that unsafe filenames are sanitised<br/>
- [ ] Test that uploaded files are not directly accessible within the web root<br/>
- [ ] Test that uploaded files are not served on the same hostname/port<br/>
- [ ] Test that files and other media are integrated with the authentication and authorisation schemas<br/>

### <a name="Card">Risky Functionality - Card Payment</a>
- [ ] Test for known vulnerabilities and configuration issues on Web Server and Web Application<br/>
- [ ] Test for default or guessable password<br/>
- [ ] Test for non-production data in live environment, and vice-versa<br/>
- [ ] Test for Injection vulnerabilities<br/>
- [ ] Test for Buffer Overflows<br/>
- [ ] Test for Insecure Cryptographic Storage<br/>
- [ ] Test for Insufficient Transport Layer Protection<br/>
- [ ] Test for Improper Error Handling<br/>
- [ ] Test for all vulnerabilities with a CVSS v2 score > 4.0<br/>
- [ ] Test for Authentication and Authorization issues<br/>
- [ ] Test for CSRF<br/>

### <a name="HTML">HTML 5</a>
- [ ] Test Web Messaging<br/>
- [ ] Test for Web Storage SQL injection<br/>
- [ ] Check CORS implementation<br/>
- [ ] Check Offline Web Application<br/>

Source:<br/>
[OWASP](https://www.owasp.org/index.php/Web_Application_Security_Testing_Cheat_Sheet)

