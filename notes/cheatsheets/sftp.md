## To get a file from a machine via sftp

`sftp username@[machine_ip]:/directory/to/file /dir/you/want/it/on/local`

Add -r for directories

##To put a file to a machine through sftp

`sftp username@[machine_ip]`

Once you connect, navigate to the dir you want then:

`put /dir/file_on_your_local`
*
Again, use -r for a whole directory.
