# Google Dorks for Bug Bounty

A list of Google Dorks for Bug Bounty, Web Application Security, and Pentesting

[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/TakSec.svg?style=social&label=Follow%20%40TakSec)](https://twitter.com/TakSec)
</p>

---

### Broad domain search w/ negative search

> site:example.com -www -shop -share -ir -mfa

### Find 

> site:example.com ext:php

### Sensitive data

> inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:"example.com

### apaaja

> site:"example.com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

### Database Files

> site:"example.com" ext:sql | ext:db | ext:dbf | ext:mdb | ext:sql.gz | ext:sql.gz | ext:db.gz | ext:db.gz

### Config files

> site:"example.com" ext:xml | ext:conf | ext:cnf | ext:reg | ext:inf | ext:rdp | ext:cfg | ext:txt | ext:ora | ext:env | ext:ini 

### High inurl keyword

> inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example.com

### Backup files

> site:"example.com" ext:bkf | ext:bkp | ext:bak | ext:old | ext:backup

### PHP extension w/ parameters

> site:example.com ext:php inurl:?

### git folder

> inurl:"/.git" "example.com" -site:github.com

### Exposed documents

> site:"example.com" ext:doc | ext:docx | ext:odt | ext:pdf | ext:rtf | ext:sxw | ext:psw | ext:ppt | ext:pptx | ext:pps | ext:csv

### SQL errors

> site:"example.com" AND (intext:"sql syntax near" | intext:"syntax error has occurred" | intext:"incorrect syntax near" | intext:"unexpected end of SQL command" | intext:"Warning: mysql_connect()" | intext:"Warning: mysql_query()" | intext:"Warning: pg_connect()")

### PHP errors

> site:"example.com" AND ("PHP Parse error" | "PHP Warning" | "PHP Error")

> site:"example.com" "Index of" inurl:phpmyadmin

### Login pages

> site:"example.com" AND (inurl:signup | inurl:login | inurl:register | intitle:Signup)

### Open redirects

> site:"example.com" AND (inurl:redir | inurl:url | inurl:redirect | inurl:return | inurl:location | inurl:next | inurl:dest | inurl:src=http | inurl:r=http)

### Apache struts RCE

> site:"example.com" AND (ext:action | ext:struts | ext:do)

### Wordpress files

> site:"example.com" AND (inurl:wp-content | inurl:wp-includes)

> site:"example.com" inurl:wp-config.php intext:DB_PASSWORD

> site:"example.com" intitle:"Index of" wp-admin

### Other files

> site:"example.com" AND (intitle:index.of | ext:log | ext:php intitle:phpinfo "published by the PHP Group" | inurl:shell | inurl:backdoor | inurl:wso | inurl:cmd | shadow | passwd | boot.ini | inurl:backdoor | inurl:readme | inurl:license | inurl:install | inurl:setup | inurl:config | inurl:"/phpinfo.php" | inurl:".htaccess" | ext:swf)

> site:"example.com" AND (ext:env | ext:log | ext:sql | ext:yml | ext:pem | ext:ini | ext:logs | ext:ibd | ext:txt | ext:php.txt | ext:old | ext:key | ext:frm | ext:bak | ext:zip | ext:swp | ext:conf | ext:db | ext:config | ext:ovpn | ext:svn | ext:git | ext:cfg | ext:exs | ext:dbf | ext:mdb | ext:pem | ext:pub | ext:yaml | ext:zip | ext:asc | ext:xls | ext:xlsx")

### Disclosed XSS and Open Redirects

> site:openbugbounty.org inurl:reports intext:"example.com"

> site:example.com inurl:search= | inurl:s= | inurl:message= | inurl:q=

### Juicy Extensions

> site:"example[.]com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

### XSS prone parameters

> inurl:q= | inurl:s= | inurl:search= | inurl:query= | inurl:keyword= | inurl:lang= inurl:& site:example.com

### Open Redirect prone parameters

> inurl:url= | inurl:return= | inurl:next= | inurl:redirect= | inurl:redir= | inurl:ret= | inurl:r2= | inurl:page= inurl:& inurl:http site:example.com

### SQLi Prone Parameters

> inurl:id= | inurl:pid= | inurl:category= | inurl:cat= | inurl:action= | inurl:sid= | inurl:dir= inurl:& site:example.com

### SSRF Prone Parameters

> inurl:http | inurl:url= | inurl:path= | inurl:dest= | inurl:html= | inurl:data= | inurl:domain=  | inurl:page= inurl:& site:example.com

### LFI Prone Parameters

> inurl:include | inurl:dir | inurl:detail= | inurl:file= | inurl:folder= | inurl:inc= | inurl:locate= | inurl:doc= | inurl:conf= inurl:& site:example.com

### RCE Prone Parameters

> inurl:cmd | inurl:exec= | inurl:query= | inurl:code= | inurl:do= | inurl:run= | inurl:read=  | inurl:ping= inurl:& site:example.com

### High % inurl keywords

> inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example[.]com

### Sensitive Parameters

> inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:example[.]com

### API Docs

> inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer site:"example[.]com"

### Disclosure vulnerabilites

> site:"example.com" filename:vim_settings.xml

> site:"example.com" filename:secrets.yml

> site:"example.com" filename:config.json

> site:"example.com" filename:config.ini

> site:"example.com" filename:config.properties

> site:"example.com" filename:config.xml

> site:"example.com" filename:config.yaml

> site:"example.com" filename:config.yml

> site:"example.com" filename:credentials.json

> site:"example.com" filename:credentials.xml

### Code Leaks

> site:pastebin.com "example.com"

> site:jsfiddle.net "example.com"

> site:codebeautify.org "example.com"

> site:codepen.io "example.com"

### Cloud Storage

> site:s3.amazonaws.com "example.com"

> site:blob.core.windows.net "example.com"

> site:googleapis.com "example.com"

> site:drive.google.com "example.com"

> site:dev.azure.com "example[.]com"

> site:onedrive.live.com "example[.]com"

> site:digitaloceanspaces.com "example[.]com"

> site:sharepoint.com "example[.]com"

> site:s3-external-1.amazonaws.com "example[.]com"

> site:s3.dualstack.us-east-1.amazonaws.com "example[.]com"

> site:dropbox.com/s "example[.]com"

> site:box.com/s "example[.]com"

> site:docs.google.com inurl:"/d/" "example[.]com"

### JFrog Artifactory

> site:jfrog.io "example[.]com"

### Firebase

> site:firebaseio.com "example[.]com"

### File upload endpoints

> site:example.com ”choose file”

## Dorks that work better w/o domain

### Bug Bounty programs and Vulnerability Disclosure Programs

> "submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"

> site:*/security.txt "bounty"

### Apache Server Status Exposed

> site:*/server-status apache

### WordPress

> inurl:/wp-admin/admin-ajax.php

### Drupal

> intext:"Powered by" & intext:Drupal & inurl:user

### Joomla

> site:*/joomla/login


---

Medium articles for more dorks:

https://thegrayarea.tech/5-google-dorks-every-hacker-needs-to-know-fed21022a906

https://infosecwriteups.com/uncover-hidden-gems-in-the-cloud-with-google-dorks-8621e56a329d

https://infosecwriteups.com/10-google-dorks-for-sensitive-data-9454b09edc12

Top Parameters:

https://github.com/lutfumertceylan/top25-parameter

Proviesec dorks:

https://github.com/Proviesec/google-dorks
