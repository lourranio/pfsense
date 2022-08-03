# pfsense


freeradius
```
freeradius3
>>> Installing pfSense-pkg-freeradius3... 
Updating pfSense-core repository catalogue...
pfSense-core repository is up to date.
Updating pfSense repository catalogue...
pfSense repository is up to date.
All repositories are up to date.
The following 12 package(s) will be affected (of 0 checked):

New packages to be INSTALLED:
	bash: 5.1.12 [pfSense]
	freeradius3: 3.0.25 [pfSense]
	gdbm: 1.22 [pfSense]
	groff: 1.22.4_4 [pfSense]
	libpaper: 1.1.28 [pfSense]
	mysql57-client: 5.7.36 [pfSense]
	pfSense-pkg-freeradius3: 0.15.7_33 [pfSense]
	postgresql13-client: 13.5 [pfSense]
	protobuf: 3.17.3,1 [pfSense]
	psutils: 1.17_5 [pfSense]
	talloc: 2.3.1 [pfSense]
	uchardet: 0.0.7 [pfSense]

Number of packages to be installed: 12

The process will require 121 MiB more space.
13 MiB to be downloaded.
[1/12] Fetching pfSense-pkg-freeradius3-0.15.7_33.pkg: ........ done
[2/12] Fetching bash-5.1.12.pkg: .......... done
[3/12] Fetching freeradius3-3.0.25.pkg: .......... done
[4/12] Fetching talloc-2.3.1.pkg: ...... done
[5/12] Fetching postgresql13-client-13.5.pkg: .......... done
[6/12] Fetching mysql57-client-5.7.36.pkg: .......... done
[7/12] Fetching groff-1.22.4_4.pkg: .......... done
[8/12] Fetching uchardet-0.0.7.pkg: .......... done
[9/12] Fetching psutils-1.17_5.pkg: ........ done
[10/12] Fetching libpaper-1.1.28.pkg: .... done
[11/12] Fetching protobuf-3.17.3,1.pkg: .......... done
[12/12] Fetching gdbm-1.22.pkg: .......... done
Checking integrity... done (0 conflicting)
[1/12] Installing libpaper-1.1.28...
[1/12] Extracting libpaper-1.1.28: .......... done
[2/12] Installing uchardet-0.0.7...
[2/12] Extracting uchardet-0.0.7: .......... done
[3/12] Installing psutils-1.17_5...
[3/12] Extracting psutils-1.17_5: .......... done
[4/12] Installing groff-1.22.4_4...
[4/12] Extracting groff-1.22.4_4: .......... done
[5/12] Installing protobuf-3.17.3,1...
[5/12] Extracting protobuf-3.17.3,1: .......... done
[6/12] Installing talloc-2.3.1...
[6/12] Extracting talloc-2.3.1: .......... done
[7/12] Installing postgresql13-client-13.5...
[7/12] Extracting postgresql13-client-13.5: .......... done
[8/12] Installing mysql57-client-5.7.36...
[8/12] Extracting mysql57-client-5.7.36: .......... done
[9/12] Installing gdbm-1.22...
[9/12] Extracting gdbm-1.22: .......... done
[10/12] Installing bash-5.1.12...
[10/12] Extracting bash-5.1.12: .......... done
[11/12] Installing freeradius3-3.0.25...
===> Creating groups.
Creating group 'freeradius' with gid '133'.
===> Creating users
Creating user 'freeradius' with uid '133'.
===> Setting user and group in radiusd.conf
[11/12] Extracting freeradius3-3.0.25: .......... done
===> Bootstrapping default certificates, please wait...
===> Adjusting ownership of directory /usr/local/etc/raddb
===> Adjusting ownership of directory /var/log/radacct
===> Adjusting ownership of directory /var/run/radiusd
===> Adjusting ownership of /var/log/radius.log
===> Adjusting ownership of /var/log/radutmp
===> Adjusting ownership of /var/log/radwtmp
===> Updating libdir in /usr/local/etc/raddb/radiusd.conf
[12/12] Installing pfSense-pkg-freeradius3-0.15.7_33...
[12/12] Extracting pfSense-pkg-freeradius3-0.15.7_33: .......... done
Saving updated package information...
done.
Loading package configuration... done.
Configuring package components...
Loading package instructions...
Custom commands...
Executing custom_php_install_command()...done.
Executing custom_php_resync_config_command()...done.
Menu items... done.
Services... done.
Writing configuration... done.
=====
Message from groff-1.22.4_4:

--
In order to be able to use the html driver, you need to install the following
packages:
 - ghostscript
 - netpbm
=====
Message from postgresql13-client-13.5:

--
The PostgreSQL port has a collection of "side orders":

postgresql-docs
  For all of the html documentation

p5-Pg
  A perl5 API for client access to PostgreSQL databases.

postgresql-tcltk 
  If you want tcl/tk client support.

postgresql-jdbc
  For Java JDBC support.

postgresql-odbc
  For client access from unix applications using ODBC as access
  method. Not needed to access unix PostgreSQL servers from Win32
  using ODBC. See below.

ruby-postgres, py-psycopg2
  For client access to PostgreSQL databases using the ruby & python
  languages.

postgresql-plperl, postgresql-pltcl & postgresql-plruby
  For using perl5, tcl & ruby as procedural languages.

postgresql-contrib
  Lots of contributed utilities, postgresql functions and
  datatypes. There you find pg_standby, pgcrypto and many other cool
  things.

etc...
=====
Message from mysql57-client-5.7.36:

--
This is the mysql CLIENT without the server.
for complete server and client, please install databases/mysql57-server
=====
Message from freeradius3-3.0.25:

--
To enable FreeRADIUS, put the following line in /etc/rc.conf

radiusd_enable="YES"


The sample configuration can be found at
/usr/local/share/examples/freeradius/raddb

If you are upgrading FreeRADIUS, you are advised to use this as a reference
for updating your configuration.


FreeRADIUS will look for its configuration directory at
/usr/local/etc/raddb by default.

If you did not already have a configuration at this location, the sample
configuration has been copied to this location and has been bootstrapped.


If you wish to point FreeRADIUS to a configuration at a different
location, put the following line in /etc/rc.conf

radiusd_flags="-d /path/to/raddb"


To start the server in normal (daemon) mode, run:

/usr/local/etc/rc.d/radiusd start

and to stop the server, run:

/usr/local/etc/rc.d/radiusd stop


To start the server in debugging mode, run:

/usr/local/etc/rc.d/radiusd debug


You are advised to make cautious changes to the configuration, and to test
frequently, using debugging mode where necessary. Try to resist the
temptation to disable or delete things that you don't understand - you may
well break things!

Useful configuration advice can be found in the FreeRADIUS Wiki at
http://wiki.freeradius.org
=====
Message from pfSense-pkg-freeradius3-0.15.7_33:

--
Please visit Services > FreeRADIUS menu to configure the package.

EAP certificate configuration is required before using the package.
Visit System > Cert. Manager and create a CA and a server certificate.
After that, visit Services > FreeRADIUS > EAP tab and complete
the 'Certificates for TLS' section (and, optionally, also the 'EAP-TLS' section.)
>>> Cleaning up cache... done.
Success

```
