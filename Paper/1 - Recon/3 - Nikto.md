Another tool we use for recon is nikto. 

```bash
nikto -h http://10.129.105.222
```

```output
- Nikto v2.1.6 
---------------------------------------------------------------------------  
+ Target IP:          10.129.105.222  
+ Target Hostname:    10.129.105.222  
+ Target Port:        80  
+ Start Time:         2022-02-06 09:06:14 (GMT-8)  
---------------------------------------------------------------------------  
+ Server: Apache/2.4.37 (centos) OpenSSL/1.1.1k mod_fcgid/2.3.9  
+ The anti-clickjacking X-Frame-Options header is not present.  
+ The X-XSS-Protection header is not defined. This header can hint to the user agent to protect against some forms of XSS  
+ Uncommon header 'x-backend-server' found, with contents: office.paper  
+ The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type  
+ Retrieved x-powered-by header: PHP/7.2.24  
+ Allowed HTTP Methods: POST, OPTIONS, HEAD, GET, TRACE    
+ OSVDB-877: HTTP TRACE method is active, suggesting the host is vulnerable to XST  
+ OSVDB-3092: /manual/: Web server manual found.  
+ OSVDB-3268: /icons/: Directory indexing found.  
+ OSVDB-3268: /manual/images/: Directory indexing found.  
+ OSVDB-3233: /icons/README: Apache default file found.  
+ 8724 requests: 0 error(s) and 11 item(s) reported on remote host  
+ End Time:           2022-02-06 09:20:24 (GMT-8) (850 seconds)  
---------------------------------------------------------------------------
```

We found a hostname in the 'x-backend-server' header.

```
office.paper
```
