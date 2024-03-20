# Sat Feb 10 17:57:13 EST 2024
#
# Files to edit to get the custom build working:
NG_BASE=/home/gmbroth/projects/udemy/Udemy_NGINX_Fundamentals_High-Performance_Servers_from_Scratch/custom-build/nginx-1.25.3
${NG_BASE}/auto/options

Caution: there are two nginx programs installed by the Udemy course:
- The package (apt-get) nginx is installed at /usr/sbin/nginx
- The configured nginx (custom-build/nginx-1.25.3/run_configure.sh) is installed at /usr/bin/nginx


Be careful as the default path will pick up /usr/sbin/nginx first. This isn't
a problem if the 'service' unit commands (start, stop, status) are used but
if typing something like 'nginx -t' you'll want to be careful to specify the
correct nginx. Both nginx versions share the same /etc/nginx configuration
files, however.

