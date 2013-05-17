# Developer Public Keys

This pattern handles:

- creating a developer's home directory
- uploading a developer's public key to allow password-free access to the server
- removing access and deleting the developer's home directory when they leave the company

### To grant a developer access:

- list their username in the `$current_developers` variable in example-playbook.yml
- add their public key to the `keyfiles` folder (their username is the filename and the extension is .pub)

For example, to grant Jane Doe (using the username janedoe) access to the servers, the variables would contain:

```yml
vars:
    current_developers: [janedoe]
    retired_developers: []
```

and the keyfiles folder would contain:

    janedoe.pub

Running the playbook will create the developers' home directories (once) and upload the public keys.

### To revoke a developer's access:

- list their username in the `$retired_developers` variable
- remove their public key from the `keyfiles` folder

Running the playbook will **permanently delete** their home directory and revoke SSH access.
