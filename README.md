# cheatSheet
  /usr/bin/s3cmd ls -H s3://test/$(/bin/date -d '-1 day' +'\%Y-\%m-\%d')/ > ~/logs/shellLogs/dailyBackup.log && while IFS='' read -r Prop || [[ -n "$Prop" ]]; do  bash ~/bin/shellscript/slackBot.sh sre $Prop;  done < logs/shellLogs/dailyBackup.log
