# InfraStructure as Code Development Station

Collection of scripts for configured Development Machine with a set of Required Tools and Settings.

## Features

* asdf as package manager for many tools, like helm, terraform etc.
* install vscode as Editor
* zsh as default
* Configure SSH Keys from local Passwordstore (pass)

## Testing
### Vagrant Box

Sources: `./local`

## Usage

```
ansible-playbook \
  src/playbooks/playbook-toolset.yaml \
  -i ./inventories/general \
  -i ./inventories/private \
  --ask-become-pass
```

```
ansible-playbook \
  src/playbooks/playbook-toolset.yaml \
  -i ./inventories/general \
  -i ./inventories/private \
  --limit lenovo \
  --tags clitools\
  --ask-become-pass
```

```
ansible roger \
  -m ping \
  -i ./inventories/general \
  -i ./inventories/private \
  --ask-become-pass
```