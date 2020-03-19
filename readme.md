<h>Comandos Workshop</h>


1 - sudo yum install s3fs-fuse
2 - mkdir <your DIR>
3 - cd ${home}
4 - vi .passwd-s3fs
5 - s3fs bucket-20191126-1402 /mnt/OracleBucket -o passwd_file=${HOME}/.passwd-s3fs -o url=https://id48tvbseabm.compat.objectstorage.us-ashburn-1.oraclecloud.com  -onomultipart -o use_path_request_style -o allow_other -o uid='994' -o umask=0007
