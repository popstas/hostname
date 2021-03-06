## ANXS - hostname [![Build Status](https://travis-ci.org/viasite-ansible/ansible-role-hostname.png)](https://travis-ci.org/viasite-ansible/ansible-role-hostname)

Ansible role that sets the hostname and FQDN of the node.


#### Variables

This depends on your ansible hosts inventory.

Add the hosts to your inventory with their FQDN (e.g. foo.bar.com), and the role will take care of setting your hostname accordingly (hostname: foo, FQDN: foo.bar.com).

If you just name it with the hostname in the inventory, it will similarly work (hostname set, but no FQDN attached to it).

#### Example

Your inventory file should look like this:

```yaml
foo.bar.com     ansible_ssh_host=xxx.xxx.xxx.xxx    ansible_ssh_port=22
baz.bar.com     ansible_ssh_host=xxx.xxx.xxx.xxx    ansible_ssh_port=22
```

And the structure of the files in your host_vars folders should match accordingly:

```
- host_vars
    |- foo.bar.com
    |- baz.bar.com
```


#### Testing
This project comes with a VagrantFile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant
