# Need to create Password less authentication
We have private key available with the generated AWS instance, but we need public key to connect with private key.
in terminal you can use ``ssh-keygen`` command to generate Public Key. 

Here's a general guide on how to do it:

**Run command to generate public key to a AWS instance**

```
ssh-keygen
```

Generating public/private ed25519 key pair.

Default Path where public key generated ``/home/ubuntu/.ssh/id_ed25519``

## Here's a breakdown: 
**/usr/bin/ssh-copy-id:**
This is the command-line utility used to copy an SSH public key to a remote server's authorized_keys file.

**INFO: Source of key(s) to be installed::**
This message informs the user that the utility is about to copy a key, and it's specifying the source of the key.

**"/home/ubuntu/.ssh/id_ed25519.pub":**
This is the path to the public key file that will be copied. Specifically, it's the ED25519 public key for the user "ubuntu".

## Private key (in our case it was ``nvirginia1.pem``) set its permission to 700 (Read only)

```
sudo chmod 7000 nvirginia1.pem
```

**Run Command to copy public key to remote instance**

```
ssh-copy-id -f "-o IdentityFile ~/Ansible/nvirginia1.pem" ubuntu@52.90.101.13
```

## Now you can access remote instance without anykey pair

``ssh ubuntu@52.90.101.13``
