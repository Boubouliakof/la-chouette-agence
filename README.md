# la-chouette-agence
# la-chouette-agence-modif
# BEGIN Cache-Control Headers
<IfModule mod_headers.c>
<FilesMatch "\.(ico|jpe?g|png|gif|swf|css|gz)$">
Header set Cache-Control "max-age=2592000, public"
</FilesMatch>
<FilesMatch "\.(js)$">
Header set Cache-Control "max-age=2592000, private"
</FilesMatch>
<filesMatch "\.(html|htm)$">
Header set Cache-Control "max-age=7200, public"
</filesMatch>
# Enleve le cache pour les ressources dynamiques
<FilesMatch "\.(pl|php|cgi|spl|scgi|fcgi)$">
Header unset Cache-Control
</FilesMatch>
</IfModule>
# END Cache-Control Headers

# BEGIN Expires Headers
<IfModule mod_expires.c>
ExpiresActive On
ExpiresByType image/jpg "access plus 1 year"
ExpiresByType image/jpeg "access plus 1 year"
ExpiresByType image/gif "access plus 1 year"
ExpiresByType image/png "access plus 1 year"
ExpiresByType text/css "access plus 1 month"
ExpiresByType application/pdf "access plus 1 month"
ExpiresByType text/x-javascript "access plus 1 month"
ExpiresByType application/x-shockwave-flash "access plus 1 month"
ExpiresByType image/x-icon "access plus 1 year"
ExpiresDefault "access plus 2 days"
</IfModule>
# END Expires Headers

RewriteEngine On
RewriteCond %{HTTP_HOST} ^boubouliakof.github.io/la-chouette-agence-modif/index.html [NC] 
RewriteRule ^(.*)$ https://www.boubouliakof.github.io/la-chouette-agence-modif/index.html/$1 [L,R=301]
