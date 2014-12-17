README fork

#automysqlbacku

::line 307
cp -al "${1}${suffix}.enc" "${CONFIG_backup_dir}"/latest/
cp -al "${1}.enc" "${CONFIG_backup_dir}"/latest/

::line 2248

#automysqlbackup.conf

CONFIG_db_exclude=( 'information_schema' )
CONFIG_table_exclude=( 'mysql.event' )