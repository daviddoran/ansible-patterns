# Developer public key files

Place your developers' public keys in this folder.

To generate a new public/private key pair:

    ssh-keygen -t rsa -C "developer name"

By default this will create two files:

    ~/.ssh/id_rsa
    ~/.ssh/id_rsa.pub

To enable ansible to copy the public keys to the server:

1. Copy the id_rsa.pub file (not id_rsa) to ./keyfiles/
2. Rename the file to the developer's username (e.g. daviddoran.pub)

The username is the username of the account on the server. If the developer
uses a different username on their dev computer then they'll need to manually
give the username on the command line or add an alias in ~/.ssh/config
