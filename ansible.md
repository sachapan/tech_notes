# Ansible stuff goes here

## Convert inventory ini to yaml or json

| Format | Command |
| --- | --- |
| yaml | `ansible-inventory -i inventory.ini -y --list > inventory.yaml` |
| json | `ansible-inventory -i inventory.ini --list > inventory.yaml` |


## Linode deployment
`https://www.linode.com/docs/guides/deploy-linodes-using-ansible/`

## Using apt-key

Which is being [deprecated.](https://www.jeffgeerling.com/blog/2022/aptkey-deprecated-debianubuntu-how-fix-ansible)
