PRX Download
=============

This is a bash script that automates the download of shows you are subscribed to at PRX, using the SubAuto delivery method. 
This only works with shows that use the SubAuto method for delivery and allow series subscription

Setup
=====

The following environment variables should be set up:
* PD_FTP_SERVER - The PRX FTP location set up for your account, e.g. youraccount.prxtransfer.org
* PD_FTP_USER - Your PRX FTP user login
* PD_FTP_PASSWORD - Your PRX FTP password
* PD_LOCALDIR - The parent directory where you want files downloaded to
* PD_SHOW_DATA_FILE - The file that lists the shows you want to download, Default is show_data.txt
* PD_NOTIFY_EMAIL - Comma delimited list of email addresses where to send download results

Show Data
=========
The file specified in PD_SHOW_DATA_FILE is a text file with a line for each show formatted as follows:

Show name (for information only)|ftp_directory|local_subdirectory

ftp_directory is the directory on the PRX server for that show
local_subdirectory is the directory on your local machine where files should go for that show. It must exist

Mail Setup
==========
The script uses the "mail" command, assuming Postfix is installed. This is dependent on the type of machine this is running on and
what email servers you use.

These tutorials may be helpful:

* https://askubuntu.com/questions/457003/setting-up-a-send-only-mail-server
* https://www.howtoforge.com/postfix_relaying_through_another_mailserver
