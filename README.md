# rustd-hbbx
FreeBSD build for rustdesk-server, till the auto build/release works

The tar.gz file contains the rustdesk-servers `hbbs` & `hbbr` binaries, the `rustdesk-utils`, plus the rcd scripts expecting the below details (home dir & service user). The tar.gz file has the full path from root, extract it with `-C /` option to do extract from root dir. 

Necessary commands:
Service user - `pw adduser rustdesk -d /nonexistent -s /usr/sbin/nologin -c "Rustdesk Server user"`

Running directory - `mkdir /var/lib/rustdesk-server` (Your certificates and database files should be created/exist there)

Ownership - `chown -R rustdesk:rustdesk /var/lib/rustdesk-server/`  

Rights - `chmod -R 660 /var/lib/rustdesk-server/` If you want to minimmize group rights `640` should be ok as well
