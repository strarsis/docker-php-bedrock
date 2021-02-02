# docker-php-bedrock
Docker image for PHP with roots.io Bedrock

## PHP Extensions

### PHP 7.x

| Extension                               | [Trellis](https://github.com/roots/trellis) | [Docker php-fpm](https://hub.docker.com/_/php) | docker-php-bedrock |
|-----------------------------------------|---------------------------------|----------------|-------------------|
| [**WordPress recommended**](https://make.wordpress.org/hosting/handbook/handbook/server-environment/#php-extensions) | | | |
| curl                                    | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| dom                                     | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| exif                                    | ✅ (built in)                   | ❌              | ✅ (docker-php-ext-install) |
| fileinfo                                | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| hash                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| json                                    | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| mbstring                                | ✅ (php*-common; php*-mbstring) | ✅ (built in)   | ✅ (built in)   |
| mysqli                                  | ✅ (built in)                   | ❌              | ✅ (docker-php-ext-install) |
| sodium                                  | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| openssl                                 | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| pcre                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| imagick                                 | ❌                              | ❌              | ✅ (pecl)       |
| imagick with GraphicsMagick (for PDF)   | ❌                              | ❌              | ✅ (pecl)       |
| xml                                     | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| zip                                     | ✅ (php*-common; php*-zip)      | ❌              | ✅ (pecl)       |
| [**WordPress fallback**](https://make.wordpress.org/hosting/handbook/handbook/server-environment/#php-extensions:~:text=modules%20WordPress%20may%20use) | | | |
| filter                                  | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| gd                                      | ✅ (php*-common; php*-gd)       | ❌              | ✅ (docker-php-ext-install) |
| iconv                                   | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| mcrypt                                  | ❌                              | ❌              | ✅ (pecl)       |
| simplexml                               | ✅ (php*-common; php*-xml)      | ✅ (built in)   | ✅ (built in)   |
| xmlreader                               | ✅ (php*-common; php*-xml)      | ✅ (built in)   | ✅ (built in)   |
| zlib                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| [**WordPress update/write themes/plugins**](https://make.wordpress.org/hosting/handbook/handbook/server-environment/#php-extensions:~:text=extensions%20are%20used%20for%20file%20changes) | | | |
| ssh2                                    | ❌                              | ❌              | ❌              |
| ftp                                     | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)*<sub>1</sub>   |
| sockets                                 | ✅ (built in)                   | ❌              | ❌              |
| [**Trellis additional/differing extensions**](https://github.com/roots/trellis/blob/68e313ffc1a2c34badfcc22cda6a5aaba11ec2f9/roles/php/defaults/main.yml#L4) | | | |
| mysql                                   | ✅ (php*-common; php*-mysql)    | ❌              | ❌              |
| opcache                                 | ✅ (php*-common; php*-opcache)  | ❌              | ✅ (docker-php-ext-install) |

*<sub>1</sub>: SSH/FTP/Sockets remote access for WordPress to write theme/plugin files isn't needed for container usage, but is already built into the PHP Dockerhub image.

