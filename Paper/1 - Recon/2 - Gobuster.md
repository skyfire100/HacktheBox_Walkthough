Ran gobuster on http://10.129.105.222. This gives us page under /manual. This turns out to be the manual for Apache.

```bash
gobuster dir -u http://10.129.105.222 -w /usr/share/seclists/Discovery/Web-Content/raft-large-words.txt -t 40 -o recon/gobuster.out
```

```output
===============================================================  
Gobuster v3.1.0  
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)  
===============================================================  
[+] Url:                     http://10.129.105.222  
[+] Method:                  GET  
[+] Threads:                 40  
[+] Wordlist:                /usr/share/seclists/Discovery/Web-Content/raft-large-words.txt  
[+] Negative Status codes:   404  
[+] User Agent:              gobuster/3.1.0  
[+] Timeout:                 10s  
===============================================================  
2022/02/06 08:57:42 Starting gobuster in directory enumeration mode  
===============================================================  
/.html                (Status: 403) [Size: 199]  
/.htm                 (Status: 403) [Size: 199]  
/manual               (Status: 301) [Size: 237] [--> http://10.129.105.222/manual/]  
/.                    (Status: 403) [Size: 199691]                                    
/.htaccess            (Status: 403) [Size: 199]                                       
/.htc                 (Status: 403) [Size: 199]                                       
/.html_var_DE         (Status: 403) [Size: 199]                                       
/.htpasswd            (Status: 403) [Size: 199]                                       
/.html.               (Status: 403) [Size: 199]                                       
/.html.html           (Status: 403) [Size: 199]                                       
/.htpasswds           (Status: 403) [Size: 199]                                       
/.htm.                (Status: 403) [Size: 199]                                       
/.htmll               (Status: 403) [Size: 199]                                       
/.html.old            (Status: 403) [Size: 199]                                       
/.html.bak            (Status: 403) [Size: 199]                                       
/.ht                  (Status: 403) [Size: 199]                                       
/.htm.htm             (Status: 403) [Size: 199]                                       
/.hta                 (Status: 403) [Size: 199]                                       
/.htgroup             (Status: 403) [Size: 199]                                       
/.html1               (Status: 403) [Size: 199]                                       
/.html.printable      (Status: 403) [Size: 199]                                       
/.html.LCK            (Status: 403) [Size: 199]                                       
/.htm.LCK             (Status: 403) [Size: 199]                                       
/.html.php            (Status: 403) [Size: 199]                                       
/.htx                 (Status: 403) [Size: 199]                                       
/.htmls               (Status: 403) [Size: 199]                                       
/.htaccess.bak        (Status: 403) [Size: 199]                                       
/.htlm                (Status: 403) [Size: 199]                                       
/.htm2                (Status: 403) [Size: 199]                                       
/.html-               (Status: 403) [Size: 199]                                       
/.htuser              (Status: 403) [Size: 199]                                       
/.htm.d               (Status: 403) [Size: 199]                                       
/.htacess             (Status: 403) [Size: 199]                                       
/.htmlpar             (Status: 403) [Size: 199]                                       
/.html.orig           (Status: 403) [Size: 199]                                       
/.htm.html            (Status: 403) [Size: 199]                                       
/.html_files          (Status: 403) [Size: 199]                                       
/.html_               (Status: 403) [Size: 199]                                       
/.htmlprint           (Status: 403) [Size: 199]                                       
/.html.sav            (Status: 403) [Size: 199]                                       
/.hts                 (Status: 403) [Size: 199]                                       
/.html-1              (Status: 403) [Size: 199]                                       
/.htm.old             (Status: 403) [Size: 199]                                       
/.htaccess.old        (Status: 403) [Size: 199]                                       
/.htm.bak             (Status: 403) [Size: 199]                                       
/.htm.rc              (Status: 403) [Size: 199]                                       
/.htm3                (Status: 403) [Size: 199]                                       
/.html--              (Status: 403) [Size: 199]                                       
/.htm5                (Status: 403) [Size: 199]                                       
/.htm7                (Status: 403) [Size: 199]                                       
/.htm_                (Status: 403) [Size: 199]                                       
/.htm8                (Status: 403) [Size: 199]                                       
/.html-0              (Status: 403) [Size: 199]                                       
/.html-2              (Status: 403) [Size: 199]                                       
/.html-p              (Status: 403) [Size: 199]                                       
/.html-c              (Status: 403) [Size: 199]                                       
/.html-old            (Status: 403) [Size: 199]                                       
/.html.none           (Status: 403) [Size: 199]                                       
/.html5               (Status: 403) [Size: 199]                                       
/.html.start          (Status: 403) [Size: 199]                                       
/.html7               (Status: 403) [Size: 199]                                       
/.html.images         (Status: 403) [Size: 199]                                       
/.htmlq               (Status: 403) [Size: 199]                                       
/.html.htm            (Status: 403) [Size: 199]                                       
/.htmlfeed            (Status: 403) [Size: 199]                                       
/.html.pdf            (Status: 403) [Size: 199]                                       
/.htmlDolmetschen     (Status: 403) [Size: 199]                                       
/.htmlc               (Status: 403) [Size: 199]                                       
/.htmlBAK             (Status: 403) [Size: 199]                                       
/.html4               (Status: 403) [Size: 199]                                       
/.html.txt            (Status: 403) [Size: 199]                                       
/.html.inc            (Status: 403) [Size: 199]                                       
/.html_old            (Status: 403) [Size: 199]                                       
/.htmla               (Status: 403) [Size: 199]                                       
/.htmlu               (Status: 403) [Size: 199]                                       
/.htn                 (Status: 403) [Size: 199]                                       
                                                                                     
===============================================================  
2022/02/06 09:03:17 Finished  
===============================================================
```