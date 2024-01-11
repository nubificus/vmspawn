# vmspawn
Action to spawn a kcli VM and run a command

Use with a workflow like the following:

```
name: Create a kcli VM and run a command

on:
  push:
    branches: 
    - main

jobs:
  vmspawn:
    runs-on: [self-hosted, x86_64]
    steps:
      - name: Do vm-spawn
        uses: nubificus/vmspawn@v1
        with:
          kcli_key: ${{ secrets.KCLI_ID_RSA }}
          script: "ls -latr /tmp"
```
