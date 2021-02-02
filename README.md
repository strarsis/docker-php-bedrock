# docker-php-bedrock
Docker image for PHP with roots.io Bedrock

## PHP Extensions

### PHP 7.x

| Extension                               | [Trellis](https://github.com/roots/trellis) | [Docker php-fpm](https://hub.docker.com/_/php) | docker-php-bedrock |
|-----------------------------------------|---------------------------------|----------------|-------------------|
| **WordPress recommended**               |                                 |                  |                 |
| curl                                    | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| dom                                     | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| exif                                    | ✅ (built in)                   | ❌              | ✅ (built in)   |
| fileinfo                                | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| hash                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| json                                    | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| mbstring                                | ✅ (php*-common; php*-mbstring) | ✅ (built in)   | ✅ (built in)   |
| mysqli                                  | ✅ (built in)                   | ❌              | ✅ (built in)   |
| sodium                                  | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| openssl                                 | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| pcre                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| imagick                                 | ❌                              | ❌              | ✅ (built in)   |
| xml                                     | ✅ (php*-common)                | ✅ (built in)   | ✅ (built in)   |
| zip                                     | ✅ (php*-common; php*-zip)      | ❌              | ✅ (built in)   |
| **WordPress fallback**                      |                              |                |                  |
| filter                                  | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| gd                                      | ✅ (php*-common; php*-gd)       | ❌              | ✅ (built in)   |
| iconv                                   | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| mcrypt                                  | ❌                              | ❌              | ✅ (built in)   |
| simplexml                               | ✅ (php*-common; php*-xml)      | ✅ (built in)   | ✅ (built in)   |
| xmlreader                               | ✅ (php*-common; php*-xml)      | ✅ (built in)   | ✅ (built in)   |
| zlib                                    | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| **WordPress update/write themes/plugins**   |                              |                |                   |
| ssh2                                    | ❌                              | ❌              | ❌              |
| ftp                                     | ✅ (built in)                   | ✅ (built in)   | ✅ (built in)   |
| sockets                                 | ✅ (built in)                   | ❌              | ❌              |
| **Trellis additional/differing extensions** |                              |                |                   |
| mysql                                   | ✅ (php*-common; php*-mysql)    | ❌              | ❌              |
| opcache                                 | ✅ (php*-common; php*-opcache)  | ❌              | ✅ (built in)   |
