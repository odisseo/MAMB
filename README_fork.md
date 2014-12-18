README fork

#automysqlbacku

::line 307
cp -al "${1}${suffix}.enc" "${CONFIG_backup_dir}"/latest/
cp -al "${1}.enc" "${CONFIG_backup_dir}"/latest/

::line 2248

;;line 1990
deleted: exit ${status}

:line 167
'log')
  if [[ -s "$log_errfile" ]]; then
    cat "$log_file" && printf "\n###### WARNING ######\nErrors reported during AutoMySQLBackup execution.. Backup failed\nError log below..\n" && cat "$log_errfile" | mail -s "ERRORS REPORTED: MySQL Backup error Log for ${CONFIG_mysql_dump_host_friendly:-$CONFIG_mysql_dump_host} - ${datetimestamp}" ${CONFIG_mail_address}
  else
	      cat "$log_file" | mail -s "MySQL Backup Log for ${CONFIG_mysql_dump_host_friendly:-$CONFIG_mysql_dump_host} - ${datetimestamp}" ${CONFIG_mail_address}
	    fi
	    ;;
	    
:line 2251
opt_flags=( "${!opt_flag_@}" )	# array of all set variables starting with opt_flag_
opt_config_file_number=$#
if (( $# >= 1 )) && (( ${#opt_flags[@]} == 0 )); then
  for (( o=1 ; o <= $opt_config_file_number; o++ ))
  do
     opt_config_file="$1"; opt_flag_config_file=1; method_backup
     shift
  done
  exit ${status}
elif (( $# == 0 )) && (( ${#opt_flags[@]} == 0 )); then
  method_backup; exit ${status}
fi

#automysqlbackup.conf

CONFIG_db_exclude=( 'information_schema' )
CONFIG_table_exclude=( 'mysql.event' )