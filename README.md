# Getting started with Selective Replication

  1. Run the following commands to create the yml policy
```bash
export SAFE_NAME="<safe-name>"
envsubst '$SAFE_NAME' < templates/sr-follower-prod.yml.tmp > sr-follower-prod.yml
```

  2. Load the policy once after logging in via Conjur CLI
```bash
# Enter login creds to get CLI session token
conjur login

# Load the policy to root from template
conjur policy load -b root -f sr-follower-prod.yml
```
