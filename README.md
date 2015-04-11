# vagrant-wordpress

A simple Vagrant configuration for Wordpress provisioned with Ansible

## Requirements

- [Vagrant](https://www.vagrantup.com/)
- [Ansible](http://www.ansible.com/)

## Setup

If the Vagrant plugin hostsupdater (https://github.com/cogitatio/vagrant-hostsupdater) is installed, the following will automatically configure your local machine's hosts file to be aware of the domains specified below. Watch the provisioning script as you may need to enter a password for Vagrant to access your hosts file. If not, update your hosts file to include this line:

```
192.168.50.2 www.wordpress.dev
```

## Getting Started

1. `git clone --recursive https://github.com/slogsdon/vagrant-wordpress`
2. `cd vagrant-wordpress`
3. `vagrant up`
4. Head to <http://www.wordpress.local>

## License

vagrant-wordpress is released under the MIT License.

See [LICENSE](https://github.com/slogsdon/vagrant-wordpress/blob/master/LICENSE) for details.
