# ssh deployments

Adds SSH key to ssh-agent

# Configuration

Pass configuration with `env` vars

1. `SSH_PRIVATE_KEY` [required]

This should be the private key part of an ssh key pair. The public key part should be added to the authorized_keys file on the server that receives the deployment.

2. `SSH_AUTH_SOCK` [optional]

Where to place the SSH Agent auth socket

# Usage

```
  - name: Adds SSH key to ssh-agent
    uses: irishdistillers/github-actions-ssh@master
    env:
      SSH_PRIVATE_KEY: ${{ secrets.SERVER_SSH_KEY }}
      SSH_AUTH_SOCK: "/tmp/ssh-auth.sock"
```
