# rustd-hbbx
FreeBSD build for rustdesk-server, till the auto build/release works

Service user created via `pw adduser rustdesk -d /nonexistent -s /usr/sbin/nologin -c "Rustdesk Server user"`

Rcd script set to run the binaries in the directory of `/var/lib/rustdesk-server/`, which means your certificates and database files should be created/exist there.

Directory owned by service user via `chown -R rustdesk:rustdesk /var/lib/rustdesk-server/`  
Rights set with `chmod -R 660 /var/lib/rustdesk-server/` If you want to minimmize group rights `640` should be ok as well
