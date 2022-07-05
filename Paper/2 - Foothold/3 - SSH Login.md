lets try the creds we just got and try to ssh into the box.

```bash
ssh rocketchat@paper.htb
```

```output
rocketchat@paper.htb's password: Queenofblad3s!23
Permission denied, please try again.
```

but no luck with the password Queenofblad3s!23

trying daniel gives us a different outcome

```bash
ssh dwight@paper.htb
```

```output
dwight@paper.htb's password: Queenofblad3s!23
Activate the web console with: systemctl enable --now cockpit.socket  
  
Last login: Mon Feb  7 08:47:57 2022 from 10.10.14.169  
[dwight@paper ~]$
```

nice we have a shell!