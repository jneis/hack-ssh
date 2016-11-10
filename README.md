# hack-ssh
hacking ssh server &amp; clients

### Setup

- Copy public key from local machine to remote (using password authentication with remote credentials)

  `$~> ssh-copy-id remote`

- Disable password authentication on remote machine

   `$~> vim /etc/ssh/sshd_config`

   `
   ...
   PermitEmptyPasswords no
   ...
   PasswordAuthentication no
   ...
   `


