# Ansible stuff goes here

## Convert inventory ini to yaml or json

| Format | Command |
| --- | --- |
| yaml | `ansible-inventory -i inventory.ini -y --list > inventory.yaml` |
| json | `ansible-inventory -i inventory.ini --list > inventory.yaml` |


## Linode deployment
`https://www.linode.com/docs/guides/deploy-linodes-using-ansible/`

## Adding hostname with hard coded IP addresses in inventory file
`server1 ansible_host=192.168.45.12`

## Using apt-key

Which is being [deprecated.](https://www.jeffgeerling.com/blog/2022/aptkey-deprecated-debianubuntu-how-fix-ansible)

## Semaphore ansible GUI

[on my investigate and test list](https://docs.semui.co/)
