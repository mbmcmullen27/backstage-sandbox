# Backstage

1. create
    ```
    npx @backstage/create-app@latest
    ```

1. add postgres backend package
    ```
    yarn add --cwd packages/backend pg
    ```

1. install postgres
    ```
    sudo apt-get install postgresql
    sudo -u postgres psql
    
    postgres=# ALTER USER postgres PASSWORD 'secret';
    ```



## Azure VM
1. get private key
    ```
    terraform output -raw tls_private_key > id_rsa
    ```

1. get ip address
    ```
    terraform output public_ip_address
    ```

1. connect
    ```
    ssh -i id_rsa azureuser@23.96.124.95
    ```