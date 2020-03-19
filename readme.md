<h>Workshop H2O on Oracle Cloud</h>

  Está workshop tem como objetivo apresentar a instalação e configuração da aplicação H2O. Abaixo seguem os comandos para configuração da VM, sendo a instalação da library Fuse junto com os comandos para fazer o "mount", e também a a configuração da API S3.

# Configuração Fuse
  1 - sudo yum install s3fs-fuse
  2 - mkdir <your DIR>
  3 - cd ${home}
  4 - vi .passwd-s3fs
  5 - s3fs <bucket name> <mount path> -o passwd_file=${HOME}/.passwd-s3fs -o url=https://<namespace>.compat.objectstorage.<Region>.oraclecloud.com  -onomultipart -o use_path_request_style -o allow_other -o uid='994' -o umask=0007

# Configuração S3 API
  # S3 auth
  aws_auth = "True"

  # S3 Connector credentials
  aws_access_key_id = "9bcfb61f004a95a4e6db0503a33fd49efdaf748a"

  # S3 Connector credentials
  aws_secret_access_key = "IKq1saSrCdAF/44Qtf0JtqpAA0BLCbdBfVAB2vvTacw="
  
  # Sets enpoint URL that will be used to access S3.
  aws_s3_endpoint_url = "https://id48tvbseabm.compat.objectstorage.us-ashburn-1.oraclecloud.com"
