# Digression: SSH

## What are SSH keys?

An SSH key pair is an access credential for the SSH (secure shell) network protocol. It is used for secure remote communication between machines (like file transfer, network management, and remote operating system access) on an unsecured open network.

A key pair consists of a public and a private key.

The private key is kept secret on the clients machine. It is encrypted with a passphrase. The passphrase is defined when the key is generated (but can be changed later). If the private key is leaked, the passphrase is an additional protection to prevent identity theft.

The public key is the counterpart to the private key. To allow access to a remote machine, the public key needs to registered there.

When the private key gets leaked, you should immediately revoke your private/public key pair. To do so, remove the public key from all remote machines it was registered at (e.g. Bitbucket, Github, ...), then delete the key pair from your machine and generate a new one.

### Types of SSH keys

There are different types of SSH keys; most commonly used are Ed25519 and RSA keys. The former are faster and smaller but the latter are universally supported. At the office we need to use RSA keys.

## How to generate an SSH key

Before generating a new key, check if you already have an existing RSA key.

On mac, ssh keys are usually stored at `/home/<your user name>/.ssh/`. The dot in front of the folder name indicates that it is a hidden folder. To show them in the Finder press `Command + Shift + .`. If you do not have the folder or it's empty, proceed to generate a new key.

### MacOS

1. Open the Terminal and enter the following command to generate a new RSA key that has your office email address as a comment.  
  `ssh-keygen -t rsa -b 2048 -C "<your-email>"`
2. Accept the suggested filename and directory.
3. Specify a passphrase.
