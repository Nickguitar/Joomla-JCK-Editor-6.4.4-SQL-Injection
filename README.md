# Joomla-JCK-Editor-6.4.4-SQL-Injection

The JCK Editor Jtreelink plugin for Joomla! fails to correctly parse the user inputs, allowing SQL Injection.
This exploit takes advantage of this security flaw and dump the administrators credentials and possibly upload a PHP RCE shell.

Exploit Title: Joomla JCK Editor 6.4.4 SQL Injection

Googke Dork: inurl:/plugins/editors/jckeditor/plugins/jtreelink/

Date: 05/03/2021

Exploit Author: Nicholas Ferreira

Vendor Homepage: http://docs.arkextensions.com/downloads/jck-editor

Version: 6.4.4

Tested on: Debian 10

CVE : CVE-2018-17254


# Usage
user@lol~: php JCKEditor_SQLi_Exploit.php --url target.com/plugins/

You must specify the /plugins/ directory. This is because some websites are not hosted on the root of the webserver, e.g, the applications may be as target.com/site/, or target.com/2021/, or something like that.

With -r or --rce, the exploit will try to craft and upload a PHP script that allows remote command execution. This will only work if the MySQL allows stacked queries, which is not the default configuration, so it will probably not work. =(
