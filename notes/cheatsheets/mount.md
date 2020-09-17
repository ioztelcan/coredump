# mount

## Mounting directories from a server to another machine can be done with following steps:

* On the server, add an entry into /etc/exports to share the directory with options

`[directory_path] *(rw,insecure,no_root_squash)`

* Then run following command to share the directory \(may require root privileges\).

`exportfs -r`

* Exporting can be verified with

`exportfs`

Now the directory can be mounted on the second server

`mount [server_ip:directory] [mount_point]`

It can be verified with:

`mount -t nfs`

!!!Important: If mounting fails with an error similar to:

`svc: failed to register lockdv1 RPC service (errno 5)`

following command might help \(possibly the only option needed is nolock\):

`mount -o nolock,proto=tcp -t nfs [ip_addr:directory_to_be_mounted] [local_mount_point]`

_nolock:_ Disables file locking. It is occasionally required when connecting to older NFS servers.

Another issue might be missing nfs-common libraries. It can be installed with apt.

## To mount / partition as read-write in repair mode:

mount -o remount,rw /

## Bind mount path to a second location

mount --bind /origin/path /destination/path

## To mount Usb disk as user writable:

mount -o uid=username,gid=usergroup /dev/sdx /mnt/xxx

## To mount a remote NFS directory

mount -t nfs example.com:/remote/example/dir /local/example/dir

## To mount an ISO

mount -o loop disk1.iso /mnt/disk

