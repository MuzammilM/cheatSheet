# cheatSheet

## crontab entry to write data to a file and read the file line by line and send notifications
    30 02 * * * /usr/bin/s3cmd ls -H s3://test/$(/bin/date -d '-1 day' +'\%Y-\%m-\%d')/ > ~/logs/shellLogs/dailyBackup.log && while IFS='' read -r Prop || [[ -n "$Prop" ]]; do  bash ~/bin/shellscript/slackBot.sh experiment $Prop;  done < logs/shellLogs/dailyBackup.log
