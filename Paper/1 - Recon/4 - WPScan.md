heading to http://office.paper/ and viewing the source shows us some directories that are associated with wordpress. (wp-contnet... etc)

lets see what wp scan will give us


```bash
wpscan --url http://office.paper/ --enumerate
```


```output
_______________________________________________________________  
        __          _______   _____  
        \ \        / /  __ \ / ____|  
         \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®  
          \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \  
           \  /\  /  | |     ____) | (__| (_| | | | |  
            \/  \/   |_|    |_____/ \___|\__,_|_| |_|  
  
        WordPress Security Scanner by the WPScan Team  
                        Version 3.8.17  
      Sponsored by Automattic - https://automattic.com/  
      @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart  
_______________________________________________________________  
  
[+] URL: http://office.paper/ [10.129.105.222]  
[+] Started: Sun Feb  6 09:28:38 2022  
  
Interesting Finding(s):  
  
[+] Headers  
| Interesting Entries:  
|  - Server: Apache/2.4.37 (centos) OpenSSL/1.1.1k mod_fcgid/2.3.9  
|  - X-Powered-By: PHP/7.2.24  
|  - X-Backend-Server: office.paper  
| Found By: Headers (Passive Detection)  
| Confidence: 100%  
  
[+] WordPress readme found: http://office.paper/readme.html  
| Found By: Direct Access (Aggressive Detection)  
| Confidence: 100%  
  
[+] WordPress version 5.2.3 identified (Insecure, released on 2019-09-05).  
| Found By: Rss Generator (Passive Detection)  
|  - http://office.paper/index.php/feed/, <generator>https://wordpress.org/?v=5.2.3</generator>  
|  - http://office.paper/index.php/comments/feed/, <generator>https://wordpress.org/?v=5.2.3</generator>  
  
[+] WordPress theme in use: construction-techup  
| Location: http://office.paper/wp-content/themes/construction-techup/  
| Last Updated: 2021-07-17T00:00:00.000Z  
| Readme: http://office.paper/wp-content/themes/construction-techup/readme.txt  
| [!] The version is out of date, the latest version is 1.4  
| Style URL: http://office.paper/wp-content/themes/construction-techup/style.css?ver=1.1  
| Style Name: Construction Techup  
| Description: Construction Techup is child theme of Techup a Free WordPress Theme useful for Business, corporate a...  
| Author: wptexture  
| Author URI: https://testerwp.com/  
|  
| Found By: Css Style In Homepage (Passive Detection)  
|  
| Version: 1.1 (80% confidence)  
| Found By: Style (Passive Detection)  
|  - http://office.paper/wp-content/themes/construction-techup/style.css?ver=1.1, Match: 'Version: 1.1'  
  
[+] Enumerating Vulnerable Plugins (via Passive Methods)  
  
[i] No plugins Found.  
  
[+] Enumerating Vulnerable Themes (via Passive and Aggressive Methods)  
Checking Known Locations - Time: 00:00:08 <===========================================================================================================================================================> (400 / 400) 100.00% Time: 00:00:08  
[+] Checking Theme Versions (via Passive and Aggressive Methods)  
  
[i] No themes Found.  
  
[+] Enumerating Timthumbs (via Passive and Aggressive Methods)  
Checking Known Locations - Time: 00:00:48 <=========================================================================================================================================================> (2575 / 2575) 100.00% Time: 00:00:48  
  
[i] No Timthumbs Found.  
  
[+] Enumerating Config Backups (via Passive and Aggressive Methods)  
Checking Config Backups - Time: 00:00:02 <============================================================================================================================================================> (137 / 137) 100.00% Time: 00:00:02  
  
[i] No Config Backups Found.  
  
[+] Enumerating DB Exports (via Passive and Aggressive Methods)  
Checking DB Exports - Time: 00:00:01 <==================================================================================================================================================================> (71 / 71) 100.00% Time: 00:00:01  
  
[i] No DB Exports Found.  
  
[+] Enumerating Medias (via Passive and Aggressive Methods) (Permalink setting must be set to "Plain" for those to be detected)  
Brute Forcing Attachment IDs - Time: 00:00:15 <=======================================================================================================================================================> (100 / 100) 100.00% Time: 00:00:15  
  
[i] No Medias Found.  
  
[+] Enumerating Users (via Passive and Aggressive Methods)  
Brute Forcing Author IDs - Time: 00:00:03 <=============================================================================================================================================================> (10 / 10) 100.00% Time: 00:00:03  
  
[i] User(s) Identified:  
  
[+] prisonmike  
| Found By: Author Posts - Author Pattern (Passive Detection)  
| Confirmed By:  
|  Rss Generator (Passive Detection)  
|  Wp Json Api (Aggressive Detection)  
|   - http://office.paper/index.php/wp-json/wp/v2/users/?per_page=100&page=1  
|  Author Id Brute Forcing - Author Pattern (Aggressive Detection)  
|  Login Error Messages (Aggressive Detection)  
  
[+] nick  
| Found By: Wp Json Api (Aggressive Detection)  
|  - http://office.paper/index.php/wp-json/wp/v2/users/?per_page=100&page=1  
| Confirmed By:  
|  Author Id Brute Forcing - Author Pattern (Aggressive Detection)  
|  Login Error Messages (Aggressive Detection)  
  
[+] creedthoughts  
| Found By: Author Id Brute Forcing - Author Pattern (Aggressive Detection)  
| Confirmed By: Login Error Messages (Aggressive Detection)  
  
[!] No WPScan API Token given, as a result vulnerability data has not been output.  
[!] You can get a free API token with 25 daily requests by registering at https://wpscan.com/register  
  
[+] Finished: Sun Feb  6 09:30:09 2022  
[+] Requests Done: 3341  
[+] Cached Requests: 10  
[+] Data Sent: 915.619 KB  
[+] Data Received: 923.961 KB  
[+] Memory used: 231.145 MB  
[+] Elapsed time: 00:01:30

```

we found a couple users

```
prisonmike
nick
creedthoughts
```