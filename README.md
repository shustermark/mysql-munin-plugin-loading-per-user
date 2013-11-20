mysql-munin-plugin-loading-per-user
===================================

Plugin measure loading MySQL databases per user (CPU_Time).

1. You have to use that repository for mysql: http://repo.cloudlinux.com/other/cl5/

2. To enable statistics gathering, add the following setting to your my.cnf file 
in the [mysqld] section (or use it on the command-line when starting the server):
userstat = 1
Or you can simply change the value of the userstat system variable:
SET GLOBAL userstat=1;
Userstat provides the following new FLUSH and SHOW commands.
FLUSH USER_STATISTICS;
SHOW USER_STATISTICS;

3. Copy this plugin into munin plugins folder, usually /usr/share/munin/plugins/
4. Make sure that permissions is 775 so you can execute it.
5. Make symlink: ln -s /usr/share/munin/plugins/mysql_users /etc/munin/plugins/mysql_users
