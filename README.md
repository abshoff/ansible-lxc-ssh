# ansible-lxc-ssh

This Ansible connection plugin connects to [LXC containers](https://linuxcontainers.org/lxc/news/) running on a host machine by using `ssh` to connect to the host machine and `sudo lxc-attach` to enter the container.

To load the plugin, place it into the connection plugin directory or reference the plugin path in `ansible.cfg`.

```ini
[defaults]
connection_plugins = /path/to/connection_plugins/lxc_ssh
```

Then, modify your `hosts` file to use the `lxc_ssh` transport:

```yaml
ansible_connection: lxc_ssh
ansible_host: lxc_host
lxc_container: lxc_container
```

Containers can be created with the Ansible `lxc_container` module.

## Fork

This version has been forked from [Andreas Scherbaum](https://github.com/andreasscherbaum/ansible-lxc-ssh) which had been forked from the original author [Pierre Chifflier](https://github.com/chifflier/ansible-lxc-ssh). Various other authors have also contributed to the project.

The main difference of this fork is the focus on compatability with the `lxc-*` tools in a `sudo` setting and different Ansible releases. It will be synced with the other repositories from time to time.
