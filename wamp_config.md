### Config server

#### Exemple:

- File: C:\wamp64\bin\apache\apache2.4.46\conf\extra\httpd-vhosts.conf

```bash
# Virtual Hosts
#
<VirtualHost *:80>
  ServerName localhost
  ServerAlias localhost
  DocumentRoot "${INSTALL_DIR}/www"
  <Directory "${INSTALL_DIR}/www/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require local
  </Directory>
</VirtualHost>

<VirtualHost *:80>
	DocumentRoot "C:\wamp64\www\teste\public"
	ServerName teste-laravel
	DirectoryIndex index.php
	<Directory "C:\wamp64\www\teste\public">
		Options All
		AllowOverride All
		Order Allow,Deny
		Allow from all
	</Directory>
</VirtualHost>

#
<VirtualHost *:80>
	ServerName innoutproject
	DocumentRoot "C:\wamp64\www\innout\public"
	<Directory  "C:\wamp64\www\innout\public">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>
```