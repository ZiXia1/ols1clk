# ols1clk

## Description
--------

ols1clk is a one-click installation script for OpenLiteSpeed. Using this script, you can quickly and easily install OpenLiteSpeed with it’s default settings. We also provide a **-W** parameter that will install WordPress at the same time but it must still be configured through the wp-config.php page. A MariaDB database can also be set up using this script if needed. If you already have a WordPress installation running on another server, it can be imported into OpenLiteSpeed with no hassle using the **--wordpresspath** parameter. To completely install WordPress with your OpenLiteSpeed installation, skipping the need for the wp-config.php page, use the **--wordpressplus** flag. This can be used with **--wpuser**, **--wppassword**, **--wplang**, and **--sitetitle** to configure each of the settings normally set by wp-config.php.

## Running ols1clk

ols1clk can be run in the following way:
*./ols1clk.sh [options] [options] …*

When run with no options, ols1clk will install OpenLiteSpeed with the default settings and values.

### Options:
|  Opt |    Options    | Description|
| :---: | ---------  | ---  |
| `-A` |`--adminpassword [PASSWORD]`|      To set the WebAdmin password for OpenLiteSpeed instead of using a random one.|
| `-E` |`--email [EMAIL]`|                 To set the administrator email.|
|      |`--lsphp [VERSION]`    |           To set the LSPHP version, such as 80. We currently support versions '56 70 71 72 73 74 80'.|
|      |`--mariadbver [VERSION]`  |        To set MariaDB version, such as 10.5. We currently support versions '10.2 10.3 10.4 10.5'.|
| `-W` |`--wordpress`|                     To install WordPress. You will still need to complete the WordPress setup by browser|
|      |  `--wordpressplus [SITEDOMAIN]`|  To install, setup, and configure WordPress, also LSCache will be enabled|
|      |  `--wordpresspath [WP_PATH]`|     To specify a location for the new WordPress installation or use for an existing WordPress.|
| `-R` | `--dbrootpassword [PASSWORD]` |   To set the database root password instead of using a random one.|
|      |  `--dbname [DATABASENAME]` |      To set the database name to be used by WordPress.|
|      |  `--dbuser [DBUSERNAME]`   |      To set the WordPress username in the database.|
|      |  `--dbpassword [PASSWORD]` |      To set the WordPress table password in MySQL instead of using a random one.|
|      |  `--listenport [PORT]`  |         To set the HTTP server listener port, default is 80.|
|      |  `--ssllistenport [PORT]` |       To set the HTTPS server listener port, default is 443.|
|      |  `--wpuser [WP_USER]`   |         To set the WordPress admin user for WordPress dashboard login. Default value is wpuser.|
|      |   `--wppassword [PASSWORD]`    |  To set the WordPress admin user password for WordPress dashboard login.|
|      |   `--wplang [WP_LANGUAGE]` |      To set the WordPress language. Default value is "en_US" for English.|
|      |   `--sitetitle [WP_TITLE]` |      To set the WordPress site title. Default value is mySite.|
| `-U` |   `--uninstall`  |                To uninstall OpenLiteSpeed and remove installation directory.|
| `-P` |   `--purgeall`   |                To uninstall OpenLiteSpeed, remove installation directory, and purge all data in MySQL.|
| `-Q` |   `--quiet`      |                To use quiet mode, won't prompt to input anything.|
| `-V` |   `--version`    |                To display the script version information.|
| `-v` |   `--verbose`    |                To display more messages during the installation.|
|      |   `--update`      |               To update ols1clk from github.|
| `-H` |    `--help`       |               To display help messages.|

### Examples
|    Examples    | Description|
|---|---|
|      `./ols1clk.sh`                       |To install OpenLiteSpeed with a random WebAdmin password.|
|      `./ols1clk.sh --lsphp 80 `           |To install OpenLiteSpeed with lsphp80.|
|      `./ols1clk.sh -A 123456 -e a@cc.com` |To install OpenLiteSpeed with WebAdmin password  "123456" and email a@cc.com.|
|      `./ols1clk.sh -R 123456 -W `         |To install OpenLiteSpeed with WordPress and MySQL root password "123456".|
|      `./ols1clk.sh --wordpressplus a.com` |To install OpenLiteSpeed with a fully configured WordPress installation at "a.com".|


## Support & Feedback
If you still have a question after using ols1clk, you have a few options.
* Join [the GoLiteSpeed Slack community](https://litespeedtech.com/slack) for real-time discussion
* Reporting any issue on [Github ols1clk](https://github.com/litespeedtech/ols1clk/issues) project
* Reporting any issue or want to talk about OpenLiteSpeed on [Google Group](https://groups.google.com/forum/#!forum/openlitespeed-development)