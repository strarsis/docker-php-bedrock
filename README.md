# docker-php-bedrock
Docker image for PHP with roots.io Bedrock

## PHP Extensions

| Extension                               | Trellis                       | Docker php-fpm |
|-----------------------------------------|-------------------------------|----------------|
| WordPress recommended                   |                               |                |
| curl                                    | ✅ (php-common)                | ✅ (built in)   |
| dom                                     | ✅ (built in)                  | ✅ (built in)   |
| exif                                    | ✅ (built in)                  | ❌              |
| fileinfo                                | ✅ (built in)                  | ✅ (built in)   |
| hash                                    | ✅ (built in)                  | ✅ (built in)   |
| json                                    | ✅ (php-common)                | ✅ (built in)   |
| mbstring                                | ✅ (php-common; php*-mbstring) | ✅ (built in)   |
| mysqli                                  | ✅ (built in)                  | ❌              |
| sodium                                  | ✅ (built in)                  | ✅ (built in)   |
| openssl                                 | ✅ (built in)                  | ✅ (built in)   |
| pcre                                    | ✅ (built in)                  | ✅ (built in)   |
| imagick                                 | ❌                             | ❌              |
| xml                                     | ✅ (php-common)                | ✅ (built in)   |
| zip                                     | ✅ (php-common; php*-zip)      | ❌              |
| WordPress fallback                      |                               |                |
| filter                                  | ✅ (built in)                  | ✅ (built in)   |
| gd                                      | ✅ (php-common; php*-gd)       | ❌              |
| iconv                                   | ✅ (built in)                  | ✅ (built in)   |
| mcrypt                                  | ❌                             | ❌              |
| simplexml                               | ✅ (php-common; php*-xml)      | ✅ (built in)   |
| xmlreader                               | ✅ (php-common; php*-xml)      | ✅ (built in)   |
| zlib                                    | ✅ (built in)                  | ✅ (built in)   |
| WordPress update/write themes/plugins   |                               |                |
| ssh2                                    | ❌                             | ❌              |
| ftp                                     | ✅ (built in)                  | ✅ (built in)   |
| sockets                                 | ✅ (built in)                  | ❌              |
| Trellis additional/differing extensions |                               |                |
| mysql                                   | ✅ (php-common; php*-mysql)    | ❌              |
| opcache                                 | ✅ (php-common; php*-opcache)  | ❌              |
| dev                                     | ✅ (php*-dev)                   | ❌              |
